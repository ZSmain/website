<script>
	const posts = [
		{
			title: 'I was wrong about aesthetics',
			excerpt: 'Aesthetics!, such a complementary thing in life...',
			date: '2025-03-16',
			slug: 'aesthetics'
		},
	];
</script>

<div class="mx-auto max-w-2xl space-y-8">
	<h1 class="text-3xl font-semibold text-white">Writing</h1>

	<div class="space-y-8">
		{#each posts as post}
			<article>
				<a href={`/blog/${post.slug}`} class="group block">
					<h2 class="text-xl font-medium text-white group-hover:text-blue-400">{post.title}</h2>
					<p class="mt-1 text-gray-400">{post.excerpt}</p>
					<time class="mt-2 block text-sm text-gray-500"
						>{new Date(post.date).toLocaleDateString('en-US', {
							year: 'numeric',
							month: 'long',
							day: 'numeric'
						})}</time
					>
				</a>
			</article>
		{/each}
	</div>
</div>
