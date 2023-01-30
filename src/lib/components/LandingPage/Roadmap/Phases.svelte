<script lang="ts">
	import PhaseCard from '$lib/components/LandingPage/Roadmap/PhaseCard.svelte'

	import reloadLogo from '$lib/assets/images/roadmap/Reload-logo.svg'
	import crossLogo from '$lib/assets/images/roadmap/cross.svg'
	import solanaLogo from '$lib/assets/images/roadmap/solana-sol-logo.svg'

	import playStoreLogo from '$lib/assets/images/roadmap/Google-Play.svg'
	import appStoreLogo from '$lib/assets/images/roadmap/App-Store.svg'

	const phases = {
		phaseOne: [
			'Build the community',
			'Collaborate with an animation studio for our MVP Heroes NFT animations',
			'Begin infinibuild development',
			'Allow 1 million viewers per channel',
			'Integrate User Profiles to allow users to establish their brand',
			'Partnership Announcements',
			[
				'Microsoft for Startups',
				'Cloudflare Startups',
				'Hatch by DigitalOcean',
				'MongoDB for Startups',
				'AWS Activate',
				'Twilio Startups',
				'Scrimba',
				'More coming soon'
			]
		],
		phaseTwo: [
			'Minting 10,000 Gen-0 MVP Heroes NFTs',
			'Collaborate with a game studio to begin MVP game development'
		],
		phaseThree: [
			'MVP Heroes benefits integration',
			'Recursion token integration',
			'Airdropping Recursion tokens to select streamers and MVP Heroes holders',
			'20% of all in-app profits will be reinvested into the liquidity pool',
			'Recursion tokens will be backed by a liquidity pool, will be tradable on a DEX, and can be used to:',
			[
				'purchase in-app features such has BUMP (bump up your channel to the top to get more visibility)',
				'purchase skins in MVP',
				'purchase merchandise from our market',
				'show your love and support by tipping users on a live-stream'
			]
		],
		phaseFour: ['Video recording, library, and responses integration'],
		phaseFive: [
			'Begin mobile app development',
			'Sending holders invites to Android app',
			'Sending holders invites to iOS app'
		]
	}
</script>

<PhaseCard title="Phase 1" headBgColorClass="bg-[#EC008C]" dotColorClass="after:bg-[#EC008C]">
	<div slot="cardContent">
		<ul class="list-disc">
			{#each phases.phaseOne.slice(0, 6) as item}
				<li>{item}</li>
			{/each}
		</ul>
		<ol class="list-decimal px-5">
			{#each phases.phaseOne[6] as item}
				<li>{item}</li>
			{/each}
		</ol>
	</div>
</PhaseCard>

<PhaseCard
	title="Phase 2"
	rightCard={true}
	headBgColorClass="bg-[#C8198B]"
	dotColorClass="after:bg-[#C8198B]">
	<ul class="list-disc" slot="cardContent">
		{#each phases.phaseTwo as item}
			<li>{item}</li>
		{/each}
	</ul>
</PhaseCard>

<PhaseCard title="Phase 3" headBgColorClass="bg-[#8A388A]" dotColorClass="after:bg-[#8A388A]">
	<div slot="cardContent">
		<ul class="list-disc">
			{#each phases.phaseThree.slice(0, 5) as item}
				<li>{item}</li>
			{/each}
		</ul>
		<ol class="list-decimal px-5">
			{#each phases.phaseThree[5] as item}
				<li>{item}</li>
			{/each}
		</ol>
	</div>
	<div class="flex flex-row" slot="extraContent">
		<img src={reloadLogo} class="w-20" alt="" />
		<img src={crossLogo} class="w-20 px-6" alt="" />
		<img src={solanaLogo} class="w-20" alt="" />
	</div>
</PhaseCard>

<PhaseCard
	title="Phase 4"
	rightCard={true}
	headBgColorClass="bg-[#4E3388]"
	dotColorClass="after:bg-[#4E3388]">
	<ul class="list-disc" slot="cardContent">
		{#each phases.phaseFour as item}
			<li>{item}</li>
		{/each}
	</ul>
</PhaseCard>

<PhaseCard title="Phase 5" headBgColorClass="bg-[#2B328C]" dotColorClass="after:bg-[#2B328C]">
	<ul class="list-disc" slot="cardContent">
		{#each phases.phaseFive as item}
			<li>{item}</li>
		{/each}
	</ul>
	<div class="flex flex-col gap-1 justify-center" slot="extraContent">
		<img src={playStoreLogo} class="w-40 h-14" alt="" />
		<img src={appStoreLogo} class="w-40 h-14" alt="" />
	</div>
</PhaseCard>
