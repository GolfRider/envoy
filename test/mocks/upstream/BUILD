load(
    "//bazel:envoy_build_system.bzl",
    "envoy_cc_mock",
    "envoy_package",
)

envoy_package()

envoy_cc_mock(
    name = "cluster_info_mocks",
    hdrs = ["cluster_info.h"],
    deps = [
        "//include/envoy/upstream:cluster_manager_interface",
        "//include/envoy/upstream:upstream_interface",
        "//source/common/stats:stats_lib",
        "//test/mocks/runtime:runtime_mocks",
        "//test/mocks/stats:stats_mocks",
    ],
)

envoy_cc_mock(
    name = "host_mocks",
    hdrs = ["host.h"],
    deps = [
        ":cluster_info_mocks",
        "//include/envoy/upstream:upstream_interface",
        "//source/common/stats:stats_lib",
    ],
)

envoy_cc_mock(
    name = "upstream_mocks",
    srcs = ["mocks.cc"],
    hdrs = ["mocks.h"],
    deps = [
        "//include/envoy/http:async_client_interface",
        "//include/envoy/upstream:cluster_manager_interface",
        "//include/envoy/upstream:health_checker_interface",
        "//include/envoy/upstream:load_balancer_interface",
        "//include/envoy/upstream:upstream_interface",
        "//source/common/network:utility_lib",
        "//source/common/stats:stats_lib",
        "//source/common/upstream:upstream_includes",
        "//source/common/upstream:upstream_lib",
        "//test/mocks/http:http_mocks",
        "//test/mocks/runtime:runtime_mocks",
        "//test/mocks/stats:stats_mocks",
    ],
)
