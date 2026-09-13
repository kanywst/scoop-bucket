# scoop-bucket

A [Scoop](https://scoop.sh) bucket for kanywst's tools.

```powershell
scoop bucket add kanywst https://github.com/kanywst/scoop-bucket
scoop install kanywst/y509
```

## Manifests

| Tool | |
| :--- | :--- |
| [rapg](https://github.com/kanywst/rapg) | Local-first secret manager for the AI-agent era. Keeps API keys out of `.env` files and out of your agent transcripts. |
| [y509](https://github.com/kanywst/y509) | TUI for X.509 certificate chains. Verifies trust, and catches the missing intermediates and bad ordering that break curl but not browsers. |

## How this stays current

`Excavator` runs every four hours, follows each manifest's `checkver` and
`autoupdate`, and commits a new version when upstream publishes one. It
computes the hash from the archive it downloads, so no hash is ever copied by
hand. `CI` runs the Scoop bucket test suite, including `bin/checkhashes.ps1`,
on every push.
