# modulestf Homebrew tap

Homebrew formulae of [modulestf](https://modules.tf).

```sh
brew install modulestf/tap/mtf-facts
```

| Formula | What it is |
|---------|------------|
| `mtf-facts` | [modulestf/facts](https://github.com/modulestf/facts): an offline CLI that reports deterministic facts about Terraform module trees. A pull request review by the [modulestf skills](https://github.com/modulestf/modulestf) needs it. |

Update with `brew upgrade mtf-facts`.

## How the formula is updated

The formula installs the release binary for your platform (macOS or Linux, arm64 or amd64) and pins its SHA-256 from the release's `SHA256SUMS`. [scripts/update-formula.sh](scripts/update-formula.sh) renders it. Before it pins a binary, it checks with `gh attestation verify` that the facts release workflow built that binary from the release tag.

The `update-formula` workflow runs the script daily, by hand, and when a facts release asks for it, and commits only a changed formula. Do not edit `Formula/mtf-facts.rb` by hand.

## License

Apache-2.0
