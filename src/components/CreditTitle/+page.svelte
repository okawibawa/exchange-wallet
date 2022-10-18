<script lang='ts'>
  const formatter = new Intl.NumberFormat('id-ID', {
    style: 'currency',
    currency: 'IDR',
    maximumFractionDigits: 0
  })
  
  export let label: string;
  export let amount: number;
</script>

<template>
  <h2 class='credit__label'>{label}</h2>
  <p class='credit__amount'>
    <img class='credit__logo' src='/images/lambang-dana.png' alt='lambang dana' />
    {formatter.format(amount)}
  </p>
</template>

<style>
  .credit__label {
    font-size: 16px;
    font-weight: normal; 
    margin-bottom: 12px;
  }
  
  .credit__amount {
    display: flex;
    align-items: center;
    font-size: 34px;
    font-weight: 700;
  }
  
  .credit__logo {
    margin-right: 12px;
    width: 42px;
  }
</style>