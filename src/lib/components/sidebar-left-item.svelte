<script lang="ts">
	import LucideIcon from './lucide-icon.svelte';
	interface Item {
		title: string;
		url: string;
		icon?: string;
		latest?: boolean;
	}

	export let item: Item = {
		title: 'Sidebar Item',
		url: '/',
		icon: '',
		latest: false
	};
	export let active: boolean = false;
</script>

<a
	href={item.url}
	class={`flex w-fit items-center gap-3 rounded-full py-2.5 pl-3 pr-4 text-xl hover:bg-zinc-800 ${active ? 'font-bold' : ''}`}
>
	<div class="relative">
		<div class="flex h-8 w-8 items-center justify-center rounded-2xl">
			{#if item.icon}
				<LucideIcon name={item.icon} size={26} />
			{/if}
		</div>
		{#if item.latest}
			<span class="absolute right-0 top-0 h-2 w-2 rounded-full bg-blue-500"></span>
		{/if}
	</div>
	{item.title}
</a>
