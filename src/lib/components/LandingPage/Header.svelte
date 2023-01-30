<script lang="ts">
	import codeCrowLogo from '$lib/assets/images/logo/logo-white.svg'

	import Logo from '$lib/components/LandingPage/Logo.svelte'
	import Nav from '$lib/components/LandingPage/Nav/Nav.svelte'

	import { createEventDispatcher } from 'svelte'

	const dispatch = createEventDispatcher()

	//const openLoginDialog = () => dispatch('open', { isOpenLoginDialog: true })
</script>

<div class="w-full top-0 left-0 pt-10 absolute">
	<div class="relative z-10">
		<div
			class="container relative flex justify-between items-center space-x-4 xl:space-x-8 mx-auto">
			<div class="flex justify-start flex-grow items-center space-x-3 sm:space-x-8 lg:space-x-10">
				<Logo imageSource={codeCrowLogo} width="w-[194px]" logoLink="/" />
			</div>

			<div class="flex-shrink-0 flex items-center justify-end text-neutral-700 space-x-1">
				<Nav onClickLogin={() => dispatch('open', { isOpenLoginDialog: true })} />
			</div>
		</div>
	</div>
</div>
