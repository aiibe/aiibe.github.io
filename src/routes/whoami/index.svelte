<script>
	import { title, projects } from '../../../raw/site.json';
	import Logo from '$lib/Logo.svelte';
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<div class="grid grid-cols-1 mx-4">
	<div class="mx-auto md:w-1/2">
		<div class="mb-6">
			<h2 class="text-4xl font-bold text-gray-800">
				I love to play with web technologies to build tools like these following projects
			</h2>
		</div>

		<ul>
			{#each projects as { name, description, picture, isPublic }}
				<div class="flex mb-4 shadow max-w-xl">
					<div
						class="h-32 md:h-auto w-32 md:w-48 flex-none bg-cover bg-center bg-no-repeat rounded-l text-center overflow-hidden"
						style="background-image: url('{picture}')"
						title={name}
					/>
					<div class="p-4 flex flex-col justify-between leading-normal">
						<div class="mb-8">
							{#if !isPublic}
								<p class="text-sm text-grey-dark flex items-center">
									<svg
										class="text-grey w-3 h-3 mr-2"
										xmlns="http://www.w3.org/2000/svg"
										height="12"
										width="12"
										viewBox="0 0 20 20"
									>
										<path
											d="M4 8V6a6 6 0 1 1 12 0v2h1a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2v-8c0-1.1.9-2 2-2h1zm5 6.73V17h2v-2.27a2 2 0 1 0-2 0zM7 6v2h6V6a3 3 0 0 0-6 0z"
										/>
									</svg>
									Private
								</p>
							{:else}
								<p class="text-sm text-grey-dark flex items-center">
									<svg
										class="text-grey w-3 h-3 mr-2"
										viewBox="0 0 24 24"
										height="12"
										width="12"
										xmlns="http://www.w3.org/2000/svg"
										><path
											d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"
										/></svg
									>
									Public
								</p>
							{/if}
							<div class="text-black font-bold text-xl mb-2">{name}</div>
							<p class="text-grey-darker text-base">{description}</p>
						</div>
						<div class="flex items-center">
							<img
								class="w-10 h-10 rounded-full mr-4"
								src="https://pbs.twimg.com/profile_images/885868801232961537/b1F6H4KC_400x400.jpg"
								alt="Avatar of Jonathan Reinink"
							/>
							<div class="text-sm">
								<p class="text-black leading-none">Jonathan Reinink</p>
								<p class="text-grey-dark">Aug 18</p>
							</div>
						</div>
					</div>
				</div>
			{/each}
		</ul>
	</div>
</div>
