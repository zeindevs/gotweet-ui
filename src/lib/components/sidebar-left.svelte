<script lang="ts">
	import { page } from '$app/stores';
	import SidebarLeftItem from './sidebar-left-item.svelte';

	let sidebars = [
		{
			title: 'Home',
			icon: 'House',
			url: '/',
			latest: true
		},
		{
			title: 'Explore',
			icon: 'Search',
			url: '/explore'
		},
		{
			title: 'Notifications',
			icon: 'Bell',
			url: '/notifications'
		},
		{
			title: 'Messages',
			icon: 'Mail',
			url: '/messages'
		},
		{
			title: 'Grok',
			icon: 'SquareSlash',
			url: '/grok'
		},
		{
			title: 'Communities',
			icon: 'Users',
			url: '/communities'
		},
		{
			title: 'Profile',
			icon: 'User',
			url: '/profile'
		},
		{
			title: 'More',
			icon: 'Ellipsis',
			url: '#more'
		}
	];

	$: pathname = $page.url.pathname;
</script>

<aside class="flex max-w-xs flex-1 flex-col border-r border-zinc-800 bg-zinc-950 py-4 text-white">
	<div class="px-4">
		<a href="/" class="flex w-fit rounded-full p-1.5 text-4xl font-bold hover:bg-zinc-900">
			<img src="twitter.svg" class="h-10" alt="GoTweet" />
		</a>
	</div>
	<ul class="flex-1 px-4 py-4">
		{#each sidebars as sidebar}
			<SidebarLeftItem item={sidebar} active={pathname === sidebar.url} />
		{/each}
	</ul>
	<ul class="px-4">
		<li>
			<button class="flex w-full items-center gap-3 rounded-full py-2 pl-3 pr-4 hover:bg-zinc-900">
				<div class="h-10 w-10 overflow-hidden rounded-full bg-zinc-700">
					<img src="https://i.pravatar.cc/150?img=3" class="h-full w-full" alt="ZEN" />
				</div>
				<div class="flex flex-col text-left">
					<p class="font-medium">ZEN</p>
					<span class="text-muted-foreground text-[15px]">@zen</span>
				</div>
			</button>
		</li>
	</ul>
</aside>
