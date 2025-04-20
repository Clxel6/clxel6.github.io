<script>
	import '../app.css';
	import McBtn from '$lib/UI/McBtn.svelte';
	import McSection from '$lib/UI/McSection.svelte';

	let { children } = $props();
</script>

<McSection>
	<div class="flex gap-2">
		<McBtn text="Accueil" class="bg-defaut" />
		<McBtn link="/fiches-revisions" text="Fiches révision" class="bg-defaut" />
	</div>
</McSection>

{@render children()}
