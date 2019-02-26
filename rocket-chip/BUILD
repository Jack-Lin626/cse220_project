load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_macro_library")

scala_macro_library(
    name = "rocketchip",
    srcs = glob(["src/main/**/*.scala"]),
    deps = [":rocketchip_macros",
    	    "@chisel3//:chisel3",
	    "@berkeley_hardfloat//:berkeley_hardfloat",
	    "//3rdparty/jvm/org/json4s:json4s_native",
    	    "//3rdparty/jvm/org/json4s:json4s_jackson",    


],
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
    scalacopts = ["-Xsource:2.11"],

)

scala_macro_library(
    name = "rocketchip_macros",
    srcs = glob(["macros/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_12_8//jar"],
)