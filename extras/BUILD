java_library(
    name = "extras",
    srcs = glob(["src/main/java/com/google/gson/**/*.java"]),
    visibility = ["//visibility:public"],
    deps = [
        "//gson",
        "@maven//:com_google_errorprone_error_prone_annotations",
        "@maven//:javax_annotation_jsr250_api",
    ],
)

java_test(
    name = "GraphAdapterBuilderTest",
    srcs = ["src/test/java/com/google/gson/graph/GraphAdapterBuilderTest.java"],
    test_class = "com.google.gson.graph.GraphAdapterBuilderTest",
    deps = [
        ":extras",
        "//gson",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
    ],
)

java_test(
    name = "InterceptorTest",
    srcs = ["src/test/java/com/google/gson/interceptors/InterceptorTest.java"],
    test_class = "com.google.gson.interceptors.InterceptorTest",
    deps = [
        ":extras",
        "//gson",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
    ],
)

java_test(
    name = "PostConstructAdapterFactoryTest",
    srcs = ["src/test/java/com/google/gson/typeadapters/PostConstructAdapterFactoryTest.java"],
    test_class = "com.google.gson.typeadapters.PostConstructAdapterFactoryTest",
    deps = [
        ":extras",
        "//gson",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
        "@maven//:javax_annotation_jsr250_api",
    ],
)

java_test(
    name = "RuntimeTypeAdapterFactoryTest",
    srcs = ["src/test/java/com/google/gson/typeadapters/RuntimeTypeAdapterFactoryTest.java"],
    test_class = "com.google.gson.typeadapters.RuntimeTypeAdapterFactoryTest",
    deps = [
        ":extras",
        "//gson",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
    ],
)

java_test(
    name = "UtcDateTypeAdapterTest",
    srcs = ["src/test/java/com/google/gson/typeadapters/UtcDateTypeAdapterTest.java"],
    test_class = "com.google.gson.typeadapters.UtcDateTypeAdapterTest",
    deps = [
        ":extras",
        "//gson",
        "@maven//:junit_junit",
        "@maven//:com_google_truth_truth",
    ],
)

test_suite(
    name = "tests",
    tests = [
        "GraphAdapterBuilderTest",
        "InterceptorTest",
        "PostConstructAdapterFactoryTest",
        "RuntimeTypeAdapterFactoryTest",
        "UtcDateTypeAdapterTest",
    ],
)
