package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = ["pki_helpers_test.go"],
    importpath = "k8s.io/kubernetes/cmd/kubeadm/app/phases/certs/pkiutil",
    library = ":go_default_library",
    deps = ["//vendor/k8s.io/client-go/util/cert:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = ["pki_helpers.go"],
    importpath = "k8s.io/kubernetes/cmd/kubeadm/app/phases/certs/pkiutil",
    deps = ["//vendor/k8s.io/client-go/util/cert:go_default_library"],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)
