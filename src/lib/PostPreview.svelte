<script lang="ts">
	import { Avatar } from '@skeletonlabs/skeleton';
	export let title: string = 'Title';
	export let author: string = 'Author';
	export let content: string = 'Content';
	export let subreddit: string = 'Subreddit';

	export let upvote = false;
	export let downvote = false;
	export let voteCount = 0;

	function vote(event) {
		const target = event.target;
		if (target.classList.contains('upvote')) {
			upvote = !upvote;

			// switching case from downvote to upvote
			if (downvote) {
				target.style.color = 'green';
				target.nextElementSibling.style.color = 'inherit';
				voteCount += 2;
				downvote = !downvote;
				return;
			}

			downvote = false;

			if (upvote) {
				target.style.color = 'green';
				target.nextElementSibling.style.color = 'inherit';
				voteCount++;
			} else {
				target.style.color = 'inherit';
				voteCount--;
			}
		} else {
			downvote = !downvote;

			// switching case from upvote to downvote
			if (upvote) {
				target.style.color = 'red';
				target.previousElementSibling.style.color = 'inherit';
				voteCount -= 2;
				upvote = !upvote;
				return;
			}

			upvote = false;

			if (downvote) {
				target.style.color = 'red';
				target.previousElementSibling.style.color = 'inherit';
				voteCount--;
			} else {
				target.style.color = 'inherit';
				voteCount++;
			}
		}
	}
</script>

<link
	rel="stylesheet"
	href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
/>

<div
	class="flex max-w-5xl pl-0 text-sm rounded-lg p-6 shadow-[0_2px_15px_-3px_rgba(0,0,0,0.07),0_10px_20px_-2px_rgba(0,0,0,0.04)]"
>
	<div class="flex-auto pl-4 pr-4">
		<div class="text-center flex flex-col max-sm:hidden">
			<button on:click={vote} class="material-symbols-outlined upvote"> expand_less </button>
			{voteCount}
			<button on:click={vote} class="material-symbols-outlined downvote"> expand_more </button>
		</div>
	</div>
	<div class="flex-auto">
		<h5 class="mb-2 text-xl font-semibold leading-tight text-neutral-800 dark:text-neutral-50">
			{title}
		</h5>
		<p class="mb-4 text-base text-neutral-600 dark:text-neutral-200 line-clamp-3">
			{content}
		</p>
		<div class="flex place-content-between max-sm:hidden">
			<p>{subreddit}</p>
			<p>
				Posted by u/{author}
			</p>
		</div>
		<div class="flex place-content-between sm:hidden">
			<div class="text-center flex">
				<button on:click={vote} class="material-symbols-outlined upvote"> expand_less </button>
				{voteCount}
				<button on:click={vote} class="material-symbols-outlined downvote"> expand_more </button>
			</div>
			<p>
				{subreddit}
			</p>
		</div>
	</div>
</div>

<style>
	.material-symbols-outlined {
		font-variation-settings: 'FILL' 0, 'wght' 600, 'GRAD' 0, 'opsz' 48;
	}
</style>
