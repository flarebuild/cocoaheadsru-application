workspace(name = "cocoaheadsru_application")

load(
    "@bazel_tools//tools/build_defs/repo:git.bzl",
    "git_repository",
)

# rules_apple, rules_swift and apple_support no longer support releases. If
# you'd like to pin down these dependencies to a specific commit, please add the
# following to the top of your WORKSPACE, using the commit you'd like to pin for
# each of the repositories.
git_repository(
    name = "build_bazel_rules_apple",
    remote = "https://github.com/bazelbuild/rules_apple.git",
    commit = "2c24d057f6597846fcdb957d0e9f0d452bb336c9",
)

git_repository(
    name = "build_bazel_rules_swift",
    remote = "https://github.com/bazelbuild/rules_swift.git",
    commit = "8767e70f1a8b500f5f3683cb23258964737a3888",
)

load(
    "@build_bazel_rules_apple//apple:repositories.bzl",
    "apple_rules_dependencies",
)

apple_rules_dependencies()

load(
    "@build_bazel_rules_swift//swift:repositories.bzl",
    "swift_rules_dependencies",
)

swift_rules_dependencies()

load(
    "@com_google_protobuf//:protobuf_deps.bzl",
    "protobuf_deps",
)

protobuf_deps()
