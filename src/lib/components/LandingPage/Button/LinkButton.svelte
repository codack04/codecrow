<script lang="ts">
	export let title: string,
		link: string,
		border: string,
		startIcon = '',
		endIcon = '',
		addClass = '',
		startIconClass = '',
		endIconClass = '',
		targetBlank: boolean
</script>

<a
	href={link}
	class="{border} {addClass}"
	target={targetBlank == true ? '_blank' : ''}
	rel="noreferrer">
	<img src={startIcon} class={startIconClass} alt="" />
	{title}
	<img src={endIcon} class={endIconClass} alt="" />
</a>
