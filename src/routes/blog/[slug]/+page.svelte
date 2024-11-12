<script>
	import { page } from '$app/stores';
	import { formatDistance } from 'date-fns';

	// This would typically come from your content management system or markdown files
	const posts = {
		'getting-started-with-sveltekit': {
			title: 'Getting Started with SvelteKit',
			date: '2024-01-15',
			content: `
          <h2>Introduction</h2>
          <p>SvelteKit is a framework for building web applications of all sizes, with a beautiful development experience and flexible filesystem-based routing.</p>
          
          <h2>Why SvelteKit?</h2>
          <p>SvelteKit offers several advantages:</p>
          <ul>
            <li>Zero-config deployment to any platform</li>
            <li>Automatic code-splitting</li>
            <li>Server-side rendering (SSR) by default</li>
            <li>Static site generation (SSG) capabilities</li>
          </ul>
        `
		}
	};

	let post = $derived(posts[$page.params.slug]);
</script>

{#if post}
	<article class="max-w-3xl mx-auto space-y-8">
		<header class="space-y-4">
			<h1 class="text-3xl font-bold">{post.title}</h1>
			<div class="text-gray-400">
				{formatDistance(new Date(post.date), new Date(), { addSuffix: true })}
			</div>
		</header>

		<div class="prose prose-invert max-w-none">
			{@html post.content}
		</div>
	</article>
{:else}
	<div class="text-center py-12">
		<h1 class="text-2xl font-bold">Post not found</h1>
		<a href="/blog" class="text-purple-400 hover:underline">Back to blog</a>
	</div>
{/if}
