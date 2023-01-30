<script lang="ts">
	export let title: string,
		rightCard: boolean = false,
		headBgColorClass: string,
		dotColorClass: string
</script>

<li
	class="list-none relative flex justify-between  {rightCard == true
		? 'flex-row-reverse'
		: 'flex-row'}">
	<div class="flex flex-col drop-shadow-xl w-2/5">
		<div class="flex">
			{#if rightCard == true}
				<div
					class="flex w-[30px] {headBgColorClass} clip-path-roadmapCardRight rotate-180 h-auto mr-[-0.5px] z-[100]" />
				<div
					class="flex w-[465px] {headBgColorClass} text-white font-semibold text-base py-2 px-7 after:content-[''] after:rounded-full after:h-7 after:w-7 {dotColorClass} after:absolute after:left-[-28%] after:mt-[-2px] before:border-[#F8F8F8] before:h-0 before:w-[106px] before:border-t-2 before:border-dashed before:absolute before:left-[-22%] before:mt-[11.2px]">
					{title}
				</div>
			{:else}
				<div
					class="flex w-[465px] {headBgColorClass} text-white font-semibold text-base py-2 px-7 after:content-[''] after:rounded-full after:h-7 after:w-7 {dotColorClass} after:absolute after:left-[122%] after:mt-[-2px] before:border-[#F8F8F8] before:h-0 before:w-[106px] before:border-t-2 before:border-dashed before:absolute before:left-[100%] before:mt-[11.2px]">
					{title}
				</div>
				<div
					class="flex w-[30px] {headBgColorClass} clip-path-roadmapCardLeft h-auto ml-[-0.4px] z-[100]" />
			{/if}
		</div>

		<div
			class="flex w-[94%] bg-[#F8F8F8] text-[#444F58] font-normal text-sm rounded-b py-3 px-10 {rightCard ==
			true
				? 'ml-[6%]'
				: ''}">
			<slot name="cardContent" />
		</div>
	</div>
	<div class="flex align-middle text-center justify-center w-2/5">
		<slot name="extraContent" />
	</div>
</li>
