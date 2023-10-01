<script lang="ts">
	export let title: string;
	export let place: string;
	export let date_range: string;
</script>

<div>
	<span style="color: grey;" class="font-medium">{title}</span>
	<span class="flex flex-row justify-between">
		<strong>{place}</strong>
		<i>{date_range}</i>
	</span>
	<slot><!-- optional fallback --></slot>
</div>

<style>
</style>
