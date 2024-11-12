<script>
	import { Github, Mail, Linkedin } from 'lucide-svelte';
</script>

<div class="max-w-3xl mx-auto space-y-8">
	<section class="space-y-4">
		<h1 class="text-3xl font-bold">About Me</h1>
		<p class="text-gray-300">
			I'm a passionate full-stack developer with expertise in modern web technologies. My journey in
			software development started with a curiosity for creating things that make a difference in
			people's lives.
		</p>
	</section>

	<section class="space-y-4">
		<h2 class="text-2xl font-semibold">Skills</h2>
		<div class="grid grid-cols-2 md:grid-cols-3 gap-4">
			<div class="bg-gray-900 p-4 rounded-lg">
				<h3 class="font-medium mb-2">Frontend</h3>
				<ul class="text-gray-400 space-y-1">
					<li>React / SvelteKit</li>
					<li>TypeScript</li>
					<li>Tailwind CSS</li>
				</ul>
			</div>
			<div class="bg-gray-900 p-4 rounded-lg">
				<h3 class="font-medium mb-2">Backend</h3>
				<ul class="text-gray-400 space-y-1">
					<li>Node.js</li>
					<li>PostgreSQL</li>
					<li>REST APIs</li>
				</ul>
			</div>
			<div class="bg-gray-900 p-4 rounded-lg">
				<h3 class="font-medium mb-2">Tools</h3>
				<ul class="text-gray-400 space-y-1">
					<li>Git</li>
					<li>Docker</li>
					<li>AWS</li>
				</ul>
			</div>
		</div>
	</section>

	<section class="space-y-4">
		<h2 class="text-2xl font-semibold">Contact</h2>
		<div class="flex flex-col md:flex-row gap-4">
			<a
				href="mailto:your.email@example.com"
				class="flex items-center gap-2 text-gray-300 hover:text-purple-400"
			>
				<Mail size={20} />
				<span>your.email@example.com</span>
			</a>
			<a
				href="https://github.com/yourusername"
				class="flex items-center gap-2 text-gray-300 hover:text-purple-400"
			>
				<Github size={20} />
				<span>GitHub</span>
			</a>
			<a
				href="https://linkedin.com/in/yourusername"
				class="flex items-center gap-2 text-gray-300 hover:text-purple-400"
			>
				<Linkedin size={20} />
				<span>LinkedIn</span>
			</a>
		</div>
	</section>
</div>
