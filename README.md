# lerna-experiment

Based on [lerna v4.0.0](https://github.com/lerna/lerna/blob/6cb8ab2d4af7ce25c812e8fb05cd04650105705f/README.md)

---

## `lerna add <package> [globs...]`

Add a single dependency to matched globs of lerna packages

| Example                                    | Description                                                                  |
| ------------------------------------------ | ---------------------------------------------------------------------------- |
| `lerna add module1 packages/prefix-\* `    | Adds the `module1` package to the packages in the 'prefix-' prefixed folders |
| `lerna add module1 --scope=module2`        | Install `module1` to `module2`                                               |
| `lerna add module1 --scope=module2 --dev`  | Install `module1` to `module2` in devDependencies                            |
| `lerna add module1 --scope=module2 --peer` | Install `module1` to `module2` in peerDependencies                           |
| `lerna add module1`                        | Install `module1` in all modules except module1                              |
| `lerna add module1 --no-bootstrap`         | Skip automatic `lerna bootstrap`                                             |

---

## `lerna bootstrap`

Link local packages together and install remaining package dependencies

Notable options:

| Option    | Description                                                                                                                                                                                      |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `--hoist` | Install external dependencies matching `[glob]` (Default: `'**'`) to the repo root. Read more [here](https://github.com/lerna/lerna/blob/6cb8ab2d4af7ce25c812e8fb05cd04650105705f/doc/hoist.md). |

---

## `lerna clean`

Remove the `node_modules` directory from all packages.

---

## `lerna exec [cmd] [args...]`

Execute an arbitrary command in each package.

For example, the command below will run `ls -al` on each lerna package.

```shell
lerna exec -- ls -al
```
