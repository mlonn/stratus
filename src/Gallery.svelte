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

<div id="gallery-container">
  <Image image="outside1" />
  <Image image="outside2" />
  <Image image="outside3" />
  <Image image="outside4" />
  <Image image="outside5" />
  <Image image="outside6" />
  <Image image="outside7" />
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
  <Image image="webasto" />
</div>

<style>
  #gallery-container {
    max-width: 1280px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>
