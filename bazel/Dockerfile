FROM openjdk:8-alpine

ARG version=0.5.4
ARG os=$(uname -o)
ARG arch=$(uname -m)

RUN apk add --no-cache --virtual .build-deps wget zip g++ unzip python bash && \
  wget -q https://github.com/bazelbuild/bazel/releases/download/${version}/bazel-${version}-without-jdk-installer-${os}-${arch}.sh && \
  chmod +x bazel-${version}-without-jdk-installer-${os}-${arch}.sh && \
  bash bazel-${version}-without-jdk-installer-${os}-${arch}.sh --prefix=/ && \
  bazel && \
  apk del .build-deps

CMD ["bazel"]
