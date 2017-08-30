FROM openjdk:8

RUN echo "deb [arch=amd64] http://storage.googleapis.com/bazel-apt stable jdk1.8" | tee /etc/apt/sources.list.d/bazel.list; \
curl https://bazel.build/bazel-release.pub.gpg | apt-key add - ; \
apt-get update && apt-get install bazel -y && apt-get clean; \
bazel && mkdir /build
# need to extract stuff on first run

WORKDIR /build
CMD ["bazel"]
