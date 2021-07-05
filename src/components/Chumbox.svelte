<script>
  import Chumpiece from "./Chumpiece.svelte";
  import data from "../data/chum.csv";
  console.log(data);

  const width = 400;
  const height = 400;
</script>

<div class="chum-container">
  {#each data as d}
    <span class="chumpiece">
      <Chumpiece
        url="{d.image_url}"
        title="{d.title}"
        height="{height}"
        width="{width}"
      />
    </span>
  {/each}
</div>

<style>
  .chum-container {
    max-width: 90%;
    margin: 0 auto;
    display: grid;
    grid-gap: 10px;
    grid-template-columns: auto auto auto;
    /* display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between; */
  }

  .chumpiece {
    display: inline;
  }
</style>
