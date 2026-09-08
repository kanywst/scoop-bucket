# scoop-bucket

A [Scoop](https://scoop.sh) bucket for kanywst's tools.

```powershell
scoop bucket add kanywst https://github.com/kanywst/scoop-bucket
scoop install kanywst/y509
```

## Manifests

| Tool | |
| :--- | :--- |
| [y509](https://github.com/kanywst/y509) | TUI for X.509 certificate chains. Verifies trust, and catches the missing intermediates and bad ordering that break curl but not browsers. |

Manifests carry `checkver` and `autoupdate`, so a new upstream release is picked
up without editing the URL and hash by hand.
