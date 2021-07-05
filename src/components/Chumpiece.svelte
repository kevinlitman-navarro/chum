<script>
  export let url;
  export let title;
  export let height;
  export let width;
</script>

<p class="title">{title}</p>
<img src="{url}" alt="{title}" heigth="{height}" width="{width}" />

<style>
  .title {
    font-weight: bold;
  }
</style>
