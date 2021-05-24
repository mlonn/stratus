<!-- svelte-ignore a11y-missing-attribute -->
<script lang="ts">
  export let image: string;
  export let clickable: boolean;
  export let w: number = 300;
  export let h: number = 200;

  const base = 'https://res.cloudinary.com/dzf3v5esf/image/upload/q_auto';
  const cloudinaryId = 'v1621842384/Serenity';
  const url = `${base}/${cloudinaryId}/${image}.jpg`;
  const thumbnail = `${base}/w_${Math.floor(w * 1.05)},h_${Math.floor(
    h * 1.05
  )},c_fill/${cloudinaryId}/${image}.jpg`;
</script>

<a data-src={url} data-sub-html="<div></div>" data-slide-name={image}>
  <img
    class={clickable ? 'clickable' : ''}
    style={`width:${w}; height:${h}`}
    alt={image}
    src={thumbnail}
  />
</a>

<style>
  a {
    margin-right: 4px;
    margin-bottom: 4px;
    max-width: 100%;
  }
  img {
    transition: all ease-in-out 0.2s;
    max-width: 100%;
    display: block;
  }
  img.clickable {
    cursor: pointer;
  }
  img.clickable:hover {
    transform: scale(1.05);
    transform: perspective(500px) rotateY(5deg);
    transform: perspective(500px) rotateX(5deg);
    border-radius: 5px;
    box-shadow: 0px 0px 15px 15px rgba(40, 44, 52, 0.8);
  }
</style>
