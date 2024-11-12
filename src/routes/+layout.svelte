<script lang="ts">
	import '../app.css';
	import { Menu, X, Github, Linkedin } from 'lucide-svelte';
	import { writable } from 'svelte/store';

	/** @type {{children?: import('svelte').Snippet}} */
	let { children } = $props();

	const isMenuOpen = writable(false);
</script>

<div class="min-h-screen bg-[#1e1e1e] text-gray-100">
	<header class="border-b border-gray-800">
		<nav class="container mx-auto px-4 py-4">
			<div class="flex justify-between items-center">
				<a href="/" class="text-xl font-bold hover:text-purple-400">Portfolio</a>

				<!-- Mobile menu button -->
				<button class="md:hidden" onclick={() => ($isMenuOpen = !$isMenuOpen)}>
					{#if $isMenuOpen}
						<X size={24} />
					{:else}
						<Menu size={24} />
					{/if}
				</button>

				<!-- Desktop menu -->
				<div class="hidden md:flex space-x-8">
					<a href="/projects" class="hover:text-purple-400">Projects</a>
					<a href="/blog" class="hover:text-purple-400">Blog</a>
					<a href="/about" class="hover:text-purple-400">About</a>
				</div>

				<!-- Social links -->
				<div class="hidden md:flex space-x-4">
					<a href="https://github.com" target="_blank" rel="noopener noreferrer">
						<Github size={20} />
					</a>
					<a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">
						<Linkedin size={20} />
					</a>
				</div>
			</div>

			<!-- Mobile menu -->
			{#if $isMenuOpen}
				<div class="md:hidden pt-4 pb-2">
					<div class="flex flex-col space-y-4">
						<a href="/projects" class="hover:text-purple-400">Projects</a>
						<a href="/blog" class="hover:text-purple-400">Blog</a>
						<a href="/about" class="hover:text-purple-400">About</a>
					</div>
				</div>
			{/if}
		</nav>
	</header>

	<main class="container mx-auto px-4 py-8">
		{@render children?.()}
	</main>

	<footer class="border-t border-gray-800 py-8">
		<div class="container mx-auto px-4 text-center text-gray-400">
			<p>© {new Date().getFullYear()} Your Name. All rights reserved.</p>
		</div>
	</footer>
</div>
