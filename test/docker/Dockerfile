FROM xotosphere/testinfra:5.2.2-python-3.8.5-slim-buster as test-testinfra
FROM xotosphere/base-image:sut as test-build

# fix issue "/usr/local/bin/python: error while loading shared libraries: libpython3.8.so.1.0: cannot open shared object file: No such file or directory"
ENV LD_LIBRARY_PATH=/usr/local/lib

ARG DOCKER_TEST_DIR=./docker/test

RUN mkdir -p $DOCKER_TEST_DIR

WORKDIR $DOCKER_TEST_DIR

COPY --from=test-testinfra /usr/local/lib /usr/local/lib
COPY --from=test-testinfra /usr/local/bin /usr/local/bin

# COPY --chown=$USER_NAME:$USER_GROUP ./test .
COPY --chown=$USER_NAME:$USER_GROUP ./ .

ENTRYPOINT ["pytest"]
