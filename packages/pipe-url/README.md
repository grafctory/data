# @grafctory/pipe-url

[![npm](https://img.shields.io/npm/v/@grafctory/pipe-url)](https://www.npmjs.com/package/@grafctory/pipe-url)

URL processing tasks for [@grafctory/pipe](https://github.com/grafctory/pipe).

Provides ready-made [@grafctory/flow](https://github.com/grafctory/flow) steps for working with resources identified by
URLs in pipelines run by the [@grafctory/gear](https://github.com/grafctory/gear) job executor.

# Installation

```shell
npm install @grafctory/gear      # the job executor
npm install @grafctory/pipe-url  # this package
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

[fetch]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-url.fetch.html

[crawl]: https://grafctory.github.io/pipe/functions/_grafctory_pipe-url.crawl.html

# Support

- open an [issue](https://github.com/grafctory/pipe/issues) to report a problem or to suggest a new feature
- start a [discussion](https://github.com/grafctory/pipe/discussions) to ask a how-to question or to share an idea

# License

This project is licensed under the Apache 2.0 License –
see [LICENSE](https://github.com/grafctory/pipe?tab=Apache-2.0-1-ov-file) file for details.
