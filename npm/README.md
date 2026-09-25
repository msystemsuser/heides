# heides (npm installer)

[![npm](https://img.shields.io/npm/v/heides)](https://www.npmjs.com/package/heides) [![license](https://img.shields.io/npm/l/heides)](LICENSE) [![MCP](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io) [![Tawakkul Labs](https://img.shields.io/badge/by-Tawakkul%20Labs-0f766e)](https://tawakkul-labs.co.ke)

Installs the prebuilt [HEIDES](https://github.com/AbduljabbarBXR/heides) binary for your platform and exposes the `heides` command. HEIDES is a deterministic code analysis harness that gives AI agents senses, memory and judgment for code.

```bash
npm install -g heides
heides --help
```

On install, the matching binary is downloaded from GitHub Releases into the package `bin/` folder. No Rust toolchain needed.

## Supported platforms

| OS | Arch | Asset |
|----|------|-------|
| Linux (glibc) | x64 | `heides-x86_64-unknown-linux-gnu` |
| Linux (glibc) | arm64 | `heides-aarch64-unknown-linux-gnu` |
| Android / Termux | arm64 | `heides-aarch64-linux-android` |
| macOS | arm64 | `heides-aarch64-apple-darwin` |
| macOS | x64 | `heides-x86_64-apple-darwin` |
| Windows | x64 | `heides-x86_64-pc-windows-msvc.exe` |

Other platforms, including musl/Alpine, are not supported by the installer. Install from source instead (`cargo install heides`) or pick a build from the [releases page](https://github.com/AbduljabbarBXR/heides/releases).

## Usage

Same as the native binary:

```bash
heides scan .
heides check .
heides mcp   # MCP server over stdio for agents
```

## Versions

The npm package version and HEIDES binary version are managed separately. The installer downloads HEIDES 0.14.4 by default; set `HEIDES_BIN_VERSION` during installation to select another release.

## Uninstall

```bash
npm uninstall -g heides
```

## License

MIT. See [LICENSE](./LICENSE). Binary builds follow the [HEIDES repo license](https://github.com/AbduljabbarBXR/heides).

---

Links: [npm](https://www.npmjs.com/package/heides) | [GitHub](https://github.com/AbduljabbarBXR/heides) | [Tawakkul Labs](https://tawakkul-labs.co.ke)
