config_setting(
    name = "java17",
    values = {"java_language_version": "17"},
)

TEST_DEPS = [
        "//gson:gson",
        "@maven//:org_junit_jupiter_junit_jupiter",
        "@maven//:org_junit_jupiter_junit_jupiter_api",
        "@maven//:com_google_truth_truth",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_guava_guava_testlib",
    ]

java_test(
    name = "tests",
    srcs = select({
            ":java17": ["src/test/java/com/google/gson/native_test/ReflectionTest.java",
                        "src/test/java/com/google/gson/native_test/Java17RecordReflectionTest.java"],
            "//conditions:default": ["src/test/java/com/google/gson/native_test/ReflectionTest.java"]
    }),
    test_class = "com.google.gson.native_test.ReflectionTest",
    deps = TEST_DEPS
)
