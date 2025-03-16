<script>
	import { page } from '$app/stores';

	const posts = {
		'aesthetics': {
			title: 'I was wrong about aesthetics',
			date: '2025-03-16',
			content: `
          	<p>
				Aesthetics, such a complementary thing in life. Life is about essentials and important things. When it comes to clothes, I used to think you should wear simple, good-quality ones in black or brown. Dark blue felt like a stretch, and mixing in flashy colors like red? Absolutely forbidden. With food, I believed in eating healthy. What people call a "treat meal" isn’t a treat—it’s a cheat meal. In coding, I obsessed over performance. I’d squeeze every bit of speed out of the code, even if it turned ugly. That was fine, because it was fast—blazingly fast. And don’t get me started on code editors. Those theme-obsessed hippies, asking their favorite YouTuber, "Oh, what’s the name of that beautiful theme?" Khukh. Some even buy fonts. No comment needed.
			</p>
			<p>
				That’s how I used to approach everything—always picking simple, sensible defaults and trusting people smarter than me who followed frameworks and best practices. How did I feel about it? It didn’t matter! I figured I didn’t know better and would get used to it. But then I read an article by David Heinemeier Hansson that shook me. He wrote about how much he enjoys writing Ruby, despite its obvious performance trade-offs, and how that joy matters. It made me question the rigid framework I’d trapped myself in.
			</p>
			<p>
				Recently, I also heard Mitchell Hashimoto, the creator of the Ghostty terminal, on a podcast. He was asked why he chose the Zig programming language over Rust or Go—a language he’d mastered over a decade. His answer? "I don’t enjoy writing Go anymore." Instead, he found joy in Zig. That hit me hard. We—you, me, all of us—spend so much time at our computers. Why torture ourselves with what the gurus say is the "right" way? Why not choose what we enjoy?
			</p>
          	<p>
				Hansson and Hashimoto made it clear: enjoyment isn’t a luxury—it’s essential, especially in things we do every day, like coding. It’s not just about best practices or peak performance; it’s about finding joy in the process. So, I was wrong about aesthetics. They’re not just complementary—they’re vital. Why not choose what makes you happy?
			</p>
        	`
		},
	};

	let post = $derived(posts[$page.params.slug]);
</script>

<article class="mx-auto max-w-2xl">
	{#if post}
		<header class="mb-8">
			<h1 class="text-3xl font-semibold text-white">{post.title}</h1>
			<time class="mt-2 block text-gray-400">
				{new Date(post.date).toLocaleDateString('en-US', {
					year: 'numeric',
					month: 'long',
					day: 'numeric'
				})}
			</time>
		</header>

		<div class="prose">
			{@html post.content}
		</div>

		<div class="mt-16">
			<a href="/blog" class="text-blue-400 hover:text-blue-300">← All posts</a>
		</div>
	{:else}
		<div class="py-12 text-center">
			<h1 class="mb-4 text-2xl font-semibold text-white">Post not found</h1>
			<a href="/blog" class="text-blue-400 hover:text-blue-300">Back to blog</a>
		</div>
	{/if}
</article>
