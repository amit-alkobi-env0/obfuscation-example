# Obfuscation example

Illustrates how the code obfuscation and the errors stack traces

### Steps
1. run `pnpm install`
2. run `pnpm run build`
3. run `node -r source-map-support/register ./dist/main.js`

### Expected error trace
```
Error: This is an error from func1
    at func1 (/Users/amitalkobi/src/playground/obfuscation/obfuscation-example/dist/webpack:/my-webpack-project/src/pack1/module1.ts:2:11)
    at /Users/amitalkobi/src/playground/obfuscation/obfuscation-example/dist/webpack:/my-webpack-project/src/index.ts:3:1
    at Object.<anonymous> (/Users/amitalkobi/src/playground/obfuscation/obfuscation-example/dist/main.js:1:118)
    at Module._compile (node:internal/modules/cjs/loader:1101:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1153:10)
    at Module.load (node:internal/modules/cjs/loader:981:32)
    at Function.Module._load (node:internal/modules/cjs/loader:822:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:79:12)
    at node:internal/main/run_main_module:17:47

```