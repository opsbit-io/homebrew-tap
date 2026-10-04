# homebrew-tap

Homebrew tap for [CTX](https://github.com/opsbit-io/ctx), a native cloud and
Kubernetes context manager for macOS.

```sh
brew install --cask opsbit-io/tap/ctx
```

Upgrading later:

```sh
brew upgrade --cask ctx
```

Coming from the old `eliasaf-abargel/tap`? Run `brew uninstall --cask ctx`, then
install from `opsbit-io/tap` as above. Your settings are kept.

## How the cask stays current

`Casks/ctx.rb` is updated by [`sync-cask.yml`](.github/workflows/sync-cask.yml),
which reads the latest CTX release, hashes the published asset and commits the
result when either the version or the hash has changed. It runs on a schedule
and can be started by hand from the Actions tab; it needs no personal access token.
