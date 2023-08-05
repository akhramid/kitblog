<script lang="ts">
	import { title, description } from '$lib/config';

	import Header from './layout/header.svelte';
	import Footer from './layout/footer.svelte';
	import '../styles/app.css';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={description} />
</svelte:head>

<Header />
<main class="px-8 py-6">
	<slot />
</main>
<Footer />
