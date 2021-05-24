<!-- svelte-ignore a11y-missing-attribute -->
<script lang="ts">
  export let image: string;
  export let w: string | number = 300;
  export let h: string | number = 200;
  const base = 'https://res.cloudinary.com/dzf3v5esf/image/upload/q_auto';
  const cloudinaryId = 'v1621842384/Serenity';
  const url = `${base}/${cloudinaryId}/${image}.jpg`;
  const thumbnail = `${base}/w_${w},h_${h},c_fill/${cloudinaryId}/${image}.jpg`;
</script>

<a data-src={url} data-sub-html="<div></div>">
  <img class="img-responsive" alt={image} src={thumbnail} />
</a>

<style>
  a {
    margin-right: 4px;
    margin-bottom: 4px;
    max-width: 100%;
  }
  img {
    max-width: 100%;
    display: block;
  }
</style>
