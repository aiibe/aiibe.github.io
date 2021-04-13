<script>
	import { title, projects } from '../../raw/site.json';
	import { goto } from '$app/navigation';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="grid grid-cols-1 mx-4 flex-grow">
	<div class="mx-auto md:w-1/2 py-4 text-center flex-grow">
		<div class="flex flex-col h-full">
			<div class="flex-grow flex flex-col justify-center items-center">
				<div class="mb-12">
					<p class="text-4xl font-bold text-gray-800">Hello, my name is Souk.</p>
					<p class="text-2xl font-bold text-gray-400">
						I build web apps with Javascript and other languages.
					</p>
				</div>

				<a
					href="/whoami"
					class="flex bg-gray-900 font-bold text-white px-4 py-3 transition duration-300 ease-in-out hover:bg-gray-600 mr-6"
				>
					Get to know me
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="inline ml-2 w-6 stroke-current text-white stroke-2"
						viewBox="0 0 24 24"
						fill="none"
						stroke-linecap="round"
						stroke-linejoin="round"
						><line x1="5" y1="12" x2="19" y2="12" /><polyline points="12 5 19 12 12 19" /></svg
					>
				</a>
			</div>

			<div class="my-8">
				<p class="text-sm text-gray-400">Built with SvelteKit</p>
			</div>
		</div>
	</div>
</div>
