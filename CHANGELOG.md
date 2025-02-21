## v0.1.17

- fixed a regression where `dum <bin>` stopped working

## v0.1.16

- Resolve `-c <dir>` to absolute path, previously it always searches package.json from current directory even if `-c` contains `../`.
- Allow flags in `install` `uninstall` `add` commands.

## v0.1.15

- Forward args to `install` `uninstall` and `add` commands

## v0.1.14

- Commands like `install` `uninstall` `add` are now handled before npm scripts, previously if there're no scripts or no package.json the command will not be executed.
- Properly restore cursor after `ctrl-c`.

## v0.1.13

- Ability to select npm scripts interactively, with `-i, --interactive` flag

## v0.1.12

- Properly concat `$PATH` on Windows. [#24](https://github.com/egoist/dum/issues/24)

## v0.1.11

- Resolve `node_modules/.bin` in parent directories too

## v0.1.10

- Fallback to run binaries in `node_modules/.bin/` when specified script doesn't exist in `package.json`.
- Available via Homebrew `brew install egoist/tap/dum`

## v0.1.9

- Add `remove` command, mirrors `npm remove` `yarn remove` and `pnpm remove`.
- Add `-c <dir>` flag to change working directory.

## v0.1.8

### Fixes

- Fetch `PATH` env at runtime.

## v0.1.7

- Add command `add`

## v0.1.6

- Forward args to `install` command.

## v0.1.5

- Alias script `t` to `test`, so `dum t` and `dum test` are equivalent.
- Add `install` command to automatically run `npm i`, `yarn` or `pnpm i` depending on the project.
