<script lang="ts">
	import LinkButton from '$lib/components/LandingPage/Button/LinkButton.svelte'

	export let title: string,
		link: string,
		bgColor: string,
		border: string,
		startIcon = '',
		endIcon = '',
		optionalClass = '',
		startIconClass = '',
		endIconClass = '',
		targetBlank: boolean
</script>

<LinkButton
	{title}
	{link}
	{targetBlank}
	{border}
	{startIcon}
	{endIcon}
	{startIconClass}
	{endIconClass}
	addClass="btn gap-2 px-6 py-2 rounded text-white font-medium text-[13px] leading-[18px] tracking-[0.35px] {bgColor} {optionalClass}" />
