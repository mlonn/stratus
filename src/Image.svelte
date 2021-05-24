<!-- svelte-ignore a11y-missing-attribute -->
<script lang="ts">
  export let image: string;
  const base = 'https://res.cloudinary.com/dzf3v5esf/image/upload';
  const cloudinaryId = 'v1621842386/Serenity';
  const url = `${base}/${cloudinaryId}/${image}.jpg`;
  const thumbnail = `${base}/h_250,c_scale/${cloudinaryId}/${image}.jpg`;
</script>

<a data-src={url} data-sub-html="<div></div>">
  <img class="img-responsive" alt={image} src={thumbnail} />
</a>

<style>
  a {
    margin-right: 4px;
    margin-bottom: 4px;
  }
  img {
    display: block;
  }
</style>
