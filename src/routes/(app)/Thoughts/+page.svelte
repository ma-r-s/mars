<script>
	import { entries } from './entries.js';
</script>

{#each entries as { link, title, date }}
	<a href={`/Thoughts/${link}`} class="mb-4 flex justify-between">
		<p>{title}</p>
		<p class="text-sm opacity-70">{date}</p>
	</a>
{/each}
