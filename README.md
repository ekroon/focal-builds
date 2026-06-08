# focal-builds

Pre-built binaries compiled on Ubuntu 20.04 (Focal) for glibc 2.31 compatibility.

This repository publishes release assets built on Ubuntu 20.04 so they can run in
Focal-based devcontainers where newer upstream binaries require a newer glibc.

## Neovim

Release tags are prefixed by tool name, for example `neovim-v0.12.2`.

The Neovim workflow publishes `nvim-linux-x86_64.tar.gz`, containing:

```text
nvim-linux-x86_64/
  bin/
    nvim
```

Mise usage:

```toml
[tools]
"github:ekroon/focal-builds[matching=neovim]" = "latest"
```

## Adding more tools

Add a separate workflow per tool, and prefix release tags with the tool name, for
example `ripgrep-14.1.1` or `fd-10.2.0`. Keep release assets named and packaged
in the layout expected by the consumer.
