<script>
  import Header from '../../components/Header/+page.svelte'
  import ButtonFixedBottom from '../../components/ButtonFixedBottom/+page.svelte'
  
  const formatter = new Intl.NumberFormat('id-ID', {
    style: 'currency',
    currency: 'IDR',
    maximumFractionDigits: 0
  })
</script>

<template>
  <Header title='Penukaran Chaca Point' />
  
  <div class='util__padding'>
    <div class='exchange__info-description'>
      <p class='exchange__info-description-title'>Nilai Konversi</p>
      <p>1 Rupiah = 1 Chaca Point</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Saldo</p>
      <p>{formatter.format(80000)}</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Bonus</p>
      <p class='exchange__info-bonus'>+10.000 CP</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Total</p>
      <p class='exchange__info-total'>
        <img class='exchange__info-logo' src='/images/star-shiny.svg' alt='lambang cp' />
        80.000 CP
      </p>
    </div>
  </div>
  
  <ButtonFixedBottom text='Kirim' />
</template>

<style>
  .util__padding {
    padding: 0 1rem;
  }

  .exchange__info-description {
    padding: 1rem;
    background-color: #F8F8F8;
    border: 1px solid #DBDBDB;
    border-radius: 12px;
    margin-bottom: 24px;
  }
  
  .exchange__info-description-title {
    font-weight: 600;
    margin-bottom: 1rem;
  }

  .exchange__info {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 1rem 0;
  }
  
  .exchange__info:not(:last-child) {
    border-bottom: 1px solid lightgrey;
  }
  
  .exchange__info-label {
    font-weight: 600;
  }
  
  .exchange__info-bonus {
    font-weight: 600;
    color: #FE9C00;
  }
  
  .exchange__info-total {
    display: flex;
    align-items: center;
    font-size: 34px;
    font-weight: 700;
    color: #FE9C00;
  }
  
  .exchange__info-logo {
    width: 42px;
    margin-right: 8px;
  }
</style>