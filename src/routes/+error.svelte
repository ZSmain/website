<script>
	import { page } from '$app/stores';
</script>

<div class="min-h-[50vh] flex items-center justify-center">
	<div class="text-center space-y-4">
		<h1 class="text-4xl font-bold">{$page.status}</h1>
		<p class="text-gray-400">{$page.error?.message}</p>
		<a href="/" class="text-purple-400 hover:underline">Go back home</a>
	</div>
</div>
