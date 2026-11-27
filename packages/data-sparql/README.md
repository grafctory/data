# @grafctory/data-sparql

[![npm][npm-badge]][npm] [![Grafctory][grafctory-badge]][grafctory]

[npm-badge]: https://img.shields.io/npm/v/@grafctory/data-sparql
[npm]: https://www.npmjs.com/package/@grafctory/data-sparql
[grafctory-badge]: https://img.shields.io/badge/part%20of-Grafctory-blue
[grafctory]: https://github.com/grafctory

SPARQL processing tasks for [@grafctory/data].

Provides ready-made [@grafctory/flow] steps for working with SPARQL repositories in
pipelines run by the [@grafctory/gear] job executor.

[@grafctory/data]: https://github.com/grafctory/data
[@grafctory/flow]: https://github.com/grafctory/flow
[@grafctory/gear]: https://github.com/grafctory/gear
[@grafctory/wire-sparql]: https://grafctory.github.io/wire/modules/_grafctory_wire-sparql.html

# Installation

```shell
npm install @grafctory/gear                       # the job executor
npm install @grafctory/data-sparql                # this package
npm install @grafctory/wire-sparql-<backend>      # repository connector for the target engine
```

> [!IMPORTANT]
>
> Node.js 22 or later is required.

> [!WARNING]
>
> TypeScript consumers must use `"moduleResolution": "nodenext"/"node16"/"bundler"` in `tsconfig.json`.
> The legacy `"node"` resolver is not supported.

Repositories are reached through the backend connectors listed by [@grafctory/wire-sparql]: install the one for the
engine the pipeline targets, together with any peer dependency that the connector itself requires.

# Usage

| Task                       | Description                     |
|----------------------------|---------------------------------|
| [`select()`][select]       | SPARQL `SELECT` query runner    |
| [`construct()`][construct] | SPARQL `CONSTRUCT` query runner |
| [`update()`][update]       | SPARQL Update request runner    |
| [`upload()`][upload]       | RDF graph uploader              |

[select]: https://grafctory.github.io/data/functions/_grafctory_data-sparql.select.html

[construct]: https://grafctory.github.io/data/functions/_grafctory_data-sparql.construct.html

[update]: https://grafctory.github.io/data/functions/_grafctory_data-sparql.update.html

[upload]: https://grafctory.github.io/data/functions/_grafctory_data-sparql.upload.html

[createRepository]: https://grafctory.github.io/data/functions/_grafctory_data-sparql.createRepository.html

The repository service has no default: a job binds a repository connector to [`createRepository()`][createRepository]
once, and every task or sink given no repository of its own then reads from or writes to the repository it reaches.

# Support

- open an [issue](https://github.com/grafctory/data/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/data/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/data?tab=Apache-2.0-1-ov-file) file for details.

<sub>Grafctory™ is a trademark of Metreeca srl.</sub>
