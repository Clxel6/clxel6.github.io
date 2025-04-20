<section {...$$restProps}>
	<slot {...$$restProps}/>
</section>

<style>
	section {
		border: 2px solid #bbb;
		background-color: #fcfcfcb8;
		box-shadow:
			inset -2px -2px #0000000f,
			inset 2px 2px #ffffff0d;
		padding: 12px;
	}
</style>
