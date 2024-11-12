<script lang="ts">
	import { formatDistance } from 'date-fns';

	let { post } = $props();
</script>

<a href={`/blog/${post.slug}`}>
	<article class="bg-gray-900 p-6 rounded-lg hover:bg-gray-800 transition">
		<div class="space-y-4">
			<h2 class="text-xl font-semibold">{post.title}</h2>
			<p class="text-gray-400">{post.excerpt}</p>

			<div class="flex flex-wrap gap-2">
				{#each post.tags as tag}
					<span class="px-3 py-1 bg-purple-900/30 text-purple-300 rounded-full text-sm">
						{tag}
					</span>
				{/each}
			</div>

			<div class="text-sm text-gray-500">
				{formatDistance(new Date(post.date), new Date(), { addSuffix: true })}
			</div>
		</div>
	</article>
</a>
