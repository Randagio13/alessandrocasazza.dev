<script>
  let time = new Date()
  export let socialIcons = []
</script>
<div class="max-w-screen-xl mx-auto bg-gray-800 p-10">
  <div class="text-center mb-2">
    {#each socialIcons as { src, alt, path }}
       <a class="no-underline" href={path} target="_blank">
        <img class="w-10 h-10 inline-block" src={src} alt={alt} />
       </a>
    {/each}
  </div>
  <p class="text-gray-200 text-sm text-center">Copyright © {time.getFullYear()} - Made with 💖 and <img class="w-5 h-5 inline-block object-contain" src="sveltejsLogo.png" alt="Svelte JS" /> by myself.</p>
</div>