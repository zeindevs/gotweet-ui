<script>
	import { blur } from 'svelte/transition';
	import LucideIcon from './lucide-icon.svelte';

	export let post = '';
</script>

<form class="border-b border-zinc-800">
	<div class="flex gap-3 p-4">
		<div class="h-10 w-10 overflow-hidden rounded-full bg-zinc-700">
			<img src="https://i.pravatar.cc/150?img=3" class="h-full w-full" alt="ZEN" />
		</div>
		<div class="flex-1">
			<input
				class="w-full bg-transparent py-2 outline-none"
				placeholder="What is happening?!"
				bind:value={post}
			/>
			{#if post}
				<div transition:blur class="border-b border-zinc-800 p-3">
					<button class="flex items-center gap-2 text-sm text-blue-500">
						<span class="flex items-center justify-center text-blue-500">
							<LucideIcon name="Globe" size={16} />
						</span> Everyone can reply</button
					>
				</div>
				<div transition:blur class="flex justify-between p-3 pb-0">
					<ul class="flex items-center gap-1">
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="Image" size={20} />
							</button>
						</li>
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="ImagePlay" size={20} />
							</button>
						</li>
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="ListTodo" size={20} />
							</button>
						</li>
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="Smile" size={20} />
							</button>
						</li>
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="CalendarClock" size={20} />
							</button>
						</li>
						<li>
							<button
								class="flex items-center justify-center rounded-full p-1.5 text-blue-500 hover:bg-blue-500/20"
							>
								<LucideIcon name="MapPin" size={20} />
							</button>
						</li>
					</ul>
					<button class="rounded-full bg-blue-500 px-5 py-2 font-medium hover:bg-blue-500/90"
						>Post</button
					>
				</div>
			{/if}
		</div>
	</div>
</form>
