FROM openjdk:8-alpine

ARG version=0.5.4

RUN apk add --no-cache --virtual .build-deps wget && \
wget -q https://github.com/bazelbuild/bazel/releases/download/${version}/bazel-${version}-installer-linux-x86_64.sh && \
chmod +x bazel-${version}-installer-linux-x86_64.sh && \
pwd && ls -la && \
bazel-${version}-installer-linux-x86_64.sh && \
apk del .build-deps

CMD ["bazel"]
