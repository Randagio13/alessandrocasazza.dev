<script>
  import { tweened } from 'svelte/motion'
  import { cubicOut } from 'svelte/easing'
  import { onMount } from 'svelte'
  export let value
  export let max = 100
  export let className
  export let duration = 400
  const progress = tweened(0, {
    duration,
    easing: cubicOut
  });
  onMount(() => {
    progress.set(value)
  })
</script>

<progress value={$progress} max={max} class={className} />
<p class="text-center text-base text-gray-700">{parseInt($progress)}%</p>