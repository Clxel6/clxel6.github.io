<script>
	import McSection from '$lib/UI/McSection.svelte';

	const equations = {
		eq1: `$$I\\,(\\text{W·m}^{-2}) = \\frac{P\\,(\\text{W})}{S\\,(\\text{m}^2)}$$`,
		eq2: `$$L\\,(\\text{dB}) = 10 \\cdot \\log\\left(\\frac{I\\,(\\text{W·m}^{-2})}{I_0}\\right)$$`,
		eq3: `$$f_{reçue}\\,(\\text{Hz}) = f_e \\,(\\text{Hz}) \\cdot \\frac{c\\,(\\text{m·s}^{-1})}{c\\,(\\text{m·s}^{-1}) + v\\,(\\text{m·s}^{-1})}$$`,
		eq4: `$$f_{reçue}\\,(\\text{Hz}) = f_e \\,(\\text{Hz}) \\cdot \\frac{c\\,(\\text{m·s}^{-1})}{c\\,(\\text{m·s}^{-1}) - v\\,(\\text{m·s}^{-1})}$$`
	};
</script>

<McSection>
	<div class="flex flex-col gap-8">
		<!-- Intensité sonore -->
		<div>
			<h2 class="text-xl text-red-700">I. Intensité sonore</h2>
			<p>
				- Un son émet <span class="fluo">une puissance $ P $ dans toutes les directions</span>.
				<br />
				- Ce son se répartit sur <span class="fluo">une surface $ S $ d'une sphère</span>. <br />
				- L'intensité de ce son suit la formule :
			</p>
			<p class="fluov text-xl">{@html equations.eq1}</p>
			<p>
				- L'intensité sonore est comprise entre {@html '$ I_0 = 1,0 \\times 10^{-12} \\;\\text{W·m}^{-2} $'}
				et {@html '$ I_{douleur} = 1,0 \\;\\text{W·m}^{-2} $'}. <br />
				- Pour faciliter les études, on utilise le niveau d’intensité sonore.
			</p>
		</div>

		<!-- Niveau d'intensité sonore -->
		<div>
			<h2 class="text-xl text-red-700">II. Niveau d'intensité sonore</h2>
			<p class="fluov text-xl">{@html equations.eq2}</p>
			<p>
				- <span class="fluor">ATTENTION</span> Les niveaux d’intensité
				<span class="fluo">ne s’additionnent pas</span> (contrairement aux intensités).
			</p>
		</div>

		<!-- Atténuation -->
		<div>
			<h2 class="text-xl text-red-700">III. Atténuation</h2>
			<p>
				- Correspond à une diminution du niveau sonore. <br />
				<span class="fluo">Atténuation géométrique</span> (éloignement de la source) : {@html '$ A = L_{proche} - L_{éloigné} $'}
				<br />
				<span class="fluo">Atténuation par absorbtion</span> (présence d’une paroi) : {@html '$ A = L_{incident} - L_{transmis} $'}
			</p>
		</div>

		<!-- Effet Doppler -->
		<div>
			<h2 class="text-xl text-red-700">IV. Effet Doppler</h2>
			<p>
				- <span class="fluo">Changement de la fréquence reçue</span> par un observateur mobile (ou
				source mobile). <br />
				Si la source s'éloigne :
			</p>
			<p class="fluov text-xl">{@html equations.eq3}</p>
			<p>Si la source se rapproche :</p>
			<p class="fluov text-xl">{@html equations.eq4}</p>
			<p>
				avec $ f_e $ la fréquence émise, $ c $ la vitesse de l'onde et $ v $ la vitesse de la
				source.
			</p>
			<img src="/effet-doppler.jpg" alt="" />
		</div>
	</div>
</McSection>

<!-- 
<section class="mc-section m-2">
    <div class="flex flex-col gap-8">
        <div>
            <h2 class="text-3xl text-red-700">I. Intensité sonore</h2>
            <p>
                - Un son émet <span class="fluo">une puissance \( P \) dans toutes les directions</span>. <br />
                - Ce son se répartit sur <span class="fluo">une surface \( S \) d'une sphère</span>. <br />
                - L'intensité de ce son suit la formule :
            </p>
            <MathJax content={equations.eq1} />
            <p>
                - L’intensité sonore est comprise entre 
                <MathJax content="\( I_0 = 1.0 \times 10^{-12} \text{W·m}^{-2} \\)" /> <br />
                - Pour faciliter les études, on utilise le niveau d’intensité sonore.
            </p>
        </div>

        <div>
            <h2 class="text-3xl text-red-700">II. Niveau d’intensité sonore</h2>
            <p>
                Le niveau d’intensité sonore est donné par la formule suivante :
            </p>
            <MathJax content={equations.eq2} />
            <p>
                - <span class="fluor">ATTENTION</span> : Les niveaux d’intensité
                <span class="fluo">ne s’additionnent pas</span> (contrairement aux intensités).
            </p>
        </div>

        <div>
            <h2 class="text-3xl text-red-700">III. Atténuation</h2>
            <p>- Correspond à une diminution du niveau sonore.</p>
            <p>
                <span class="fluo">Atténuation géométrique</span> (éloignement de la source) :
                <MathJax content={equations.eq3} />
            </p>
            <p>
                <span class="fluo">Atténuation par absorption</span> (présence d’une paroi) :
                <MathJax content={equations.eq4} />
            </p>
        </div>

        <div>
            <h2 class="text-3xl text-red-700">IV. Effet Doppler</h2>
            <p>
                - <span class="fluo">Changement de la fréquence \( f_e \) reçue</span>
                par un observateur mobile (ou source mobile).
            </p>
            <p>Si la source s’éloigne :</p>
            <MathJax content={equations.eq5} />
            <p>Si la source se rapproche :</p>
            <MathJax content={equations.eq6} />
            <p>avec \( c \) la vitesse de l’onde et \( v \) celle de l’émetteur.</p>
            <img src="/effet-doppler.jpg" alt="Effet Doppler" />
        </div>
    </div>
</section> -->
