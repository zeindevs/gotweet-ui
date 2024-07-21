<script lang="ts">
	import SidebarLeft from '$lib/components/sidebar-left.svelte';
	import SidebarRight from '$lib/components/sidebar-right.svelte';
	import Tweet from '$lib/components/tweet.svelte';
	import TweetForm from '$lib/components/tweet-form.svelte';

	let post: string = '';
	let active = 'foryou';
</script>

<svelte:head>
	<title>GoTweet</title>
</svelte:head>

<div class="mx-auto flex h-screen max-w-7xl overflow-hidden bg-zinc-950 text-white">
	<SidebarLeft />

	<main class="flex-1 overflow-auto">
		<div class="grid grid-cols-2 divide-x divide-zinc-800 border-b border-zinc-800">
			<button
				class="relative px-5 py-3.5 font-medium hover:bg-zinc-900"
				on:click={() => (active = 'foryou')}
			>
				{#if active === 'foryou'}
					<span class="absolute bottom-0 left-0 right-0 mx-auto h-1 w-[15%] rounded bg-blue-500"
					></span>
				{/if}
				For you
			</button>
			<button
				class="relative px-5 py-3.5 font-medium hover:bg-zinc-900"
				on:click={() => (active = 'following')}
			>
				{#if active === 'following'}
					<span class="absolute bottom-0 left-0 right-0 mx-auto h-1 w-[15%] rounded bg-blue-500"
					></span>
				{/if}
				Following
			</button>
		</div>

		<TweetForm {post} />

		<div class="border-b border-zinc-800">
			<button class="w-full px-4 py-3 text-blue-500 hover:bg-zinc-900/50">Show 498 posts</button>
		</div>
		<div>
			{#each Array(5) as _}
				<Tweet
					name="ZEN"
					username="zen"
					tweet={'Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde in repellendus, dolore neque maxime dolorem expedita sequi pariatur, eos maiores nam quis minima provident, aspernatur beatae temporibus? Tempora, voluptates veritatis.'}
				/>
			{/each}
		</div>
	</main>

	<SidebarRight />
</div>
