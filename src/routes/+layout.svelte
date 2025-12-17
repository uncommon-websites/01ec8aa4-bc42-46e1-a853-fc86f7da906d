<script lang="ts">
	import "../app.css";
    import Header from "$lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<div class="min-h-screen bg-white font-sans text-gray-900 selection:bg-primary-100 selection:text-primary-900">
    <Header />
    <slot />
    <Footer />
</div>
