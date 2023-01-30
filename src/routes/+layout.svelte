<script lang="ts">
	import '$lib/assets/styles/tailwind-output.css'

	import Header from '$lib/components/LandingPage/Header.svelte'
	import Footer from '$lib/components/LandingPage/Footer.svelte'
	import LoginCard from '$lib/components/LandingPage/Login/LoginCard.svelte'

	import { classList } from 'svelte-body'

	// From Store
	import { isOpenLoginDialog } from '$lib/stores/store'
</script>

<svelte:head>
	<link
		href="https://fonts.googleapis.com/css?family=Montserrat:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i"
		rel="stylesheet" />
</svelte:head>

<svelte:body
	use:classList={$isOpenLoginDialog == true
		? 'overflow-hidden h-screen'
		: 'scrollbar-thin scrollbar-thumb-[#aeaeae] scrollbar-track-[#25252A] scrollbar-thumb-rounded'} />

<div>
	<Header on:open={(e) => isOpenLoginDialog.update(() => e.detail.isOpenLoginDialog)} />

	<slot />

	<Footer />
</div>

<LoginCard isOpenLoginDialogProp={$isOpenLoginDialog} />

<style global>
	:root {
		--color-default: #ffffff;
	}
	@media (prefers-color-scheme: dark) {
		:root {
			--my-color: #25252a;
		}
	}
	[data-theme='dark'] {
		--color-default: #25252a;
	}
	[data-theme='light'] {
		--my-color: #ffffff;
	}
	body {
		background-color: var(--color-default);
	}
</style>
