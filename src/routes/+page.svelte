<script>
    import Gallery from '$lib/Gallery.svelte'
    import { Button } from 'flowbite-svelte';
    import images from "$lib/data.json";
</script>


<Gallery items={images} class="gap-4 grid-cols-2 md:grid-cols-6" />