# tool7/homebrew-tap

A personal [Homebrew](https://brew.sh) tap shipping pre-built binaries for tools maintained by [@tool7](https://github.com/tool7).

## Available casks

| Cask | Description | Source |
| --- | --- | --- |
| `scout` | Local CLI for querying Git history, Jira tickets, and source code from configured projects. | [tool7/scout](https://github.com/tool7/scout) |

## Installation

> [!IMPORTANT]
> **Always use the fully-qualified name `tool7/tap/<cask>`.**
> The short form `brew install <cask>` resolves against *all* taps Homebrew knows about, and short names like `scout` collide with unrelated casks in `homebrew/cask`. Using the qualified name guarantees Homebrew installs the binary from this tap.

```sh
brew install tool7/tap/scout
```

That single command tap-and-installs in one step — no separate `brew tap` needed.

## Upgrade

```sh
brew upgrade tool7/tap/scout
```

Or upgrade everything at once: `brew upgrade`.

## Uninstall

```sh
brew uninstall --cask tool7/tap/scout
```

To also remove the tap itself:

```sh
brew untap tool7/tap
```

## Verify the install

After `brew install tool7/tap/scout`, confirm you got the right binary:

```sh
scout --version
```

Expected output (the commit SHA and build date will differ):

```
scout 0.1.0
commit: <full sha>
built:  2026-04-29T16:00:00Z
```

If `scout --version` prints something else, you almost certainly installed a different `scout` package. Uninstall it and re-run the qualified-name command above.

## How this tap is maintained

Casks here are auto-generated and committed by [GoReleaser](https://goreleaser.com) on every tagged release of the upstream project — they are **not** hand-edited. Pull requests changing files under `Casks/` will be overwritten on the next release; please open issues against the upstream project instead.
