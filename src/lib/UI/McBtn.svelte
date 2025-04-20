<script>
	export let link = '/';
	export let img = '';
	export let text = '';
</script>

<button {...$$restProps}>
	<a href={link}>
		{#if img}
			<img src={img} alt="" />
		{/if}
		{#if text}
			<span>{text}</span>
		{/if}
	</a>
</button>

<style>
	button {
		cursor: pointer;
		width: 100%;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
		text-align: center;
		border: 2px solid rgba(0, 0, 0, 0.4);
		font-size: 1em;
		font-weight: bold;
		transition-property:
			background-color, color, border-color, box-shadow, opacity, padding, margin;
		transition-duration: 0.1s;
	}

	button > * {
		width: calc(100% + 4px);
		height: calc(100% + 4px);
		margin: -2px;
		padding: 8px 10px 14px !important;
		display: flex;
		gap: 6px;
		text-align: center;
		align-items: center;
		justify-content: center;
		text-decoration: none;
		transition-property: padding, margin;
		transition-duration: 0.1s;
	}

	button img {
		max-height: 32px;
		max-width: 32px;
	}

	button::after {
		content: '';
		display: block;
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		z-index: 1;
		box-shadow:
			0 -6px 0 0 rgb(104, 104, 104) inset,
			2px 2px 0 0 rgba(178, 178, 178, 0.5) inset,
			-2px -8px 0 0 rgba(153, 153, 153, 0.5) inset;
		mix-blend-mode: hard-light;
		transition:
			0.1s background-color,
			box-shadow;
		pointer-events: none;
	}

	button:hover::after {
		background-color: #ffffff1a;
	}

	button:active {
		margin-top: 6px;
	}

	button:active > * {
		padding: 14px 10px 8px !important;
		margin-top: -8px;
		height: calc(100% + 10px);
	}

	button:active::after {
		box-shadow:
			2px 2px 0 0 rgba(178, 178, 178, 0.5) inset,
			-2px -2px 0 0 rgba(153, 153, 153, 0.5) inset;
		background-color: #0000001a;
	}
</style>
