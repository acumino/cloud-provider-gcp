load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = ["resolver.go"],
    importmap = "k8s.io/cloud-provider-gcp/vendor/go.etcd.io/etcd/client/v3/internal/resolver",
    importpath = "go.etcd.io/etcd/client/v3/internal/resolver",
    visibility = ["//vendor/go.etcd.io/etcd/client/v3:__subpackages__"],
    deps = [
        "//vendor/go.etcd.io/etcd/client/v3/internal/endpoint:go_default_library",
        "//vendor/google.golang.org/grpc/resolver:go_default_library",
        "//vendor/google.golang.org/grpc/resolver/manual:go_default_library",
        "//vendor/google.golang.org/grpc/serviceconfig:go_default_library",
    ],
)
