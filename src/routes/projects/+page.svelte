<script>
	import ProjectCard from '$lib/components/ProjectCard.svelte';

	const projects = [
		{
			title: 'Project One',
			description: 'A full-stack web application built with SvelteKit and PostgreSQL',
			tags: ['SvelteKit', 'PostgreSQL', 'TailwindCSS'],
			github: 'https://github.com/yourusername/project-one',
			demo: 'https://project-one.demo',
			image: 'https://via.placeholder.com/600x400'
		}
		// Add more projects here
	];
</script>

<div class="space-y-8">
	<h1 class="text-3xl font-bold">Projects</h1>

	<div class="grid md:grid-cols-2 gap-8">
		{#each projects as project}
			<ProjectCard {project} />
		{/each}
	</div>
</div>
