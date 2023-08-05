<script>
	let expanded = false

	function onMenuToggleClick() {
		expanded = !expanded
	}
</script>

<nav class="bg-gray-100 px-4 py-4 transition-[height] duration-300">
	<div class="flex flex-row items-center justify-between">
		<a href="/" class="text-2xl font-bold">Kitblog</a>

		<ul class="hidden md:flex md:flex-row md:gap-x-8">
			<li>
				<a href="/explore">Explore</a>
			</li>
			<li>
				<a href="/about">About</a>
			</li>
			<li>
				<a href="/contact">Contact</a>
			</li>
			<li>
				<a href="/rss.xml">RSS</a>
			</li>
		</ul>

		<button
			class="hidden rounded-lg bg-blue-700 px-5 py-2.5 text-sm font-medium text-white hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800 md:block">
			Login
		</button>

		<button
			class="block rounded-lg border border-gray-200 bg-white px-5 py-2.5 text-sm font-medium text-gray-900 hover:bg-gray-100 hover:text-blue-700 focus:z-10 focus:outline-none focus:ring-4 focus:ring-gray-200 dark:border-gray-600 dark:bg-gray-800 dark:text-gray-400 dark:hover:bg-gray-700 dark:hover:text-white dark:focus:ring-gray-700 md:hidden"
			on:click={onMenuToggleClick}>
			Menu
		</button>
	</div>

	{#if expanded}
		<ul class="mt-8 flex flex-row flex-wrap justify-center gap-x-8 gap-y-4 md:hidden">
			<li class="grid place-content-center">
				<a class="px-4 py-2" href="/explore">Explore</a>
			</li>
			<li class="grid place-content-center">
				<a class="px-4 py-2" href="/about">About</a>
			</li>
			<li class="grid place-content-center">
				<a class="px-4 py-2" href="/contact">Contact</a>
			</li>
			<li class="grid place-content-center">
				<a class="px-4 py-2" href="/rss.xml">RSS</a>
			</li>
			<li class="grid place-content-center">
				<button
					class="rounded-lg bg-blue-700 px-5 py-2.5 text-sm font-medium text-white hover:bg-blue-800 focus:outline-none focus:ring-4 focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
					Login
				</button>
			</li>
		</ul>
	{/if}
</nav>
