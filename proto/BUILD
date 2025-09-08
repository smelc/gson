load("@rules_proto//proto:defs.bzl", "proto_library")
load("@rules_java//java:defs.bzl", "java_proto_library", "java_library")

java_library(
    name = "proto",
    srcs = glob(["src/main/java/**/*.java"]),
    visibility = ["//visibility:public"],
    deps = [
        "//gson",
        "@maven//:com_google_protobuf_protobuf_java",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_errorprone_error_prone_annotations",
    ],
)
