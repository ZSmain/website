<script lang="ts">
	import '../app.css';
	import { page } from '$app/stores';

	let { children } = $props();
</script>

<div class="bg-background min-h-screen">
	<header class="mx-auto max-w-2xl px-4 py-8">
		<nav>
			<div class="flex items-center justify-between">
				<a href="/" class="text-accent font-mono font-medium">Ismail Zouaoui</a>

				<div class="flex space-x-6">
					<a href="/blog" class="nav-link" class:active={$page.url.pathname === '/blog'}>Writing</a>
					<a href="/about" class="nav-link" class:active={$page.url.pathname === '/about'}>About</a>
				</div>
			</div>
		</nav>
	</header>

	<main class="px-4 py-12">
		{@render children()}
	</main>
</div>
