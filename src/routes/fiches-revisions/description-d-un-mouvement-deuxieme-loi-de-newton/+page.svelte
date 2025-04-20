<script>
	import McSection from '$lib/UI/McSection.svelte';

	const equations = {
		eq1: `$$\\vec{OM}(t) = \\begin{pmatrix}x(t) \\\\ y(t)\\end{pmatrix}$$`,
		eq2: `$$\\vec{v}(t) = \\frac{d\\vec{OM}}{dt} = \\begin{pmatrix}x'(t) \\\\ y'(t)\\end{pmatrix}$$`,
		eq3: `$$\\vec{a}(t) = \\frac{d\\vec{v}}{dt} = \\begin{pmatrix}x''(t) \\\\ y''(t)\\end{pmatrix}$$`,
		eq4: `$$\\vec{v} = \\text{cste},\\ \\vec{a} = 0 \\Rightarrow \\text{mouvement rectiligne uniforme}$$`,
		eq5: `$$\\vec{a} = \\text{cste} \\Rightarrow \\text{mouvement rectiligne uniformément accéléré}$$`,
		eq6: `$$\\vec{v} = \\text{cste} \\nRightarrow \\vec{a} = 0$$`,
		eq7: `$$\\vec{v}(t) = v(t) \\cdot \\vec{T}$$`,
		eq8: `$$\\vec{a}(t) = \\frac{dv}{dt} \\cdot \\vec{T} + \\frac{v^2}{R} \\cdot \\vec{N}$$`,
		eq9: `$$\\sum \\vec{F} = m \\cdot \\vec{a}$$`
	};
</script>

<McSection>
	<div class="flex flex-col gap-8">
		<!-- I. Vecteurs position, vitesse, accélération -->
		<div>
			<h2 class="text-xl text-red-700">I. Vecteurs position, vitesse, accélération</h2>
			<p>- Le vecteur position d’un point $ M $ à l’instant $ t $ est :</p>
			<p class="fluov text-xl">{@html equations.eq1}</p>
			<p>- Le vecteur vitesse est la dérivée du vecteur position :</p>
			<p class="fluov text-xl">{@html equations.eq2}</p>
			<p>- Le vecteur accélération est la dérivée du vecteur vitesse :</p>
			<p class="fluov text-xl">{@html equations.eq3}</p>
		</div>

		<!-- II. Exemples de mouvements -->
		<div>
			<h2 class="text-xl text-red-700">II. Exemples de mouvements</h2>
			<p>
				{@html '$ \\vec{v} = \\text{cste},\\ \\vec{a} = \\vec{0} \\Rightarrow $'} mouvement rectiligne
				uniforme
			</p>
			<p>
				{@html '$ \\vec{a} = \\text{cste} \\Rightarrow $'} mouvement rectiligne uniformément accéléré
			</p>
		</div>

		<!-- III. Mouvement circulaire -->
		<div>
			<h2 class="text-xl text-red-700">III. Mouvement circulaire</h2>
			<p>
				- <span class="fluor">ATTENTION</span>
				{@html '$ \\vec{v} = \\text{cste} \\nRightarrow \\vec{a} = \\vec{0} $'}
			</p>
			<p>
				- On utilise le <span class="fluo">repère de Frenet</span> :
			</p>
			<img src="/frenet.png" alt="Repère de Frenet" />
			<p class="fluov text-xl">{@html equations.eq7}</p>
			<p class="fluov text-xl">{@html equations.eq8}</p>
		</div>

		<!-- IV. Deuxième loi de Newton -->
		<div>
			<h2 class="text-xl text-red-700">IV. Deuxième loi de Newton</h2>
			<p>
				- Dans un <span class="fluo">référentiel galiléen</span>, la somme des forces appliquées à
				un système est égale à la masse fois l'accélération, soit :
			</p>
			<p class="fluov text-xl">{@html equations.eq9}</p>
		</div>
	</div>
</McSection>
