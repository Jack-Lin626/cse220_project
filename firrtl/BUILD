package(default_visibility = ["//visibility:public"])

load("@io_bazel_rules_scala//scala:scala.bzl", "scala_binary")

scala_binary(
    name = "firrtl_bin",
    data = ["src/main/resources/logback.xml"],
    main_class = "firrtl.Driver",
    deps = ["//src/main/scala:firrtl"],
)
