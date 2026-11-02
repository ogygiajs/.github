# ogygia

**The missing layer for SvelteKit.**

Your pages go out as plain HTML, and only the parts you mark load any JavaScript. Mark a component
with an import attribute, and it becomes an island that wakes on load, when idle, when visible, or on
first touch. Everything else stays static. ogygia works with SvelteKit as it is, with no patches to
Kit.

```svelte
<script>
	import Cart from './Cart.svelte' with { wake: 'load' };
	import Chart from './Chart.svelte' with { wake: 'visible' };
</script>
```

On top of islands: server islands for the personal bits of a cached page, remote functions and
async Svelte inside islands, an SPA router, cross-island state, content collections, fragment
federation across apps, feature flags decided on the server, and a profiler and devtools that show
what every island costs.

**Docs and guides:** [ogygiajs.dev](https://ogygiajs.dev)

## Repositories

- [**ogygia**](https://github.com/ogygiajs/ogygia): the library, its docs site and its test apps.
- [**benchmarks**](https://github.com/ogygiajs/benchmarks): ogygiaBench, the same blog built in
  ogygia and other frameworks and measured side by side.

## Packages

| Package | What it is |
| --- | --- |
| [`ogygia`](https://www.npmjs.com/package/ogygia) | What an app installs: islands, regions, the router and the Vite plugin |
| [`@ogygia/devtools`](https://www.npmjs.com/package/@ogygia/devtools) | The in-page dock and the SSR profiler |
| [`@ogygia/postrender`](https://www.npmjs.com/package/@ogygia/postrender) | Request-time prerendering: a page that read nothing personal is stored and served as bytes |
| [`@ogygia/content`](https://www.npmjs.com/package/@ogygia/content) | Content collections, markdown with Shiki, docs and blog shells, search |
| [`@ogygia/router`](https://www.npmjs.com/package/@ogygia/router) | The server router: Kit's routing model as values, with a typed client |
| [`@ogygia/federation`](https://www.npmjs.com/package/@ogygia/federation) | Apps sharing pages and widgets as signed regions |
| [`@ogygia/flags`](https://www.npmjs.com/package/@ogygia/flags) | Feature flags and A/B tests, decided on the server, no flag code in the browser |
| [`@ogygia/testing`](https://www.npmjs.com/package/@ogygia/testing) | The devtools and profiler as test primitives for Playwright |
| [`@ogygia/cli`](https://www.npmjs.com/package/@ogygia/cli) | Scaffolds, the AI skill, the MCP server, perf budgets |
| [`@ogygia/core`](https://www.npmjs.com/package/@ogygia/core) | The shared core the others build on |

## Get involved

Questions and ideas are welcome in
[issues](https://github.com/ogygiajs/ogygia/issues). To report a security problem, please use a
[private report](https://github.com/ogygiajs/ogygia/security/advisories/new) instead.

Ogygia is the island in the Odyssey, which is why everything here is named after islands.
