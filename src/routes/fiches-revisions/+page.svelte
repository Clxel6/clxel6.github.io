<script>
	import McSection from '$lib/UI/McSection.svelte';
</script>

<div class="flex flex-col gap-1 mt-1">
	<McSection>
		<h1 class="text-xl">Physique</h1>
		<div class="m-2 grid grid-cols-5 gap-2">
			<a href="/fiches-revisions/son-et-effet-doppler" data-sveltekit-reload>
				<McSection class="text-center underline">Son et Effet Doppler</McSection>
			</a>
			<a href="/fiches-revisions/diffraction-et-interferences" data-sveltekit-reload>
				<McSection class="text-center underline">Diffraction et Interférences</McSection>
			</a>
			<a
				href="/fiches-revisions/description-d-un-mouvement-deuxieme-loi-de-newton"
				data-sveltekit-reload
			>
				<McSection class="text-center underline">
					Description d'un mouvement, Deuxième loi de Newton
				</McSection>
			</a>
			<a href="/fiches-revisions/mouvement-dans-un-champ-uniforme" data-sveltekit-reload>
				<McSection class="text-center underline">Mouvement dans un champ uniforme</McSection>
			</a>
			<a href="/fiches-revisions/mouvement-dans-un-champ-de-gravitation" data-sveltekit-reload>
				<McSection class="text-center underline">Mouvement dans un champ de gravitation</McSection>
			</a>
		</div>
		<p>A venir : dipole RC, lunettre astro, thermodynamique, dynamique des fluides.</p>
	</McSection>

	<McSection>
		<h1 class="text-xl">Chimie</h1>
		<p>A venir : tout</p>
	</McSection>
</div>
