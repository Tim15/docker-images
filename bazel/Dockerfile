FROM openjdk:8-alpine

ARG version=0.5.4

RUN apk add --no-cache --virtual .build-deps wget zip g++ unzip python bash && \
wget -q https://github.com/bazelbuild/bazel/releases/download/${version}/bazel-${version}-installer-linux-x86_64.sh && \
chmod +x bazel-${version}-installer-linux-x86_64.sh && \
bash bazel-${version}-installer-linux-x86_64.sh && \
apk del .build-deps

CMD ["bazel"]
