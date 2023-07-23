<script>
	export let bgcolor = 'black';
</script>

<div
	class="flex flex-col text-center items-center"
	style="background-color: {bgcolor}; color: white;"
>
	<slot><!-- optional fallback --></slot>
</div>

<style>
	div {
		/* y x */
		padding: 20px 10px;
		text-align: left;
	}
</style>
