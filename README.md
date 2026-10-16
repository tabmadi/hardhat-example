# Hardhat Example

**This example is incomplete.** It holds a [Hardhat](https://hardhat.org) project with the toolchain set up, but no contract or test yet.

## What it shows

Hardhat is a development environment for Ethereum smart contracts. It compiles Solidity, runs tests on a local network, and deploys. The goal of this example is to show that loop with one small contract and its tests.

The repo has the setup that the loop needs:

- `hardhat.config.js` sets the Solidity compiler to `0.8.24`.
- Yarn installs Hardhat with the `node-modules` linker, so editors find the packages.
- `mise run build` compiles the contracts, and `mise run test` runs the tests.

## Run it

1. Install [mise](https://mise.jdx.dev/getting-started.html).
2. Install the tools and dependencies, then compile and test:

   ```bash
   git clone git@github.com:tabmadi/hardhat-example.git
   cd hardhat-example
   mise install
   mise run setup
   mise run build
   mise run test
   ```

With no contract, `build` prints `Nothing to compile`, and `test` finds no test.

## How it works

| File | Holds |
| --- | --- |
| [`hardhat.config.js`](hardhat.config.js) | The Hardhat config: the Solidity version |
| [`package.json`](package.json) | Hardhat as a dev dependency, and the Yarn version |
| [`.yarnrc.yml`](.yarnrc.yml) | The Yarn linker setting |

A contract goes in `contracts/`, and a test goes in `test/`. Hardhat finds both by default.

## What is deliberately missing

- **A contract and its tests**: this is the missing part that makes the example incomplete.
- **Deployment**: no network other than the local Hardhat network.

## Tasks

| Task | Does |
| --- | --- |
| `mise run setup` | Installs the locked dependencies and the git hooks |
| `mise run build` | Compiles the contracts |
| `mise run test` | Runs the contract tests |
| `mise run lint` | Runs `lint:js`, `lint:md`, and `lint:secrets` |
| `mise run format` | Applies every formatter |
| `mise run check` | Runs `lint` and `test`. Run it before you finish a change |
| `mise run ci` | Runs exactly what CI runs. The `pre-push` hook runs it too |

## License

Apache License 2.0. See [LICENSE](LICENSE).
