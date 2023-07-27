<template>
<div>
        Nama : {{ datas.namaku }} <br>
        Makanan : {{ makanan }} <br>
        harga : {{ datas.hargas }}  <br>
        qty : {{ qty }} <br>
        Total Harga : {{ jumlah }} <br>
        Bayar : {{ datas.uangmasuk }}<br>
        Kembalian :  {{ kembalian }}
</div>

<br><br>

    <!-- contoh -->
<div>
    <span>{{datas.angka}}</span> <br>
    <button @click="tambah"> Tambah </button>
    <button @click="kurang"> Kurang </button>
</div>

   <!-- tugas -->
<div>
    <span>{{datas.namaku}}</span> <br>
    <button @click="setnama"> setnama </button>
</div>

</template>


<script>
  export default {
    props :['nama','makanan','qty'],
  
  data(){
    return{
        datas:{
        nama: this.nama,
        makanan: this.makanan,
        hargas: 5000,
        qty: this.qty,  
        uangmasuk : 100000,
        angka : 0,
        namaku : 'Nama aku siapa ya?'
    },
    }
  },

  methods:{
    tambah(){
        this.datas.angka++
    },
    kurang(){
        this.datas.angka--
    }, 
    setnama(){
        this.datas.namaku = "Devin Ferdynand Ganteng"
        // console.log('apa')
    }
  },

  computed:{
    jumlah(){
         return this.datas.hargas * this.datas.qty
    },
    kembalian(){
         return  this.datas.uangmasuk - this.jumlah 
    }
  }
}
</script>