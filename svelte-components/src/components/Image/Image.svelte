<script lang="ts">
    export let src: string;
    export let alt: string;

    import { onMount } from 'svelte';

    let loaded = false;
    let thisImage;

    onMount(() => {
        // onload is HTML event attribute
        // The onload property is activated when the object has finished loading.
        thisImage.onload = () => {
            loaded = true;
        }
        console.log(thisImage.onload);
    });
</script>

<style>
    img {
        height: 200px;
        opacity: 0;
        transition: opacity 1200ms ease-out;
    }
    img.loaded {
        opacity: 1;
    }
</style>

<img {src} {alt} class:loaded bind:this={thisImage} loading="lazy" />
