load("@rules_java//java:defs.bzl", "java_library", "java_test")

package(
    default_testonly = 1,
    default_visibility = ["//src:__subpackages__"],
)

filegroup(
    name = "srcs",
    testonly = 0,
    srcs = glob(["**"]),
    visibility = ["//src:__subpackages__"],
)

java_test(
    name = "AarImportTest",
    srcs = ["AarImportTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidSkylarkTest",
    srcs = ["AndroidSkylarkTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib:syntax",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/packages",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//src/test/java/com/google/devtools/build/lib/packages:testutil",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidSkylarkCommonTest",
    srcs = ["AndroidSkylarkCommonTest.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidCommonTest",
    srcs = ["AndroidCommonTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_library(
    name = "AndroidBuildViewTestCase",
    srcs = ["AndroidBuildViewTestCase.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/main/protobuf:android_deploy_info_java_proto",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//src/test/java/com/google/devtools/build/lib/rules/java:java_compile_action_test_helper",
        "//third_party:guava",
        "//third_party:jsr305",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidBinaryTest",
    timeout = "long",
    srcs = ["AndroidBinaryTest.java"],
    shard_count = 5,
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/packages",
        "//src/main/java/com/google/devtools/build/lib/packages:build_type",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/cpp",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/main/java/com/google/devtools/build/lib/util:filetype",
        "//src/main/java/com/google/devtools/build/lib/vfs",
        "//src/main/protobuf:android_deploy_info_java_proto",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/packages:testutil",
        "//src/test/java/com/google/devtools/build/lib/rules/java:java_compile_action_test_helper",
        "//src/test/java/com/google/devtools/build/lib/testutil:JunitUtils",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "ResourceFilterFactoryTest",
    srcs = ["ResourceFilterFactoryTest.java"],
    deps = [
        ":ResourceTestBase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidResourcesTest",
    srcs = ["AndroidResourcesTest.java"],
    deps = [
        ":ResourceTestBase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/packages",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/vfs:pathfragment",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidAssetsTest",
    srcs = ["AndroidAssetsTest.java"],
    deps = [
        ":ResourceTestBase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/vfs:pathfragment",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_library(
    name = "ResourceTestBase",
    srcs = ["ResourceTestBase.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/events",
        "//src/main/java/com/google/devtools/build/lib/packages",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/vfs",
        "//src/main/java/com/google/devtools/build/lib/vfs/inmemoryfs",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidDeviceScriptFixtureTest",
    srcs = ["AndroidDeviceScriptFixtureTest.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidHostServiceFixtureTest",
    srcs = ["AndroidHostServiceFixtureTest.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidInstrumentationTestTest",
    srcs = ["AndroidInstrumentationTestTest.java"],
    tags = ["no_windows"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidLibraryTest",
    srcs = ["AndroidLibraryTest.java"],
    shard_count = 5,
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/main/java/com/google/devtools/build/lib/vfs:pathfragment",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/rules/java:java_compile_action_test_helper",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidDeviceTest",
    srcs = ["AndroidDeviceTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/packages",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_library(
    name = "AndroidMultidexBaseTest",
    srcs = ["AndroidMultidexBaseTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidBinaryMultidexTest",
    srcs = ["AndroidBinaryMultidexTest.java"],
    deps = [
        ":AndroidMultidexBaseTest",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//third_party:junit4",
    ],
)

java_test(
    name = "AndroidDataBindingTest",
    srcs = ["AndroidDataBindingTest.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/main/protobuf:extra_actions_base_java_proto",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/rules/java:java_compile_action_test_helper",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidDataBindingV2Test",
    srcs = ["AndroidDataBindingV2Test.java"],
    tags = ["manual"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-compilation",
        "//src/main/protobuf:extra_actions_base_java_proto",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/rules/java:java_compile_action_test_helper",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidSdkTest",
    srcs = ["AndroidSdkTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/test/java/com/google/devtools/build/lib/analysis/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_library(
    name = "AbstractAndroidLocalTestTestBase",
    srcs = ["AbstractAndroidLocalTestTestBase.java"],
    deps = [
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_library(
    name = "AndroidLocalTestTest",
    srcs = ["AndroidLocalTestTest.java"],
    deps = [
        ":AbstractAndroidLocalTestTestBase",
        ":AndroidBuildViewTestCase",
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/rules/java:java-rules",
        "//src/test/java/com/google/devtools/build/lib/actions/util",
        "//src/test/java/com/google/devtools/build/lib/testutil",
        "//src/test/java/com/google/devtools/build/lib/testutil:JunitUtils",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

java_test(
    name = "AndroidDataConverterTest",
    srcs = ["AndroidDataConverterTest.java"],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/android",
        "//src/main/java/com/google/devtools/build/lib/vfs:pathfragment",
        "//third_party:guava",
        "//third_party:junit4",
        "//third_party:truth",
    ],
)

test_suite(
    name = "windows_tests",
    tags = [
        "-no_windows",
        "-slow",
    ],
)

test_suite(
    name = "all_windows_tests",
    tests = [
        ":windows_tests",
    ],
)
