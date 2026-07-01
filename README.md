PenguinMod/PenguinMod-Vm
Modified Scratch VM with a JIT compiler and more features.

This is a drop-in replacement for LLK/scratch-vm.

Setup
See https://github.com/TurboWarp/scratch-gui/wiki/Getting-Started to setup the complete TurboWarp environment.

If you just want to play with the VM then it's the same process as upstream scratch-vm.

Run the local web UI with:

```bash
NODE_OPTIONS=--openssl-legacy-provider npm start -- --host 0.0.0.0 --open false
```

Then open `http://localhost:8073/` in your browser.

To publish the playground to GitHub Pages, build and deploy the `playground` folder:

```bash
npm run deploy:gh-pages
```

This requires the repository to have a valid GitHub remote and branch permissions.


Extension authors
If you only use the standard reporter, boolean, and command block types, everything should just work without any changes.

Compiler Overview
For a high-level overview of how the compiler works, see https://docs.turbowarp.org/how

For more technical information, read the code in src/compiler.

Public API
This section was too out of date to be useful. We hope to re-add it as some point.

e
