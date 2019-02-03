load("@io_bazel_rules_scala//scala:scala.bzl", "scala_library")

scala_library(
    name = "firrtl",
    srcs = glob(["**/*.scala"]),
    scalac_jvm_flags = ["-Xss2M"],
    deps = [
        "//src/main/antlr4:firrtl_antlr4_java_lib",
	"//src/main/proto:firrtl_java_proto",
        "//3rdparty/jvm/ch/qos/logback:logback_classic",
        "//3rdparty/jvm/com/github/scopt",
        "//3rdparty/jvm/com/typesafe/scala_logging",
        "//3rdparty/jvm/net/jcazevedo:moultingyaml",
	"//3rdparty/jvm/org/json4s:json4s_native",
        "//3rdparty/jvm/org/scalacheck",
        "//3rdparty/jvm/org/scalatest",
        "@antlr4_runtime//jar",
        "@com_google_protobuf//:protobuf_java",
    ],
    exports = [
        "//3rdparty/jvm/net/jcazevedo:moultingyaml",
	"//3rdparty/jvm/com/github/scopt",
        "//3rdparty/jvm/com/typesafe/scala_logging",
      
    ],
    visibility = ["//visibility:public"],
)
