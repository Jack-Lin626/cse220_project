load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library", "scala_macro_library")

scala_macro_library(
    name = "rocketchip",
    srcs = glob(["src/main/**/*.scala"]),
    deps = [":rocketchip_macros",
    	    "//chisel3:chisel3",
	    "//berkeley-hardfloat:berkeley-hardfloat",
	   ],
    plugins = ["@org_scalamacros_paradise_2_11_12//jar"],

)

scala_macro_library(
    name = "rocketchip_macros",
    srcs = glob(["macros/**/*.scala"]),
    plugins = ["@org_scalamacros_paradise_2_11_12//jar"],
)