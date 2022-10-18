<script>
  import Header from '../../components/Header/+page.svelte'
  import ButtonFixedBottom from '../../components/ButtonFixedBottom/+page.svelte'
  
  const formatter = new Intl.NumberFormat('id-ID',{
    style: 'currency',
    currency: 'IDR',
    maximumFractionDigits: 0
  })
</script>

<template>
  <Header title='Penukaran E-wallet' />
  
  <div class='util__padding'>
    <div class='exchange__info'>
      <p class='exchange__info-label'>Transaksi ID</p>
      <p class='exchange__info-id'>DNA38943</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Status</p>
      <p class='exchange__info-status success'>Proses</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Jumlah Penarikan</p>
      <p class='exchange__info-amount'>{formatter.format(80000)}</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Tujuan Penarikan</p>
      <p>DANA</p>
    </div>

    <div class='exchange__info'>
      <p class='exchange__info-label'>Tanggal Penarikan</p>
      <p>{new Date('2011-10-05T14:48:00.000Z').toLocaleString('default', { dateStyle: 'short', timeStyle: 'short', hour12: false })}</p>
    </div>
    
    <p class='exchange__info-description-process'>Mohon untuk menunggu proses penarikan maksimal 3 x 24 jam pada hari kerja, terima kasih.</p>

    <div class='exchange__info-description-failed'>
      <p class='exchange__info-description-failed-title'>Pesan:</p>
      <p>Nomor Dana yang Anda masukkan terkena limit. Silahkan kirim email ke info@chaca.io untuk mengganti nomor Dana Anda.</p>
    </div>
  </div>
  
  <ButtonFixedBottom text='Laporkan Masalah' />
</template>

<style>
  .util__padding {
    padding: 0 1rem;
    padding-bottom: calc(109.5px + 1rem);
  }
  
  .exchange__info {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid lightgrey;
    padding: 1rem 0;
  }
  
  .exchange__info-label, .exchange__info-id, .exchange__info-amount {
    font-weight: 600;
  }
  
  .exchange__info-amount {
    color: #1abd00
  }
  
  .exchange__info-status {
    font-weight: 600;
  }
  
  .failed {
    color: #AD0000;
  }
  
  .process {
    color: blue;
  }
  
  .success {
    color: #1BAD00;
  }
  
  .exchange__info-description-process {
    margin-top: 24px;
    margin-bottom: 32px;
  }
  
  .exchange__info-description-failed {
    padding: 1rem;
    background-color: #F8F8F8;
    border: 1px solid #DBDBDB;
    border-radius: 12px;
  }
  
  .exchange__info-description-failed-title {
    font-weight: 600;
    margin-bottom: 1rem;
  }
</style>