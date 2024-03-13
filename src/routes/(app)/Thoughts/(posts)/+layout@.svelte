<script>
	import { page } from '$app/stores';
	$: currPage = $page.url.pathname.split('/')[2];
	import Button from '$lib/components/ui/button/button.svelte';
	import { entries } from '../entries.js';
	$: entry = entries.find((entry) => entry.link === currPage);
</script>

<p class="text-2xl font-bold md:text-3xl">{entry.title}</p>
<div class="mb-12 flex items-center justify-between">
	<p class="opacity-50">{entry.date}</p>
	<Button
		class="p-0 text-sm underline decoration-primary/50 sm:text-base"
		href="/Thoughts"
		variant="link"
	>
		Back
	</Button>
</div>
<div class="prose max-w-none dark:prose-invert">
	<slot />
</div>
