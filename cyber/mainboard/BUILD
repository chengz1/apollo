load("//tools:cpplint.bzl", "cpplint")
load("//tools:apollo_package.bzl", "apollo_package", "apollo_cc_binary")

package(default_visibility = ["//visibility:public"])

apollo_cc_binary(
    name = "mainboard",
    srcs = [
        "mainboard.cc",
        "module_argument.cc",
        "module_argument.h",
        "module_controller.cc",
        "module_controller.h",
    ],
    linkopts = [
        "-pthread",
        "-lprofiler",
        "-ltcmalloc",
    ],
    deps = [
        "//cyber",
        "//cyber/common:cyber_common",
        "//cyber/plugin_manager:cyber_plugin_manager",
        "//cyber/proto:dag_conf_cc_proto",
    ],
)

apollo_package()
cpplint()
