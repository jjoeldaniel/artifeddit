<script lang="ts">
	import PostPreview from '$lib/PostPreview.svelte';

	let sample = {
		title: 'Just finished my first custom PC build!',
		content:
			"I've been wanting to build a PC for a while now, and I finally got all the parts together and put it together last night. It's a Ryzen 5 5600X with an RTX 3080, and I'm absolutely loving it. It's so much faster and more powerful than my old laptop. I'm really happy with how it turned out.",
		author: 'BlushinglyBlue',
		subreddit: 'r/pcgaming'
	};
	let sample2 = {
		title: "What's the best way to learn a new language?",
		content:
			"I just upgraded my PC and I'm looking for some good games to check out. I'm into all sorts of genres, so feel free to recommend anything",
		author: 'SeriousLearner',
		subreddit: 'r/languagelearning'
	};
	let sample3 = {
		title: 'Building my first PC, help me choose parts',
		content:
			"I'm looking to build my first PC for gaming, and I'm not really sure where to start. I have a budget of around $1,000. Can anyone help me choose parts?",
		author: 'honoredcracker',
		subreddit: 'r/buildapc'
	};
	let sample4 = {
		title: "What's the best way to get rid of a headache?",
		content:
			"I've been having a headache for the past few hours and it's really starting to get to me. I've tried taking some ibuprofen but it's not helping much. Does anyone have any other suggestions?",
		author: 'measlyoasis_475',
		subreddit: 'r/askreddit'
	};
	let sample5 = {
		title: "What's your favorite kind of pizza?",
		content:
			"I love pizza! There are so many different kinds, it's hard to choose a favorite. But if I had to pick one, I'd say my favorite is a pepperoni pizza with extra cheese. I love the combination of the salty pepperoni and the gooey cheese. It's the perfect pizza for a lazy night at home.",
		author: 'goofy_maple',
		subreddit: 'r/askreddit'
	};
	let sample6 = {
		title: 'Upgraded my PC, any good games I should check out?',
		content:
			"I just upgraded my PC and I'm looking for some good games to check out. I'm into all sorts of genres, so feel free to recommend anything",
		author: 'PM_ME_YOUR_AESTHETICS',
		subreddit: 'r/pcmasterace'
	};
</script>

<div class="container h-full mx-auto flex justify-center">
	<div class="space-y-5 pt-5 items-center">
		<PostPreview
			title={sample.title}
			content={sample.content}
			author={sample.author}
			subreddit={sample.subreddit}
		/>
		<PostPreview
			title={sample2.title}
			content={sample2.content}
			author={sample2.author}
			subreddit={sample2.subreddit}
		/>
		<PostPreview
			title={sample3.title}
			content={sample3.content}
			author={sample3.author}
			subreddit={sample3.subreddit}
		/>
		<PostPreview
			title={sample4.title}
			content={sample4.content}
			author={sample4.author}
			subreddit={sample4.subreddit}
		/>
		<PostPreview
			title={sample5.title}
			content={sample5.content}
			author={sample5.author}
			subreddit={sample5.subreddit}
		/>
		<PostPreview
			title={sample6.title}
			content={sample6.content}
			author={sample6.author}
			subreddit={sample6.subreddit}
		/>
	</div>
</div>
