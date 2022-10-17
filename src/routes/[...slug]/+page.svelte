<script>
  import { page } from '$app/stores'
  
  const urlParams = $page.url.pathname
  const removesUrlSlash = urlParams.replace('/', '')
</script>

<template>
  {#if removesUrlSlash}
    <h2>JWT: {removesUrlSlash}</h2>
  {/if}
  
  {#if !removesUrlSlash}
    <h2>No JWT provided.</h2>
  {/if}
</template>
