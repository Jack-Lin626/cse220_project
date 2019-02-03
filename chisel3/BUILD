load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_macro_library")

scala_macro_library(
    name = "chisel3",
    srcs = glob(["src/main/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
    visibility = ["//visibility:public"],
    exports = [
        ":chisel_frontend",
        ":core_macros",
        "@firrtl//src/main/scala:firrtl",
    ],
    deps = [
        ":chisel_frontend",
        ":core_macros",
        "//3rdparty/jvm/org/scalacheck",
        "//3rdparty/jvm/org/scalatest",
        "@com_google_protobuf//:protobuf_java",
        "@firrtl//src/main/proto:firrtl_java_proto",
        "@firrtl//src/main/scala:firrtl",
        "@io_bazel_rules_scala_scala_library",
        "@io_bazel_rules_scala_scala_reflect",
    ],
)

scala_macro_library(
    name = "core_macros",
    srcs = glob(["coreMacros/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
)

scala_macro_library(
    name = "chisel_frontend",
    srcs = glob(["chiselFrontend/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
    deps = [
        ":core_macros",
        "@firrtl//src/main/scala:firrtl",
    ],
)
