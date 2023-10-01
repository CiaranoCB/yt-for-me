<script>
    import Thumb from "$lib/thumb.svelte";
    import { onMount } from "svelte";
    let loading = true;
    onMount(() => {
        setTimeout(() => {
            // where the code runs for the timeout
            loading = false;
        }, 5000);
    })
</script>

<hi></hi>

<div class="flex subscription justify-between px-8 flex-wrap">
    <Thumb
    title = "BIG FOOT SIGHTINGS!!!"
    thumbnail = "Feet and Soil.jpeg"
    avatar = "photo2.jpeg"
    creator = "Johnny Boi098"
    views = ""
    loading={loading}
    id={1}
    />
    <Thumb
    title = "Grass and McDonald Sprite River!"
    thumbnail = "Grass and Water.jpeg"
    avatar = "photo2.jpeg"
    creator = "NoFurUser123"
    views = ""
    loading={loading}
    id={2}
    />
    <Thumb />
    <Thumb />



    <Thumb />
    <Thumb />
    <Thumb />
    <Thumb />



    <Thumb />
    <Thumb />
    <Thumb />
    <Thumb />
</div>

<style>
    .flex {
        padding-bottom: 4rem;
    }
</style>