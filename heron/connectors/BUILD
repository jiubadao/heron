package(default_visibility = ["//visibility:public"])

load("/tools/rules/pex_rules", "pex_library", "pex_binary")

pex_library(
    name = "heron-pythonconnectors-py",
    srcs = glob(["**/*.py"]),
    deps = [
        "//heron/api/src/python:heron-python-py",
    ],
    # TODO:- We should turn this on as soon as bazel issues are resolved
    # reqs = ['pulsar-client==1.19.dev2']
)

# for egg production
pex_binary(
    name = "heron-pythonconnectors-package",
    srcs = glob(["**/*.py"]),
    deps = [
        "//heron/api/src/python:heron-python-py",
    ]
)

