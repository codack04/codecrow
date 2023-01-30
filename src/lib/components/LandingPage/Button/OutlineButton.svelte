<script lang="ts">
	import Button from '$lib/components/LandingPage/Button/Button.svelte'

	export let title: string,
		onClick: any,
		titleColor: string,
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
	{startIcon}
	{endIcon}
	{startIconClass}
	{endIconClass}
	{border}
	addClass="btn gap-2 px-6 py-2 rounded bg-transparent hover:bg-transparent font-medium text-[13px] leading-[18px] tracking-[0.35px] {titleColor} {optionalClass}" />
