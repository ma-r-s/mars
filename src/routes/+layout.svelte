<script>
	import '../app.pcss';
	import { ModeWatcher } from 'mode-watcher';
	import { Separator } from '$lib/components/ui/separator/index.js';
	import Button from '$lib/components/ui/button/button.svelte';
</script>

<ModeWatcher />
<div class="mx-auto w-full max-w-2xl p-4 pb-16 pt-6 sm:pb-32 sm:pt-16">
	<slot />
	<Separator class="my-12" />
	<div class="flex gap-2">
		<Button
			href="https://github.com/ma-r-s"
			variant="link"
			class="p-0 text-sm font-extralight underline decoration-primary/50"
		>
			Github
		</Button>.
		<Button
			href="https://www.instagram.com/mars.mars._/"
			variant="link"
			class="p-0 text-sm font-extralight underline decoration-primary/50"
		>
			Instagram
		</Button>.
		<Button
			href="mailto:reachmarss@gmail.com"
			variant="link"
			class="p-0 text-sm font-extralight underline decoration-primary/50"
		>
			reachmarss@gmail.com
		</Button>
	</div>
	<div class="mt-20 flex items-center justify-between">
		<p class="text-sm opacity-50">CC BY-NC 4.0 2024 © ma-r-s</p>
		<Button
			href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
			variant="link"
			class="p-0 text-xs font-extralight">?</Button
		>
	</div>
</div>
