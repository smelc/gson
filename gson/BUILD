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
