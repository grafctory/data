# @grafctory/data-store

[![npm][npm-badge]][npm] [![Grafctory][grafctory-badge]][grafctory]

[npm-badge]: https://img.shields.io/npm/v/@grafctory/data-store
[npm]: https://www.npmjs.com/package/@grafctory/data-store
[grafctory-badge]: https://img.shields.io/badge/part%20of-Grafctory-blue
[grafctory]: https://github.com/grafctory

Store processing tasks for [@grafctory/data].

Provides ready-made [@grafctory/flow] steps for working with [@grafctory/keep] stores in pipelines run by the
[@grafctory/gear] job executor.

[@grafctory/data]: https://github.com/grafctory/data
[@grafctory/flow]: https://github.com/grafctory/flow
[@grafctory/keep]: https://github.com/grafctory/keep
[@grafctory/gear]: https://github.com/grafctory/gear

# Installation

```shell
npm install @grafctory/gear                       # the job executor
npm install @grafctory/data-store                 # this package
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

[lookup]: https://grafctory.github.io/data/functions/_grafctory_data-store.lookup.html

[retire]: https://grafctory.github.io/data/functions/_grafctory_data-store.retire.html

[settle]: https://grafctory.github.io/data/functions/_grafctory_data-store.settle.html

[createStore]: https://grafctory.github.io/data/functions/_grafctory_data-store.createStore.html

The store service has no default: a job binds a store connector to [`createStore()`][createStore] once, and every task
or sink in the execution then reads from or writes to the store that connector reaches.

# Support

- open an [issue](https://github.com/grafctory/data/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/data/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/data?tab=Apache-2.0-1-ov-file) file for details.

<sub>Grafctory™ is a trademark of Metreeca srl.</sub>
