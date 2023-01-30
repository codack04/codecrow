<script lang="ts">
	export let imageSource: any, width: string, logoLink: string
</script>

<a class="" href={logoLink}>
	<img src={imageSource} class={width} alt="Logo" />
</a>
