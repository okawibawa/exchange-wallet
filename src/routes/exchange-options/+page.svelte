<script>
  import Header from '../../components/Header/+page.svelte'
  import CreditTitle from '../../components/CreditTitle/+page.svelte'
</script>

<template>
  <Header title='Penukaran Saldo Chaca'/>
  
  <div class='util__padding'>
    <CreditTitle label='Saldoku' amount={80000} />
    
    <h2 class='exchange__label'>Pilih Penukaran</h2>
    
    <div class='exchange__button-container'>
      <button class='exchange__button'>Chaca Point <span class='exchange__button-pill'>+10.000 CP</span></button>
      <img class='exchange__button-icon' src='/images/arrow-forward.svg' alt='arrow forward' />
    </div>

    <div class='exchange__button-container'>
      <button class='exchange__button'>Wallet Dana</button>
      <img class='exchange__button-icon' src='/images/arrow-forward.svg' alt='arrow forward' />
    </div>
  </div>
</template>

<style>  
  .util__padding {
    padding: 0 1rem;
  }
  
  .exchange__label {
    font-size: 16px;
    font-weight: normal;
    margin-bottom: 12px;
    margin-top: 32px;
  }
  
  .exchange__button-container {
    position: relative;
  }
  
  .exchange__button-container:nth-child(even) {
    margin-bottom: 24px;  
  }
  
  .exchange__button {
    cursor: pointer;
    font-family: 'Mulish';
    text-align: left;
    border-radius: 12px;
    border: 1px solid black;
    background-color: white;
    width: 100%;
    padding: 28px 16px;
    font-size: 18px;
    font-weight: 600;
  }
  
  .exchange__button-icon {
    position: absolute;
    top: 50%;
    right: 8px;
    transform: translateY(-50%);
    width: 24px;
    height: 24px;
  }
  
  .exchange__button-pill {
    background-color: #FE9C00;
    font-size: 12px;
    font-weight: 600px;
    padding: 4px 8px;
    margin-left: 8px;
    border-radius: 8px;
  }
</style>