# @grafctory/data

Ready-made tasks for reading and writing data in external sources.

**@grafctory/data** is the data access module of the [Grafctory][grafctory] model-driven knowledge graph framework. It
provides ready-made [@grafctory/flow] tasks that read records from web resources, object stores and databases. Matching
tasks write pipeline results back to the same sources. All tasks run under the [@grafctory/gear] job executor, which
supplies the clients, credentials and connection pools each source requires and releases them after the run.

- **Read and Write**: both directions of access to a source, in tasks that chain with any other task
- **Shared Services**: clients, credentials and connection pools, built on demand and released after the run
- **Custom Bindings**: a stubbed, throttled or recorded source swapped in for a run, leaving the job untouched
- **Minimal Footprint**: one package per source family, each pulling in only the drivers that family needs

> [!IMPORTANT]
>
> Pipelines are server-side workloads targeting [Node.js](https://nodejs.org/) 22 or later, relying on facilities such
> as the filesystem, the process environment and `fetch`. The packages are not intended for the browser.

[@grafctory/flow]: https://github.com/grafctory/flow
[@grafctory/gear]: https://github.com/grafctory/gear
[grafctory]: https://github.com/grafctory

# Installation

```shell
npm install @grafctory/gear            # job executor and shared services
npm install @grafctory/data-<source>   # task package, one per source family
```

> [!WARNING]
>
> TypeScript consumers must use `"moduleResolution": "nodenext"/"node16"/"bundler"` in `tsconfig.json`.
> The legacy `"node"` resolver is not supported.

Add a task package for each source family the pipeline reads from or writes to. Each package is self-contained and
pulls in only the drivers its own family needs. The task packages bring in [@grafctory/gear] transitively. Install it
directly anyway, since every job is configured, bound to its sources and run through its executor.

| Package                 | Description             |
|-------------------------|-------------------------|
| [@grafctory/data-url]    | URL processing tasks    |
| [@grafctory/data-store]  | Store processing tasks  |
| [@grafctory/data-sparql] | SPARQL processing tasks |

[@grafctory/data-url]: https://grafctory.github.io/data/modules/_grafctory_data-url.html

[@grafctory/data-store]: https://grafctory.github.io/data/modules/_grafctory_data-store.html

[@grafctory/data-sparql]: https://grafctory.github.io/data/modules/_grafctory_data-sparql.html

# Usage

> [!NOTE]
>
> Each package documents its own API in its README and API reference; for complete coverage, see the
> [API reference](https://grafctory.github.io/data/).

# Support

- open an [issue](https://github.com/grafctory/data/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/data/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/data?tab=Apache-2.0-1-ov-file) file for details.

<sub>Grafctory™ is a trademark of Metreeca srl.</sub>
