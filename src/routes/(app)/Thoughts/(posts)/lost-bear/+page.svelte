<script>
	import { Canvas } from '@threlte/core';
	import Scene from './Scene.svelte';
</script>

<figure>
	<blockquote>
		“She generally gave herself very good advice,(though she very seldom followed it).”
	</blockquote>
	<figcaption class="text-sm text-neutral-600">
		― Lewis Carroll, Alice’s Adventures in Wonderland
	</figcaption>
</figure>
<p>
	In the world of design, simplicity often holds the key to understanding. Consider a bear's
	journey: it walks one kilometer south, then one kilometer east, and finally one kilometer north,
	only to end up where it started.
</p>
<div class="aspect-video overflow-hidden rounded-3xl border-2">
	<Canvas>
		<Scene />
	</Canvas>
</div>
