<script>
	import BlogPost from '$lib/components/BlogPost.svelte';

	const posts = [
		{
			title: 'Getting Started with SvelteKit',
			excerpt: 'Learn how to build modern web applications with SvelteKit...',
			date: '2024-01-15',
			slug: 'getting-started-with-sveltekit',
			tags: ['SvelteKit', 'Web Development']
		}
		// Add more blog posts here
	];
</script>

<div class="space-y-8">
	<h1 class="text-3xl font-bold">Blog</h1>

	<div class="space-y-6">
		{#each posts as post}
			<BlogPost {post} />
		{/each}
	</div>
</div>
