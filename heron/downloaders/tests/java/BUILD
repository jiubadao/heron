load("/tools/rules/java_tests", "java_tests")

load("/tools/rules/heron_deps", "heron_java_proto_files")

common_deps_files = [
    "//third_party/java:powermock",
    "//third_party/java:mockito",
    "//third_party/java:junit4",
    "//third_party/java:commons-compress",
    "//heron/common/src/java:basics-java",
]

downloader_test_deps_files = \
  common_deps_files + [
    "//heron/downloaders/src/java:heron-downloader"
  ]

java_library(
    name = "tests",
    srcs = glob(["**/downloader/**/*.java"]),
    deps = downloader_test_deps_files,
)

java_tests(
  test_classes = [
    "com.twitter.heron.downloader.ExtractorTests",
  ],
  runtime_deps = [ ":tests" ],
  size = "small",
)
