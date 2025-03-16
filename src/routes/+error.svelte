<script>
	import { page } from '$app/stores';
</script>

<div class="flex min-h-[50vh] items-center justify-center">
	<div class="space-y-4 text-center">
		<h1 class="text-4xl font-bold">{$page.status}</h1>
		<p class="text-gray-400">{$page.error?.message}</p>
		<a href="/" class="text-purple-400 hover:underline">Go back home</a>
	</div>
</div>
