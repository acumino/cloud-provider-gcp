load("@io_bazel_rules_go//go:def.bzl", "go_library", "go_test")

go_library(
    name = "go_default_library",
    srcs = [
        "adapter.go",
        "cidr_allocator.go",
        "cloud_cidr_allocator.go",
        "controller_legacyprovider.go",
        "doc.go",
        "range_allocator.go",
        "timeout.go",
    ],
    importpath = "k8s.io/cloud-provider-gcp/pkg/controller/nodeipam/ipam",
    visibility = ["//visibility:public"],
    deps = [
        "//pkg/controller/nodeipam/ipam/cidrset:go_default_library",
        "//pkg/controller/nodeipam/ipam/sync:go_default_library",
        "//pkg/util:go_default_library",
        "//pkg/util/node:go_default_library",
        "//pkg/util/taints:go_default_library",
        "//providers/gce:go_default_library",
        "//vendor/github.com/google/go-cmp/cmp:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/fields:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/labels:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/types:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/runtime:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/sets:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/client-go/informers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/scheme:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/typed/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/listers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/tools/record:go_default_library",
        "//vendor/k8s.io/cloud-provider:go_default_library",
        "//vendor/k8s.io/klog/v2:go_default_library",
        "//vendor/k8s.io/metrics/pkg/client/clientset/versioned/scheme:go_default_library",
        "//vendor/k8s.io/utils/net:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "cloud_cidr_allocator_test.go",
        "controller_test.go",
        "range_allocator_test.go",
        "timeout_test.go",
    ],
    embed = [":go_default_library"],
    deps = [
        "//pkg/controller/nodeipam/ipam/cidrset:go_default_library",
        "//pkg/controller/nodeipam/ipam/test:go_default_library",
        "//pkg/controller/testutil:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/client-go/informers:go_default_library",
        "//vendor/k8s.io/client-go/informers/core/v1:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes/fake:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/controller:go_default_library",
        "//vendor/k8s.io/utils/net:go_default_library",
    ],
)
