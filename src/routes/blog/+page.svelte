<script>
	const posts = [
		{
			title: 'Learning and Touch Typing',
			excerpt: 'We generally know a lot about learning...',
			date: '2025-05-18',
			slug: 'learning-and-touch-typing'
		},
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

	<blockquote class="border-l-4 border-gray-500 pl-4 italic text-gray-400">
		<p>“I write entirely to find out what I'm thinking, what I'm looking at, what I see and what it means. What I want and what I fear. (… or to feed an LLM)”</p>
		<footer class="mt-2 text-sm text-gray-500">— Joan Didion</footer>
	</blockquote>

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
