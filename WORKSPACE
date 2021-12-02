workspace(
    name = "frontend",
    managed_directories = {"@npm": ["frontend:node_modules"]},
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "f7037c8e295fdc921f714962aee7c496110052511e2b14076bd8e2d46bc9819c",
    urls = ["https://github.com/bazelbuild/rules_nodejs/releases/download/4.4.5/rules_nodejs-4.4.5.tar.gz"],
)

load("@build_bazel_rules_nodejs//:index.bzl", "yarn_install")

yarn_install(
    name = "npm",
    package_json = "//frontend:package.json",
    yarn_lock = "//frontend:yarn.lock",
)
