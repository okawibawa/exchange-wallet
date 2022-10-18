<script>
  import { page } from '$app/stores'
  import ButtonFixedBottom from '../../components/ButtonFixedBottom/+page.svelte'
  import Header from '../../components/Header/+page.svelte'
  import { browser } from '$app/environment'
  
  const urlParams = $page.url.pathname
  const removesUrlSlash = urlParams.replace('/', '')
  
  if (browser) {
    localStorage.setItem('token', removesUrlSlash)
  }
</script>

<template>
  <Header title='Penukaran Saldo Chaca' />

  <div class='util__padding'>
    <div class='app__container'>
      {#if removesUrlSlash}
        <h2>JWT: {removesUrlSlash}</h2>
      {/if}
  
      {#if !removesUrlSlash}
        <h2>No JWT provided.</h2>
      {/if}
    </div>
  </div>

  <ButtonFixedBottom text='Tukarkan sekarang!' />
</template>

<style>
  .util__padding {
    padding: 0 1rem;  
  }  

  .app__container {
    height: 100%;
  }
</style>
