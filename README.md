# Quill Homebrew tap

[![Test Quill Formula](https://github.com/treblereel/homebrew-quill/actions/workflows/test.yml/badge.svg)](https://github.com/treblereel/homebrew-quill/actions/workflows/test.yml)
[![License: Apache-2.0](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](LICENSE)

Native [Quill](https://github.com/treblereel/quill) binaries for macOS and Linux, on Apple Silicon / ARM64 and Intel / AMD64.

Quill is a native code intelligence MCP server for JVM projects. This tap distributes its prebuilt release binaries through Homebrew.

## Install

```sh
brew install treblereel/quill/quill
quill --version
```

Homebrew downloads a prebuilt native executable and verifies its SHA-256 checksum.

Kotlin semantic analysis requires Java 17 or newer. Quill uses `JAVA_HOME`, then `java` on `PATH`; use your project’s JDK. Run `quill init` in a compiled Maven or Gradle project to prepare its index and Kotlin compiler runtime.

## Upgrade

```sh
brew update
brew upgrade treblereel/quill/quill
```

## Verify

```sh
brew test treblereel/quill/quill
```

CI installs and tests the checked-out formula on macOS and Linux, on ARM64 and x86_64. The formula test checks CLI version/help, MCP initialization, tool discovery, and clean shutdown after EOF.

## Maintaining the tap

The initial formula installs the published Quill `v0.2.0` release. Formula versions track published releases, rather than unreleased source changes.

The [Quill release workflow](https://github.com/treblereel/quill/blob/main/.github/workflows/release.yml) generates formulas from downloaded archives with verified checksums. Configure `HOMEBREW_TAP_REPOSITORY=treblereel/homebrew-quill` and `HOMEBREW_TAP_TOKEN` in the source repository to open update pull requests automatically. The token needs Contents and Pull requests write access to this tap. Updates take effect after the pull request is merged.

See [distribution setup](https://github.com/treblereel/quill/blob/main/packaging/homebrew/README.md) for the release and token setup instructions.

## Support

For Quill usage and configuration, see the [main project](https://github.com/treblereel/quill). Report analysis and runtime issues in [Quill](https://github.com/treblereel/quill/issues); report formula or Homebrew installation issues in [this tap](https://github.com/treblereel/homebrew-quill/issues).

Quill is licensed under [Apache-2.0](LICENSE).
