<script lang="ts">
	import './layout.css';
	import { resolve } from '$app/paths';

	const { children } = $props();
	import { CalendarIcon, CircleUserIcon, MenuIcon, SearchIcon } from '@lucide/svelte';

	import { AppBar } from '@skeletonlabs/skeleton-svelte';
</script>


<AppBar>
	<AppBar.Toolbar class="grid-cols-[1fr_2fr_1fr]">
		<AppBar.Lead>
		</AppBar.Lead>
		<AppBar.Headline class="flex justify-center">
			<h1 class="h1"><a href={resolve("/devblog")}> dev blog till ett spel utan namn </a></h1>
		</AppBar.Headline>
		<AppBar.Trail class="justify-end">
			<a href={resolve("/")} class="btn-icon hover:preset-tonal"><CircleUserIcon class="size-6" /></a>
		</AppBar.Trail>
	</AppBar.Toolbar>
</AppBar>


{@render children()}
