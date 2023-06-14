<script lang="ts">
	// Required Skeleton imports
	import '@skeletonlabs/skeleton/themes/theme-crimson.css';
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	import '../app.postcss';

	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
</script>

<AppShell>
	<svelte:fragment slot="header">
		<AppBar
			gridColumns="grid-cols-3"
			slotDefault="place-content-stretch"
			slotTrail="place-content-end"
			gap="gap-0"
		>
			<svelte:fragment slot="lead"
				><a href="/" class="font-bold text-xl">🧠 <span class="max-sm:hidden">ArtifEddit</span></a
				></svelte:fragment
			>
			<input class="input" title="search" type="text" placeholder="🔍 Search.." />
			<svelte:fragment slot="trail"><LightSwitch /></svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<slot />
</AppShell>
