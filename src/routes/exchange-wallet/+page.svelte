<script lang='ts'>
  import Header from '../../components/Header/+page.svelte'
  import CreditTitle from '../../components/CreditTitle/+page.svelte'
  import ButtonFixedBottom from '../../components/ButtonFixedBottom/+page.svelte'
  
  import { danaNumber } from '../../stores/dana-store'
  
  let dana: number;
  let isDisabled: boolean;

  danaNumber.subscribe((value) => {
    dana =  value;
    
    if (!value) {
      isDisabled = true; 
    } else {
      isDisabled = false;
    }
  })
  
  const handleDanaNumberInput = (e: any) => {
    danaNumber.set(e.target.value)
  }    
</script>

<template>
  <Header title='Penukaran E-wallet' />
  
  <div class='util__padding'>
    <CreditTitle label='Jumlah Penarikan' amount={80000} />
    
    <h2 class='exchange__label'>Masukkan Nomor Dana</h2>
    
    <input
      class='exchange__input'
      placeholder='Nomor Dana'
      type='text'
      on:input={handleDanaNumberInput}
    />
  </div>
    
  <ButtonFixedBottom text='Kirim' isDisabled={isDisabled} />
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
  
  .exchange__input {
    display: block;
    font-family: 'Mulish';
    padding: 28px 16px;
    border-radius: 12px;
    background-color: white;
    border: 1px solid black;
    font-size: 18px;
    color: #767676;
    width: calc(100% - 34px);
  }
  
  .exchange__input:focus {
    border: 1px solid #fedd00;
    outline: 1px solid #fedd00;
  }
</style>
