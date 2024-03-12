<script>
	let posts = [
		{
			title: 'A lost bear',
			link: 'lost-bear',
			date: '2024-03-11'
		},
		{
			title: 'Alphageometry',
			link: 'alphageometry',
			date: '2021-10-11'
		}
	];
</script>

{#each posts as { link, title, date }}
	<a href={`/Thoughts/${link}`} class="mb-4 flex justify-between">
		<p>{title}</p>
		<p class="text-primary/50">{date}</p>
	</a>
{/each}
