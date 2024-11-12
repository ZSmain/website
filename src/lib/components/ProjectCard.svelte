<script lang="ts">
	import { Github, ExternalLink } from 'lucide-svelte';

	let { project } = $props();
</script>

<div class="bg-gray-900 rounded-lg overflow-hidden">
	<img src={project.image} alt={project.title} class="w-full h-48 object-cover" />
	<div class="p-6 space-y-4">
		<h2 class="text-xl font-semibold">{project.title}</h2>
		<p class="text-gray-400">{project.description}</p>

		<div class="flex flex-wrap gap-2">
			{#each project.tags as tag}
				<span class="px-3 py-1 bg-purple-900/30 text-purple-300 rounded-full text-sm">
					{tag}
				</span>
			{/each}
		</div>

		<div class="flex space-x-4">
			<a href={project.github} class="flex items-center space-x-2 text-gray-400 hover:text-white">
				<Github size={20} />
				<span>Code</span>
			</a>
			<a href={project.demo} class="flex items-center space-x-2 text-gray-400 hover:text-white">
				<ExternalLink size={20} />
				<span>Demo</span>
			</a>
		</div>
	</div>
</div>
