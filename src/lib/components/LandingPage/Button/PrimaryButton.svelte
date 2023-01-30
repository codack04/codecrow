<script lang="ts">
	import Button from '$lib/components/LandingPage/Button/Button.svelte'

	export let title: string,
		onClick: any,
		bgColor: string,
		border: string,
		startIcon = '',
		endIcon = '',
		optionalClass = '',
		startIconClass = '',
		endIconClass = ''
</script>

<Button
	{title}
	{onClick}
	{border}
	{startIcon}
	{endIcon}
	{startIconClass}
	{endIconClass}
	addClass="btn gap-2 px-6 py-2 rounded text-white font-medium text-[13px] leading-[18px] tracking-[0.35px] {bgColor} {optionalClass}" />
