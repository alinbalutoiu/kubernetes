package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = select({
        "@io_bazel_rules_go//go/platform:android": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:darwin": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:dragonfly": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:freebsd": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:linux": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:nacl": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:netbsd": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:openbsd": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:plan9": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:solaris": [
            "service_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:windows": [
            "service_windows.go",
        ],
        "//conditions:default": [],
    }),
    importpath = "k8s.io/kubernetes/pkg/util/service",
    deps = select({
        "@io_bazel_rules_go//go/platform:android": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:darwin": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:dragonfly": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:freebsd": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:linux": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:nacl": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:netbsd": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:openbsd": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:plan9": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:solaris": [
            "//vendor/github.com/spf13/pflag:go_default_library",
        ],
        "@io_bazel_rules_go//go/platform:windows": [
            "//vendor/github.com/golang/glog:go_default_library",
            "//vendor/github.com/spf13/pflag:go_default_library",
            "//vendor/golang.org/x/sys/windows:go_default_library",
            "//vendor/golang.org/x/sys/windows/svc:go_default_library",
            "//vendor/golang.org/x/sys/windows/svc/mgr:go_default_library",
        ],
        "//conditions:default": [],
    }),
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
