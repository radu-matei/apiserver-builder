package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_test",
)

go_test(
    name = "go_default_test",
    size = "large",
    srcs = [
        "attach_detach_test.go",
        "main_test.go",
        "persistent_volumes_test.go",
    ],
    importpath = "k8s.io/kubernetes/test/integration/volume",
    tags = ["integration"],
    deps = [
        "//vendor/github.com/golang/glog:go_default_library",
        "//vendor/k8s.io/api/core/v1:go_default_library",
        "//vendor/k8s.io/api/storage/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/api/resource:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/util/wait:go_default_library",
        "//vendor/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//vendor/k8s.io/client-go/informers:go_default_library",
        "//vendor/k8s.io/client-go/kubernetes:go_default_library",
        "//vendor/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/client-go/tools/cache:go_default_library",
        "//vendor/k8s.io/client-go/tools/reference:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/api/testapi:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/cloudprovider/providers/fake:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/controller/volume/attachdetach:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/controller/volume/attachdetach/cache:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/controller/volume/persistentvolume:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/volume:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/volume/testing:go_default_library",
        "//vendor/k8s.io/kubernetes/pkg/volume/util/volumehelper:go_default_library",
        "//vendor/k8s.io/kubernetes/test/integration/framework:go_default_library",
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
