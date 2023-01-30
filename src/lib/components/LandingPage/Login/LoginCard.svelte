<script lang="ts">
	import codeCrowSingleLogo from '$lib/assets/images/logo/logo-single.svg'

	import DiscordWhiteIcon from '$lib/assets/images/login/discord-white-icon.svg'
	import GoogleIcon from '$lib/assets/images/login/google-icon.svg'
	import GithubIcon from '$lib/assets/images/login/github-icon.svg'

	import Logo from '$lib/components/LandingPage/Logo.svelte'
	import LinkPrimaryButton from '$lib/components/LandingPage/Button/LinkPrimaryButton.svelte'

	export let isOpenLoginDialogProp: any //onClickDismisDialogProp: any         on:click={onClickDismisDialogProp}
</script>

<div class="modal z-[500]" class:modal-open={isOpenLoginDialogProp}>
	<div
		class="modal-box rounded-lg bg-white w-[420px] z-[1000] scrollbar-thin scrollbar-thumb-[#25252A] scrollbar-track-[#AEAEAE] scrollbar-thumb-rounded">
		<div class="relative translate-x-0 p-2 justify-center items-center">
			<Logo
				imageSource={codeCrowSingleLogo}
				width="w-[60px] mx-auto justify-center items-center mb-7"
				logoLink="/" />
			<div class="flex flex-col gap-6">
				<LinkPrimaryButton
					title="Log in with Discord"
					link="http://localhost:8787/auth/discord"
					bgColor="bg-[#5765f1] hover:bg-[#5765f1]"
					border="border-1 border-[#5765f1] hover:border-[#5765f1]"
					optionalClass="normal-case text-base py-4 rounded-lg text-left"
					startIconClass="mr-[60px] -ml-[70px]"
					startIcon={DiscordWhiteIcon}
					targetBlank={false} />
				<LinkPrimaryButton
					title="Log in with Google"
					link="http://localhost:8787/auth/google"
					bgColor="bg-[#EEEEEE] hover:bg-[#EEEEEE]"
					border="border-1 border-[#000000] hover:border-[#000000]"
					optionalClass="normal-case text-[#25252A] text-base py-4 rounded-lg"
					startIconClass="mr-[60px] -ml-[72px]"
					startIcon={GoogleIcon}
					targetBlank={false} />
				<LinkPrimaryButton
					title="Log in with GitHub"
					link="http://localhost:8787/auth/github"
					bgColor="bg-[#000000] hover:bg-[#000000]"
					border="border-1 border-[#000000] hover:border-[#000000]"
					optionalClass="normal-case text-base py-4 rounded-lg"
					startIconClass="mr-[60px] -ml-[70px]"
					startIcon={GithubIcon}
					targetBlank={false} />
				<p
					class="justify-center items-center text-[#434F59] text-[13px] leading-[18px] font-normal text-center mt-2">
					By using our platform, you confirm that you are atleast 18 years old and agree to
					<a href="/" target="_blank" class="text-[#007BFF]">all of our policies</a>
				</p>
			</div>
		</div>
	</div>
</div>
