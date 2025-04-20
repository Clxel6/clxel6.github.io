<script>
	import McSection from '$lib/UI/McSection.svelte';

	const equations = {
		eq1: `$$\\theta\\,(\\text{rad}) = \\frac{\\lambda\\,(\\text{m})}{a\\,(\\text{m})}$$`,
		eq2: `$$\\tan(\\theta) \\approx \\theta = \\frac{L\\,(\\text{m})}{2D\\,(\\text{m})}$$`,
		eq3: `$$\\delta = d_2 - d_1$$`
	};
</script>

<McSection>
	<div class="flex flex-col gap-8">
		<!-- I. Diffraction -->
		<div>
			<h2 class="text-xl text-red-700">I. Diffraction</h2>
			<p>
				- Une onde se propage de façon rectiligne. <br />
				- Au voisinage d’un objet (ouverture ou obstacle), il y a
				<span class="fluo">étalement des directions de propagation</span>.
			</p>
			<img src="/diffraction.jpg" alt="Schéma diffraction" />
			<p>- $ \theta $ est l’angle caractéristique de diffraction.</p>
			<p class="fluov text-xl">{@html equations.eq1}</p>
			<p class="fluov text-xl">{@html equations.eq2}</p>
			<p>avec $ \lambda $ la longueur d'onde, $ a $ la mesure de l'objet.</p>
		</div>

		<!-- II. Interférences -->
		<div>
			<h2 class="text-xl text-red-700">II. Interférences</h2>
			<div class="flex flex-col gap-4 md:flex-row">
				<img src="/interferences-1.jpg" alt="Interférences 1" class="max-w-full md:max-w-1/2" />
				<img src="/interferences-2.jpg" alt="Interférences 2" class="max-w-full md:max-w-1/2" />
			</div>
			<p>
				- En tout point $ M $ où les ondes sont en phase : <span class="fluo"
					>interférences constructives</span
				>. <br />
				- En tout point $ M $ où elles sont en opposition de phase :
				<span class="fluo">interférences déstructives</span>.
			</p>
			<p>- Décalage de marche $ \delta $ :</p>
			<p class="fluov text-xl">{@html equations.eq3}</p>
			<p>
				Si {@html '$ \\delta = k \\cdot \\lambda \\Rightarrow \\text{constructives} $'} <br />
				Si {@html '$ \\delta = \\left(k + \\tfrac{1}{2}\\right) \\cdot \\lambda \\Rightarrow \\text{déstructives} $'}
				<br />
				- <span class="fluo">Interfrange $ i $</span> : distance entre deux franges sombres ou brillantes
				successives.
			</p>
		</div>
	</div>
</McSection>
