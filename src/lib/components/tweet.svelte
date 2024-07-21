<script lang="ts">
	import Ellipsis from 'lucide-svelte/icons/ellipsis';

	export let avatar = 'https://i.pravatar.cc/150?img=3';
	export let name = 'Name';
	export let username = 'username';
	export let date = 'Dec 12';
	export let tweet =
		'Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde in repellendus, dolore neque maxime dolorem expedita sequi pariatur, eos maiores nam quis minima provident, aspernatur beatae temporibus? Tempora, voluptates veritatis.';
</script>

<div class="flex gap-3 border-b border-zinc-800 p-4 hover:bg-zinc-900/50">
	<div class="h-10 w-10 overflow-hidden rounded-full bg-zinc-700">
		<img src={avatar} class="h-full w-full" alt={username} />
	</div>
	<div class="flex-1">
		<div class="flex items-center justify-between">
			<div class="flex flex-1 items-center gap-1">
				<h3 class="font-medium">{name}</h3>
				<span class="text-[15px] text-zinc-400">@{username}</span>
				<span class="text-[15px] text-zinc-400"> - </span>
				<time class="text-[15px] text-zinc-400">{date}</time>
			</div>
			<button class="rounded-full px-1 hover:bg-zinc-900"><Ellipsis size={16} /></button>
		</div>
		<div class="mt-1 space-y-3 leading-tight">
			{tweet}
		</div>
	</div>
</div>
