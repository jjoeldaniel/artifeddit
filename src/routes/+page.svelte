<script lang="ts">
	import PostPreview from '$lib/PostPreview.svelte';

	let sample = {
		title: 'AITA?',
		content:
			'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
		author: 'throwaway123'
	};
</script>

<div class="container h-full mx-auto flex justify-center">
	<div class="space-y-5 pt-5 items-center">
		{#each Array(6) as _, i}
			<PostPreview title={sample.title} content={sample.content} author={sample.author} />
		{/each}
	</div>
</div>
