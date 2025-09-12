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
    name = "reflection_test",
    srcs = ["src/test/java/com/google/gson/native_test/ReflectionTest.java"],
    test_class = "com.google.gson.native_test.ReflectionTest",
    deps = TEST_DEPS
)

java_test(
    name = "java17_record_reflection_test",
    srcs = ["src/test/java/com/google/gson/native_test/Java17RecordReflectionTest.java"],
    test_class = "com.google.gson.native_test.Java17RecordReflectionTest",
    deps = TEST_DEPS
)

test_suite(
    name = "tests",
    tests = select({
        ":java17": [
            ":reflection_test",
            ":java17_record_reflection_test",
        ],
        "//conditions:default": [":reflection_test"],
    }),

)
