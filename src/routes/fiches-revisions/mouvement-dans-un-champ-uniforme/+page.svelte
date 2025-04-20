<script>
	import McSection from '$lib/UI/McSection.svelte';

	const equations = {
		eq1: `$$\\sum \\vec{F} = \\vec{P} = m \\cdot \\vec{a} \\Rightarrow \\vec{a} = \\vec{g}$$`,
		eq2: `$$\\sum \\vec{F} = \\vec{F_e} = m \\cdot \\vec{a} \\Rightarrow \\vec{a} = \\frac{q \\cdot \\vec{E}}{m}$$`,
		eq3: `$$\\Delta E_c = \\sum W_{\\text{AB}}(\\vec{F}_{\\text{ext}})$$`,
		eq4: `$$\\Delta E_m = \\sum W_{\\text{AB}}(\\vec{F}_{\\text{nc}})$$`
	};
</script>

<McSection>
	<div class="flex flex-col gap-8">
		<!-- I. Champ uniforme -->
		<div>
			<h2 class="text-xl text-red-700">I. Champ uniforme</h2>
			<p>
				- Un <span class="fluo">champ uniforme</span> a une direction, un sens et une intensité
				constantes dans tout l’espace (ex : {@html '$ \\vec{g} $'}).<br />
				{@html '- À l’instant initial  t = 0 , on connaît la masse $ m $, un angle $ \\alpha $, une vitesse $ v $, et une position : ce sont les <span class="fluo">conditions initiales</span>.'}<br
				/>
				- Dans un référentiel galiléen, on applique la deuxième loi de Newton :
			</p>
			<p class="fluov text-xl">{@html equations.eq1}</p>
			<p>Donc {@html '$ \\vec{a} = \\begin{pmatrix}a_x = 0 \\\\ a_z = -g\\end{pmatrix} $'}</p>
			<p>
				- On détermine ensuite les expressions de {@html '$ \\vec{v}(t) $'} et {@html '$ \\vec{OM}(t) $'}
				par
				<span class="fluo">intégration</span>.<br />
				- Deux grandeurs décrivent le trajet :
				{@html '<span class="fluo">la flèche</span> (valeur maximale de $ z(t) $, lorsque $ v_z(t) = 0 $) et <span class="fluo">la portée</span> (valeur de $ x $ lorsque $ z(t) = 0 $).'}
			</p>
		</div>

		<!-- II. Champ électrique uniforme -->
		<div>
			<h2 class="text-xl text-red-700">II. Champ électrique uniforme</h2>
			<p>
				- De manière similaire, dans un champ électrique uniforme {@html '$ \\vec{E} $'}, on
				applique :
			</p>
			<p class="fluov text-xl">{@html equations.eq2}</p>
		</div>

		<!-- III. Aspect énergétique -->
		<div>
			<h2 class="text-xl text-red-700">III. Aspect énergétique</h2>
			<p>- Théorème de l’énergie cinétique :</p>
			<p class="fluov text-xl">{@html equations.eq3}</p>
			<p>- Théorème de l’énergie mécanique :</p>
			<p class="fluov text-xl">{@html equations.eq4}</p>
			<p>
				- Si les forces non conservatives sont absentes (ex : frottements),
				<span class="fluo">l’énergie mécanique est conservée</span> : {@html '$ E_m = \\text{constante} $'}.
			</p>
		</div>
	</div>
</McSection>
