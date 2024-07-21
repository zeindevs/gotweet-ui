<script>
	import Ellipsis from 'lucide-svelte/icons/ellipsis';
</script>

<aside class="flex w-full max-w-sm flex-col border-l border-zinc-800">
	<form class="border-b border-zinc-800 p-4">
		<input
			class="w-full rounded-full bg-zinc-900 px-5 py-3 outline-none ring-blue-500 focus:ring-1"
			placeholder="Search"
		/>
	</form>

	<div class="flex-1 space-y-4 overflow-y-auto p-4">
		<div class="space-y-2 rounded-2xl border border-zinc-800 p-4">
			<h3 class="text-xl font-medium">Subscribe to Premium</h3>
			<p class="text-sm leading-tight">
				Subscribe to nlck new features and if eligible, receive a share of ads revenue.
			</p>
			<div class="pt-2">
				<button
					class="rounded-full bg-blue-500 px-5 py-2.5 text-sm font-medium hover:bg-blue-500/90"
					>Subscribe</button
				>
			</div>
		</div>

		<div class="overflow-hidden rounded-2xl border border-zinc-800">
			<div class="px-4 py-3">
				<h3 class="text-xl font-bold">Trends for you</h3>
			</div>
			<div>
				<div class="flex cursor-pointer items-start px-4 py-3 hover:bg-zinc-900/50">
					<div class="flex-1">
						<span class="text-[13px] text-zinc-400">Trending in Indonesia</span>
						<h3 class="font-medium">CrowdStike</h3>
						<p class="text-[13px] leading-tight text-zinc-400">650K posts</p>
					</div>
					<button class="rounded-full px-1 hover:bg-zinc-900"><Ellipsis size={16} /></button>
				</div>
				<div class="flex cursor-pointer items-start px-4 py-3 hover:bg-zinc-900/50">
					<div class="flex-1">
						<span class="text-[13px] text-zinc-400">Trending in Indonesia</span>
						<h3 class="font-medium">Aoka</h3>
						<p class="text-[13px] leading-tight text-zinc-400">7,897 posts</p>
					</div>
					<button class="rounded-full px-1 hover:bg-zinc-900"><Ellipsis size={16} /></button>
				</div>
				<div class="flex cursor-pointer items-start px-4 py-3 hover:bg-zinc-900/50">
					<div class="flex-1">
						<span class="text-[13px] text-zinc-400">Technology · Trending</span>
						<h3 class="font-medium">Svelte</h3>
						<p class="text-[13px] leading-tight text-zinc-400">1K posts</p>
					</div>
					<button class="rounded-full px-1 hover:bg-zinc-900"><Ellipsis size={16} /></button>
				</div>
			</div>
		</div>

		<div class="overflow-hidden rounded-2xl border border-zinc-800">
			<div class="px-4 py-3">
				<h3 class="text-xl font-bold">Who to follow</h3>
			</div>
			<div>
				<div class="flex cursor-pointer items-start gap-3 px-4 py-3 hover:bg-zinc-900/50">
					<div class="h-10 w-10 rounded-full bg-zinc-700"></div>

					<div class="flex-1">
						<h3 class="font-medium">Mack</h3>
						<p class="text-[13px] leading-tight text-zinc-400">@mack</p>
					</div>
					<button
						class="rounded-full bg-white px-5 py-2 text-sm font-medium text-zinc-950 hover:bg-white/90"
						>Follow</button
					>
				</div>
				<div class="flex cursor-pointer items-start gap-3 px-4 py-3 hover:bg-zinc-900/50">
					<div class="h-10 w-10 rounded-full bg-zinc-700"></div>

					<div class="flex-1">
						<h3 class="font-medium">Zack</h3>
						<p class="text-[13px] leading-tight text-zinc-400">@zack</p>
					</div>
					<button
						class="rounded-full bg-white px-5 py-2 text-sm font-medium text-zinc-950 hover:bg-white/90"
						>Follow</button
					>
				</div>
			</div>
		</div>
	</div>
</aside>
