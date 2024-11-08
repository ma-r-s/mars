<script>
	import Toggle from '$lib/Toggle.svelte';
	import { page } from '$app/stores';
	import { Button } from '$lib/components/ui/button/index.js';
	/** @type {{children?: import('svelte').Snippet}} */
	let { children } = $props();

	let pages = ['Miscellaneous', 'Projects', 'Thoughts', 'About'];
	let currPage = $derived($page.url.pathname.split('/')[1]);
</script>

<div class="mb-2 flex items-center justify-between">
	<p class="text-xl font-bold md:text-2xl">{currPage}</p>
	<Toggle></Toggle>
</div>
<div class="mb-6 flex items-center justify-end gap-4">
	{#each pages as pageName}
		<Button
			class={`p-0 text-sm  decoration-primary/50 transition-opacity duration-300 hover:opacity-50 sm:text-base ${currPage === pageName ? 'font-extralight' : 'underline'} `}
			disabled={currPage === pageName}
			href={currPage === pageName ? '' : `/${pageName}`}
			variant="link"
		>
			{pageName}
		</Button>
	{/each}
</div>
{@render children?.()}
