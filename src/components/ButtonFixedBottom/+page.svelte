<script lang='ts'>
  export let text: string;
  export let isDisabled: boolean = false;
</script>

<template>
  <div class='button__container'>
    <button disabled={isDisabled} class={`button__container-button ${isDisabled && 'isDisabled'}`}>
      {text}
    </button>
  </div>
</template>

<style>
  .button__container {
    max-width: 600px;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 24px 16px;
    margin: auto;
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
  
  .isDisabled {
    background-color: #dbdbdb;
  }
</style>