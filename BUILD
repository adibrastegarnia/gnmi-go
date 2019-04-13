load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")

go_proto_library(
    name = "gnmi_go_proto",
    compiler = "@io_bazel_rules_go//proto:go_grpc",
    importpath = "proto/gnmi",
    proto = ":gnmi_proto",
    visibility = ["//visibility:public"],
    deps = [
        "gnmi_ext_go_proto"
    ],
)

go_proto_library(
    name = "gnmi_ext_go_proto",
    compiler = "@io_bazel_rules_go//proto:go_grpc",
    importpath = "proto/gnmi_ext",
    proto = ":gnmi_ext_proto",
    visibility = ["//visibility:public"],
    
)


proto_library(
    name = "gnmi_proto",
    srcs = ["proto/gnmi.proto"],
    deps = [
        "@com_google_protobuf//:any_proto",
        "@com_google_protobuf//:descriptor_proto",
        ":gnmi_ext_proto"
    ],
    visibility = ["//visibility:public"],
)

proto_library(
    name = "gnmi_ext_proto",
    srcs = ["proto/gnmi_ext.proto"],
    deps = [
        "@com_google_protobuf//:any_proto",
        "@com_google_protobuf//:descriptor_proto"
    ],
    visibility = ["//visibility:public"],
)


