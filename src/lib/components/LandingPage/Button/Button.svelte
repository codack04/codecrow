<script lang="ts">
	export let title: string,
		onClick: any,
		border: string,
		startIcon = '',
		endIcon = '',
		addClass = '',
		startIconClass = '',
		endIconClass = ''
</script>

<button on:click={onClick} class="{border} {addClass}">
	<img src={startIcon} class={startIconClass} alt="" />
	{title}
	<img src={endIcon} class={endIconClass} alt="" />
</button>
