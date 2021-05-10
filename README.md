# bazel_rules_playground

Following [https://www.jayconrod.com/posts/106/writing-bazel-rules--simple-binary-rule](https://www.jayconrod.com/posts/106/writing-bazel-rules--simple-binary-rule)

## Vocabulary

- **Repository** - A repository ... TODO
- **Package** - A package consists of all of the targets declared in a build file as well as all of the files and subdirectories in the directory containing the build file. Each build file implicitly defines a new package.
- **Label** - A label is a way to reference a file or target. Labels (e.g. `@io_bazel_rules_go//go:def.bzl`) consists of three parts: a repository name (`io_bazel_rules_go`), a package name (`go`), and the name of a file or target (`def.bzl`). The repository and package names can be omitted when referencing a label in the same repository or package.
- **Rule** - A rule declares files and actions that need to occur to create that file. Rules cannot perform I/O operations and therefore cannot make decisions based on source file contents.
- **Dependency Graph** - In the *loading_phase* Bazel creates a tree to understand the order in which targets need to be built.
- **File-action Graph** - In the *analysis_phase* Bazel creates a tree to understand the actions needed for each rule to produce the dependencies requested by the dependency graph.
