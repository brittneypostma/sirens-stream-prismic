<script>
	import { PrismicImage, PrismicRichText } from '@prismicio/svelte';

	/** @type {import("@prismicio/client").Content.MagicalSliceSlice} */
	export let slice;
</script>

<section data-slice-type={slice.slice_type} data-slice-variation={slice.variation}>
	<PrismicRichText field={slice.primary.rich_text} />
	<PrismicImage field={slice.primary.image} />
</section>

<style>
	section :global(img) {
		width: 200px;
		height: 200px;
	}
</style>
