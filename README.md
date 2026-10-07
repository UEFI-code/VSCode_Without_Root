# VS Code Without Root (on Linux)

The original VS Code website gives you a `deb`.

How the **FUCK** does an editor need root / sudo to install?!

## NO! DON'T GIVE IT ROOT (UNLESS YOU'RE STUPID ENOUGH)

The VS Code maintainers give us a **FUCKING REASON** why they need root:

> `Register an apt repo`

> `Install the Microsoft signing key`

> `Update alternatives`

> `Install a bunch of things into /usr (vscode, bin command, desktop entry)`

https://github.com/microsoft/vscode/issues/25037

THESE REASONS ARE **FUCKING ENOUGH**, AREN'T THEY?!

DON'T GIVE IT ROOT!

I just do this:

```bash
mkdir vscode_deb
dpkg-deb -x code_1.140.0-1790759618_amd64.deb vscode_deb/
vscode_deb/usr/share/code/bin/code
```

**ENOUGH**
