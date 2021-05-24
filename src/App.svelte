<script lang="ts">
  import lightGallery from 'lightgallery';
  import lgThumbnail from 'lightgallery/plugins/thumbnail';
  import lgZoom from 'lightgallery/plugins/zoom';
  import { onMount } from 'svelte';
  import Image from './Image.svelte';

  onMount(() => {
    lightGallery(document.getElementById('gallery-container'), {
      speed: 500,
      plugins: [lgZoom, lgThumbnail],
    });
  });
</script>

<main>
  <h1>Albin Stratus</h1>
  <div id="gallery-container">
    <Image image="main1" />
    <Image image="main2" />
    <Image image="kitchen1" />
    <Image image="kitchen2" />
    <Image image="kitchen3" />
    <Image image="back" />
    <Image image="front1" />
    <Image image="front2" />
    <Image image="bathroom" />
    <Image image="batteries" />
    <Image image="battery_charge" />
    <Image image="battery_voltage" />
  </div>
</main>

<style>
  main {
    display: grid;
    align-items: center;
    text-align: center;
    justify-content: center;
  }

  #gallery-container {
    max-width: 1280px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>
