load("@io_bazel_rules_go//proto:def.bzl", "go_proto_library")
load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["snap.pb.go"],
    importpath = "github.com/coreos/etcd/snap/snappb",
    visibility = ["//visibility:public"],
    deps = ["//vendor/github.com/golang/protobuf/proto:go_default_library"],
)

proto_library(
    name = "snappb_proto",
    srcs = ["snap.proto"],
    visibility = ["//visibility:public"],
    deps = ["//gogoproto:gogoproto_proto"],
)

go_proto_library(
    name = "snappb_go_proto",
    importpath = "github.com/coreos/etcd/snap/snappb",
    proto = ":snappb_proto",
    visibility = ["//visibility:public"],
    deps = ["//gogoproto:go_default_library"],
)
