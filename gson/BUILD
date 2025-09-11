genrule(
    name = "gson_build_config_generator",
    srcs = ["src/main/java-templates/com/google/gson/internal/GsonBuildConfig.java"],
    outs = ["GsonBuildConfig.java"],
    cmd = "sed 's/$${project.version}/2.13.2-SNAPSHOT/' $< > $@",
)

java_library(
    name = "gson_build_config",
    srcs = [":gson_build_config_generator"],
)

java_library(
    name = "gson",
    srcs = glob(
        ["src/main/java/com/google/gson/**/*.java"],
    ),
    visibility = ["//visibility:public"],
    deps = [
        ":gson_build_config",
        "@maven//:com_google_errorprone_error_prone_annotations",
    ],
)

java_test(
    name = "tests",
    srcs = glob(["src/test/java/com/google/gson/**/*.java"]),
    test_class = "com.google.gson.GsonTest",
    deps = [
        ":gson",
        ":gson_build_config",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_guava_guava_testlib",
    ],
)
