<script lang="ts">
  import lightGallery from 'lightgallery';
  import lgZoom from 'lightgallery/plugins/zoom';
  import { onMount } from 'svelte';
  import Image from './Image.svelte';

  const images = [
    'outside1',
    'outside2',
    'outside3',
    'outside4',
    'outside5',
    'outside6',
    'outside7',
    'outside8',
    'sail',
    'rainbow',
    'flags',
    'spinnaker',
    'cockpit1',
    'cockpit2',
    'main1',
    'main2',
    'kitchen1',
    'kitchen2',
    'back',
    'front1',
    'front2',
    'bathroom',
    'map',
    'engine1',
    'engine2',
    'propeller',
    'engine',
    'Konverter',
    'batteries',
    'battery_charge',
    'battery_voltage',
    'webasto',
    'blueprint',
  ];
  onMount(() => {
    lightGallery(document.getElementById('gallery-container'), {
      speed: 500,
      plugins: [lgZoom],
    });
  });
</script>

<div id="gallery-container">
  {#each images as image}
    <Image clickable {image} />
  {/each}
</div>

<style>
  #gallery-container {
    margin: 24px 0;
    max-width: 1280px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>
