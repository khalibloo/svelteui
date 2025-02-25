---
title: 'use-debounce'
group: 'svelteuidev-composables'
packageGroup: '@svelteuidev/composables'
slug: /composables/use-debounce/
description: 'Get a function that debounces its execution.'
importCode: "import { useDebounce } from '@svelteuidev/composables';"
docs: 'composables/use-debounce'
source: 'svelteui-composables/src/utilities/use-debounce/use-debounce.ts'
---

<script lang='ts'>
    import { Demo, ComposableDemos } from '@svelteuidev/demos';
	import { Heading } from "$lib/components";
    import { base } from '$app/paths';
</script>

<svelte:head>

  <title>{title} - SvelteUI</title>
</svelte:head>

<Heading {title} {group} {packageGroup} {slug} {description} {importCode} {docs} {source} />

## Usage

<Demo demo={ComposableDemos.useDebounceDemo.usage} />

## Params

| Param    | Description                                            |
| -------- | ------------------------------------------------------ |
| fn       | A function to be executed after delay milliseconds.    |
| ms       | A zero-or-greater delay in milliseconds.               |
| trailing | If true, call fn again after the time is up.           |
| leading  | If true, call fn on the leading edge of the ms timeout |

## Definition

```js
export function useDebounce<T extends FunctionArgs>(
	fn: T,
	ms?: number,
	trailing?: boolean,
	leading?: boolean
): T;
```
