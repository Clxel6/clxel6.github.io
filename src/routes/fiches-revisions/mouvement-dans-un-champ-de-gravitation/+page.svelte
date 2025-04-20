<script>
	import McSection from '$lib/UI/McSection.svelte';

	const equations = {
		eq1: `$$\\vec{F}_{B/A} = -\\vec{F}_{A/B} = G \\cdot \\frac{m_A \\cdot m_B}{r_{AB}^2} \\cdot \\vec{u}$$`,
		eq2: `$$\\mathcal{\\vec{G}} = -G \\cdot \\frac{m_A}{r_{AB}^2} \\cdot \\vec{u}$$`,
		eq3: `$$\\frac{T_p^2}{a^3} = \\frac{4\\pi^2}{G \\cdot M} = \\text{constante}$$`
	};
</script>

<McSection>
	<div class="flex flex-col gap-8">
		<!-- I. Rappels -->
		<div>
			<h2 class="text-xl text-red-700">I. Rappels</h2>
			<img src="/gravitation.png" alt="Gravitation" class="w-full" />
			<p>
				- La force gravitationnelle entre deux corps $ A $ et $ B $ est donnée par la loi
				universelle de Newton :
			</p>
			<p class="fluov text-xl">{@html equations.eq1}</p>
			<p>- Le champ de gravitation associé à une masse $ m_A $ s'écrit :</p>
			<p class="fluov text-xl">{@html equations.eq2}</p>
            <p>avec $ G $ la constante gravitationelle.</p>
			<p>
				- Dans le repère de Frenet, le vecteur unitaire {@html '$ \\vec{u} $'} est égal au vecteur normal
				{@html '$ \\vec{N} $'}.
			</p>
			<p>
				- En appliquant la 2<sup>e</sup> loi de Newton et la formule de l'accélération dans ce
				repère, on peut relier $ m_A $, $ v_A $, {@html '$ r_{AB} $'}, etc.
			</p>
		</div>

		<!-- II. Lois de Kepler -->
		<div>
			<h2 class="text-xl text-red-700">II. Lois de Kepler</h2>

			<p>
				1) <span class="fluo">Loi des orbites</span> : la trajectoire est une ellipse avec le centre
				de l'astre attracteur comme l'un des foyers. <br />
				2) <span class="fluo">Loi des aires</span> : l'aire balayée par le segment reliant les deux
				astres est constante pour des durées égales. <br />
                <img src="/kepler.jpg" alt="Kepler" class="w-full" />
				3) <span class="fluo">Loi des périodes</span> : la période $ T_p $ de révolution est liée au
				demi-grand axe $ a $ de l'ellipse par :
			</p>
			<p class="fluov text-xl">{@html equations.eq3}</p>
            <p>avec $ M $ la masse de l'astre attracteur.</p>
		</div>
	</div>
</McSection>
