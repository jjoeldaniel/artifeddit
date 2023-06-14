<script lang="ts">
	import { Avatar } from '@skeletonlabs/skeleton';
	export let title: string = 'Title';
	export let author: string = 'Author';
	export let content: string = 'Content';
</script>

<div
	class="block max-w-5xl rounded-lg p-6 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)]"
>
	<div>
		<p>hi</p>
	</div>
	<div>
		<h5 class="mb-2 text-xl font-semibold leading-tight text-neutral-800 dark:text-neutral-50">
			{title}
		</h5>
		<p class="mb-4 text-base text-neutral-600 dark:text-neutral-200 line-clamp-2">
			{content}
		</p>
		<p class="text-xs">
			Posted by {author}
		</p>
	</div>
</div>
