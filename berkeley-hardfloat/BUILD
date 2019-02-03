load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library")

scala_library(
    name = "berkeley-hardfloat",
    srcs = glob(["src/main/scala/**/*.scala"]),
    deps = ["//chisel3:chisel3"],
    visibility = ["//visibility:public"],
)