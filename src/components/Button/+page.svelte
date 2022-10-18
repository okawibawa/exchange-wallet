<script lang='ts'>
  export let text: string;
</script>

<template>
  <div class='button__container'>
    <button class='button__container-button'>
      {text}
    </button>
  </div>
</template>

<style>
  .button__container {
    padding: 24px 16px;
    background-color: white;
  }

  .button__container-button {
    cursor: pointer;
    font-family: 'Mulish';
    width: 100%;
    border-radius: 40px;
    background-color: #fedd00;
    border: none;
    padding: 18px 0;
    font-size: 1.25rem;
    font-weight: 600;
  }
</style>