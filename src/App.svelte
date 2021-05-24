<script lang="ts">
  let page = 'index';
  import Gallery from './Gallery.svelte';
  import Image from './Image.svelte';
  import PartsList from './PartsList.svelte';
</script>

<main>
  <h1>Albin Stratus no 38 Serenity</h1>
  <nav>
    <button
      class={page === 'index' ? 'active' : ''}
      on:click={() => (page = 'index')}>Hem</button
    >
    <button
      class={page === 'gallery' ? 'active' : ''}
      on:click={() => (page = 'gallery')}>Bilder</button
    >
    <button
      class={page === 'partsList' ? 'active' : ''}
      on:click={() => (page = 'partsList')}>Utrustningslista</button
    >
  </nav>
  {#if page === 'index'}
    <section>
      <p>
        Nu säljer vi vår fina Albin Stratus som vi vårdat sen 2006. Vintern 2007
        hade vi henne inomhus för större uppgradering och epoxibehandling.
        Mycket är nytt de senaste åren bland annat Motor Volvo Penta D1-30,
        Självslående fock och rullgennacker (Code 1) och Peke med kastettstege.
        Båten har inte teakdäck. Övrigt se utrustningslista
      </p>
      <p>
        Med Code1 seglar man om båtar som går för motor i 3m/s. Mycket
        lätthanterad i både lätt och hård vind allt neddraget till sittbrunn
        samt singel rev bom
      </p>
      <p>
        Stort djupt roder med fenköl gör båten lättseglad och med fantastisk
        manöverförmåga i hamn med 3 bladig foldingpropeller.
      </p>
      <p>
        Med en riktigt rymlig sittbrunn finns gott om plats för familj och
        vänner. Invändigt finns 7 kojer och gott om stuvutrymmen för
        semesterseglingen.
      </p>
      <p>
        Hon står på land i båthus klar för sjösättning. Naturligtvis ingår
        sjösättning och påmastning. Båtplats finns för sommaren 2021 i Västerås.
        Båthus kan hyras vintern 21/22
      </p>
    </section>

    <Image image="outside5" w={1000} h={667} />
  {:else if page === 'partsList'}
    <section>
      <PartsList />
    </section>
  {:else if page === 'gallery'}
    <Gallery />
  {/if}
</main>

<style>
  main {
    display: grid;
    justify-items: center;
  }
  h1 {
    text-align: center;
  }
  nav {
    display: grid;
    position: sticky;
    background-color: rgb(40, 44, 52);
    grid-template-columns: 1fr 1fr 1fr;
    align-items: end;
    top: 0;
    width: 100%;
  }
  button {
    padding: 1rem;
    color: white;
    font-size: 1em;
    background: #aaa;
    cursor: pointer;
    border-radius: none;
    border: none;
  }

  button:hover {
    background: #999;
  }
  button.active {
    background: #0486a9;
  }
  button.active:hover {
    background: #037898;
  }
  section {
    padding: 8px;
    max-width: 700px;
  }
</style>
