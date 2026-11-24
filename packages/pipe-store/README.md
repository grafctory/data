# @grafctory/pipe-store

[![npm](https://img.shields.io/npm/v/@grafctory/pipe-store)](https://www.npmjs.com/package/@grafctory/pipe-store)

Store processing tasks for [@grafctory/pipe](https://github.com/grafctory/pipe).

Provides ready-made [@grafctory/flow](https://github.com/grafctory/flow) steps for working with
[@grafctory/keep](https://github.com/grafctory/keep) stores in pipelines run by the
[@grafctory/gear](https://github.com/grafctory/gear) job executor.

# Installation

```shell
npm install @grafctory/gear                       # the job executor
npm install @grafctory/pipe-store                 # this package
npm install @grafctory/keep-<connector>           # store connector for the target backend
```

> [!IMPORTANT]
>
> Node.js 22 or later is required.

> [!WARNING]
>
> TypeScript consumers must use `"moduleResolution": "nodenext"/"node16"/"bundler"` in `tsconfig.json`.
> The legacy `"node"` resolver is not supported.

# Usage

| Task                 | Description               |
|----------------------|---------------------------|
| [`lookup()`][lookup] | Store resource retriever  |
| [`retire()`][retire] | Retired resource selector |
| [`settle()`][settle] | Resource delta writer     |

[lookup]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-store.lookup.html

[retire]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-store.retire.html

[settle]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-store.settle.html

[createStore]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-store.createStore.html

The store service has no default: a job binds a store connector to [`createStore()`][createStore] once, and every task
or sink in the execution then reads from or writes to the store that connector reaches.

# Support

- open an [issue](https://github.com/grafctory/pipe/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/pipe/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/pipe?tab=Apache-2.0-1-ov-file) file for details.
