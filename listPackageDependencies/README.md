# List npm package dependencies

Given an npm package, return all dependencies the package depends on.

For example, given [`webpack`](https://www.npmjs.com/package/webpack) package that has dependencies [`mkdirp`](https://www.npmjs.com/package/mkdirp), [`@webassemblyjs/ast`](https://www.npmjs.com/package/@webassemblyjs/ast), and many more. 
[`mkdirp`](https://www.npmjs.com/package/mkdirp) depends on [`minimist`](https://www.npmjs.com/package/minimist).
[`@webassemblyjs/ast`](https://www.npmjs.com/package/@webassemblyjs/ast) depends on [`@webassemblyjs/wast-parser`](https://www.npmjs.com/package/@webassemblyjs/wast-parser),  etc.

We would like to get back `mkdirp`, `@webassemblyjs/ast`, `minimist`, `@webassemblyjs/wast-parser`...

```
web-pack
├─┬ mkdirp
│ ├─┬ minimist
│ ├─┬ @webassemblyjs/ast
│ │ ├── @webassemblyjs/helper-module-context
│ │ ├── @webassemblyjs/helper-wasm-bytecode
│ │ └─┬ @webassemblyjs/wast-parser
│ │   ├── @webassemblyjs/ast
│ │   ├── @webassemblyjs/floating-point-hex-parser
│ │   ├── @webassemblyjs/helper-api-error
│ │   ├─┬ @webassemblyjs/helper-code-frame
│ │   │ └── @webassemblyjs/wast-printer
│ │   ├── @webassemblyjs/helper-fsm
│ │   └── @xtuc/long
│ ├── @webassemblyjs/helper-module-context
...
```

