package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "admission.go",
        "config.go",
        "doc.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/imagepolicy",
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/api/imagepolicy/v1alpha1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/runtime/schema:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/cache:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/yaml:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/admission:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/util/webhook:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/apis/imagepolicy/install:go_default_library",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "admission_test.go",
        "certs_test.go",
        "config_test.go",
    ],
    importpath = "k8s.io/kubernetes/plugin/pkg/admission/imagepolicy",
    library = ":go_default_library",
    deps = [
        "//vendor/k8s.io/api/imagepolicy/v1alpha1:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/admission:go_default_library",
        "//vendor/k8s.io/apiserver/pkg/authentication/user:go_default_library",
        "//vendor/k8s.io/client-go/tools/clientcmd/api/v1:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/apis/imagepolicy/install:go_default_library",
    ],
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
