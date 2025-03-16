<script>
	const links = [
		{ href: 'https://github.com/ZSmain', text: 'GitHub' },
		{ href: 'mailto:ishmael.zouaoui@gamil.com', text: 'Email' }
	];
</script>

<div class="mx-auto max-w-2xl space-y-8">
	<h1 class="text-3xl font-semibold text-white">About</h1>

	<div class="space-y-4 text-lg">
        <p>
            I'm a software developer with a focus on web technologies and a passion for creating intuitive user experiences.
        </p>
        
        <p>
            Currently, I'm working at <a href="https://flexup.com" class="text-blue-400 hover:text-blue-300">FlexUp</a>, 
            where I help build a platform that enables businesses to manage their finances in innovative ways.
        </p>

        <p>
            Previously, I worked at a telecommunications company where I developed internal tools
            for visualizing and analyzing network data.
        </p>

        <p>
            When I'm not coding, I enjoy reading, running, and learning new languages.
        </p>
    </div>

	<div class="border-t border-gray-800 pt-8">
		<div class="flex gap-4">
			{#each links as link}
				<a href={link.href} class="text-gray-400 hover:text-white">{link.text}</a>
			{/each}
		</div>
	</div>
</div>
