<script>
	import { title, projects } from '../../raw/site.json';
	import { goto } from '$app/navigation';

	function next(){
		goto('/whoami')
	}
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>


<div class="grid grid-cols-1 mx-4 flex-grow" on:click="{next}">
	<div class="mx-auto md:w-1/2 py-4 text-center flex-grow">
		<div class="flex flex-col h-full">
			<div><p class="text-4xl font-bold text-gray-800">Hello, my name is Souk.</p></div>

			<div class="flex-grow flex items-center">
				<p class="text-2xl font-bold text-gray-400">
					I build web tools with Javascript and other languages.
				</p>
			</div>

			<div class="my-8">
				<p class="text-sm text-gray-400">If you think this page is nice and clean</p>
				<p class="text-sm text-gray-400">Tap on this screen</p>
			</div>
		</div>
	</div>
</div>
