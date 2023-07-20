<script setup>
  import { ref } from 'vue';
  let head = "<h1>  namasaya candra</h1>"
  let nama = "namasaya devin"
  let message = "devin"
  let awal = 1
  let akhir = 0
  let size = '20px'
  let warna = "#FF0000"
  let number = 1
  let ok = 'YES'
  let contoh = ref('devinganteng')

  const items = [
    {
       nama: 'Devin',
       kelas: '11 Rpl 1', 
       alamat: 'bandung',
    }, 
    {
       nama: 'Devins',
       kelas: '11 Rpl 2', 
       alamat: 'bandung jawa',
    }, 
    ]
    function tampil(){
       contoh.value = contoh.value.split('').reverse().join('')
    }
</script>
<template>
  <div>

    <h1>  {{ contoh }}</h1>


     <input type="text" v-model="contoh">
      <p>{{ contoh }}</p>
      <span> {{ messege }}</span><br>
      <span v-html="head"></span>
      <span v-html="nama"> </span>
  
  </div>

  <div v-bind:style="{ fontSize: size , color : warna}">
     {{ nama }}
  </div>
  <br>


   <h1>{{ number + 1 }} {{ ok ? 'YES' : 'NO' }} </h1> <br>
   <!-- dijoin bisa di tambhkan angka / huruf -->
  <h1> Angka Tibalik  {{ ok.split('').reverse().join('') }}</h1> 
  <table border="1">
      <thead>
        <tr> 
          <th>No </th>
          <th>Nama </th>
          <th>kelas</th>
          <th>Alamat</th>
        </tr>
      </thead>
      <tbody>
          <tr v-for="item,index in items" :key="item">
            <td>{{index + 1 }}</td>
            <td>{{item.nama}}</td>
            <td>{{item.kelas}}</td>
            <td>{{item.alamat}}</td>
          </tr>
      </tbody>
  </table>
  <br><br>


  <a href="https://vuejs.org/guide/essentials/list.html#v-for">Dodumentasi</a>


  <!-- reversi button  -->
  <button v-on:click="tampil">Balikkan Pesan</button>

  

</template>
