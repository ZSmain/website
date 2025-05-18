<script>
	const links = [
		{ href: 'https://github.com/ZSmain', text: 'GitHub' },
		{ href: 'mailto:ishmael.zouaoui@gamil.com', text: 'Email' }
	];
</script>

<div class="mx-auto max-w-2xl space-y-12">
	<section class="space-y-4">
		<h1 class="text-accent font-mono text-4xl font-semibold">Hi, I'm Ismail</h1>
		<p class="text-text/80 text-xl leading-relaxed">
			I'm a software developer with a focus on web technologies and creating intuitive user experiences.
			Currently at <a href="https://flexup.com" class="text-accent hover:text-accent/80">FlexUp</a>, 
			where I am helping building a platform that enable businesses to manage their finances in innovative ways.
		</p>
	</section>

	<section class="space-y-4">
		<h2 class="text-accent font-mono text-2xl font-semibold">Selected projects</h2>
		<ul class="space-y-3">
			<li>
				<a href="https://hackbcn.org" class="group block">
					<span class="text-text group-hover:text-accent">HackBCN website</span>
					<span class="text-text/60 block text-sm">A website for the HackBCN coference</span>
				</a>
			</li>
		</ul>
	</section>

	<section class="space-y-4">
		<h2 class="text-accent font-mono text-2xl font-semibold">Recent posts</h2>
		<ul class="space-y-3">
			<li>
				<a href="/blog/learning-and-touch-typing" class="group block">
					<span class="text-text group-hover:text-accent">Learning and Touch Typing</span>
					<span class="text-text/60 block text-sm">We generally know a lot about learning</span>
				</a>
			</li>
			<li>
				<a href="/blog/aesthetics" class="group block">
					<span class="text-text group-hover:text-accent">Aesthetics</span>
					<span class="text-text/60 block text-sm">I was wrong about aesthetics</span>
				</a>
			</li>
		</ul>
	</section>

	<section class="border-border border-t pt-8">
		<div class="flex gap-4">
			{#each links as link}
				<a href={link.href} class="text-text/60 hover:text-accent">{link.text}</a>
			{/each}
		</div>
	</section>
</div>
