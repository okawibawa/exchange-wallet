<script lang='ts'>
  export let title: string;
</script>

<template>
  <div class='util__padding'>
    <div class='header__container'>
      <img class='header__container-icon' src='/images/arrow-back-outline.svg' alt='back icon' />
      <h1 class='header__container-title'>{title}</h1>
    </div>
  </div>
  
  <div class='header__divider'></div>
</template>

<style>
  .util__padding {
    padding: 0 1rem;  
  }  
  
  .header__container {
    padding: 20px 0;
    display: flex;
    align-items: center;
  }
  
  .header__container-icon {
    width: 24px;
    height: 24px;
    margin-right: 32px;
  }
  
  .header__container-title {
    font-size: 18px;
  }
  
  .header__divider {
    width: 100%;
    height: 1px;
    background-color: lightgrey;
    margin-bottom: 24px;
  }
</style>