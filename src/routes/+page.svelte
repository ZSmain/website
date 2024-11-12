<script>
	import { FileText, Briefcase, User } from 'lucide-svelte';
</script>

<div class="space-y-12">
	<section class="text-center space-y-4">
		<h1 class="text-4xl font-bold">Your Name</h1>
		<p class="text-xl text-gray-400">Full Stack Developer</p>
		<p class="max-w-2xl mx-auto text-gray-300">
			Passionate about creating elegant solutions to complex problems. Specializing in web
			development, cloud architecture, and open source contributions.
		</p>
	</section>

	<div class="grid md:grid-cols-3 gap-8">
		<a href="/projects" class="block p-6 bg-gray-900 rounded-lg hover:bg-gray-800 transition">
			<Briefcase class="mb-4" size={32} />
			<h2 class="text-xl font-semibold mb-2">Projects</h2>
			<p class="text-gray-400">Explore my latest work and side projects</p>
		</a>

		<a href="/blog" class="block p-6 bg-gray-900 rounded-lg hover:bg-gray-800 transition">
			<FileText class="mb-4" size={32} />
			<h2 class="text-xl font-semibold mb-2">Blog</h2>
			<p class="text-gray-400">Technical articles and thoughts on development</p>
		</a>

		<a href="/about" class="block p-6 bg-gray-900 rounded-lg hover:bg-gray-800 transition">
			<User class="mb-4" size={32} />
			<h2 class="text-xl font-semibold mb-2">About</h2>
			<p class="text-gray-400">Learn more about my journey and skills</p>
		</a>
	</div>
</div>
