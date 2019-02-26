load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_macro_library")

scala_macro_library(
    name = "berkeley_hardfloat",
    srcs = glob(["src/main/scala/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
    deps = ["@chisel3//:chisel3"],
    visibility = ["//visibility:public"],
    scalacopts = ["-Xsource:2.11"],
)


