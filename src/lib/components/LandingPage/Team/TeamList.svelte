<script lang="ts">
	import TeamMember from '$lib/components/LandingPage/Team/TeamMember.svelte'

	import teamMember1 from '$lib/assets/images/team/team-member-1.png'
	import teamMember2 from '$lib/assets/images/team/team-member-2.png'
	import teamMember3 from '$lib/assets/images/team/team-member-3.png'
	import teamMember4 from '$lib/assets/images/team/team-member-4.png'
	import teamMember5 from '$lib/assets/images/team/team-member-5.png'
	import teamMember6 from '$lib/assets/images/team/team-member-6.png'
	import teamMember7 from '$lib/assets/images/team/team-member-7.png'
	import teamMember8 from '$lib/assets/images/team/team-member-8.png'
	import teamMember9 from '$lib/assets/images/team/team-member-9.png'
	import teamMember10 from '$lib/assets/images/team/team-member-10.webp'

	const teamList = [
		{ name: 'G4g4n', position: 'Founder, CEO, Developer', avatar: teamMember1 },
		{ name: 'Ryan', position: 'COO, Project Manager', avatar: teamMember2 },
		{ name: 'Xaq', position: 'CMO, Digital Warlock, Growth Hacker', avatar: teamMember3 },
		{ name: 'Simmi', position: 'Talent Acquisition Specialist', avatar: teamMember4 },
		{ name: 'ILONG4KOMBAT', position: 'Game Consultant, QA', avatar: teamMember5 },
		{ name: 'SOLAIRE', position: 'Game Consultant, Discord Management', avatar: teamMember6 },
		{ name: 'ENRGYNVRDIES', position: 'Game Consultant, Visionary', avatar: teamMember7 },
		{ name: 'DAR', position: 'Market Analyst', avatar: teamMember8 },
		{ name: 'ULTRA2X', position: 'Quality Assurance Tester', avatar: teamMember9 },
		{
			name: 'Outsourced Contractors',
			position: 'Blockchain, web, Mobile developers',
			avatar: teamMember10
		}
	]
</script>

<div class="grid gap-4 md:gap-6 grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
	{#each teamList as member}
		<TeamMember name={member.name} position={member.position} avatar={member.avatar} />
	{/each}
</div>
