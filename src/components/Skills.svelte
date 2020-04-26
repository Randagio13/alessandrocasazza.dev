<script>
  import Progress from './Progress.svelte'
  export let logotypes = []
</script>

<div class="mx-auto w-4/5 flex flex-wrap justify-center my-10">
  {#each logotypes as { src, alt, path, value, type }}
    <div class="flex flex-col mx-10 my-5">
      <img class="w-24 h-24 mx-auto object-contain object-center" src={src} alt={alt} />
      <Progress className="mx-auto w-32 m-2" {value} duration={1000} />
    </div>
  {/each}
</div>