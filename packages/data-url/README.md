# @grafctory/data-url

[![npm][npm-badge]][npm] [![Grafctory][grafctory-badge]][grafctory]

[npm-badge]: https://img.shields.io/npm/v/@grafctory/data-url
[npm]: https://www.npmjs.com/package/@grafctory/data-url
[grafctory-badge]: https://img.shields.io/badge/part%20of-Grafctory-blue
[grafctory]: https://github.com/grafctory

URL processing tasks for [@grafctory/data].

Provides ready-made [@grafctory/flow] steps for working with resources identified by URLs in pipelines run by the
[@grafctory/gear] job executor.

[@grafctory/data]: https://github.com/grafctory/data
[@grafctory/flow]: https://github.com/grafctory/flow
[@grafctory/gear]: https://github.com/grafctory/gear

# Installation

```shell
npm install @grafctory/gear      # the job executor
npm install @grafctory/data-url  # this package
```

> [!IMPORTANT]
>
> Node.js 22 or later is required.

> [!WARNING]
>
> TypeScript consumers must use `"moduleResolution": "nodenext"/"node16"/"bundler"` in `tsconfig.json`.
> The legacy `"node"` resolver is not supported.

# Usage

| Task               | Description                    |
|--------------------|--------------------------------|
| [`fetch()`][fetch] | Resource fetcher               |
| [`crawl()`][crawl] | URL graph walker and harvester |

[fetch]: https://grafctory.github.io/data/functions/_grafctory_data-url.fetch.html

[crawl]: https://grafctory.github.io/data/functions/_grafctory_data-url.crawl.html

# Support

- open an [issue](https://github.com/grafctory/data/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/data/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/data?tab=Apache-2.0-1-ov-file) file for details.

<sub>Grafctory™ is a trademark of Metreeca srl.</sub>
