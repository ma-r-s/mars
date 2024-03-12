<script>
	import '../app.pcss';
	import { ModeWatcher } from 'mode-watcher';
	import Toggle from '$lib/Toggle.svelte';
	import { page } from '$app/stores';
	import Button from '$lib/components/ui/button/button.svelte';

	let pages = ['Blog', 'Projects', 'Thoughts', 'About'];
	$: currPage = $page.url.pathname.split('/')[1];
</script>

<ModeWatcher />

<div class="container max-w-2xl pb-16 pt-8 sm:pb-32 sm:pt-20">
	<div class="mb-2 flex items-center justify-between">
		<p class="text-2xl font-bold md:text-3xl">{currPage}</p>
		<Toggle></Toggle>
	</div>
	<div class="mb-8 flex items-center justify-end">
		{#each pages as pageName}
			<Button
				disabled={currPage === pageName}
				href={currPage === pageName ? '' : pageName}
				variant="link"
			>
				{pageName}
			</Button>
		{/each}
	</div>
	<slot />
</div>
