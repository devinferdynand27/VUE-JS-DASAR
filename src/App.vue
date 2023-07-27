<template>
  <div>
    <!-- <my-component umur="17" nama="DevinFerdynad " tanggal_lahir="02-12-2005" jk="Laki-Laki" agama="Islam" alamat="Bandung" ></my-component>
    <hobi hobi="Khayang"></hobi>   -->
    <!-- <Aritmatika angka1="1" angka2="2"> </Aritmatika> -->
      <!-- <Latihan nama="Ageng" makanan="Makroni Basah " qty="5"  ></Latihan> -->
      <CekumurComponent nama="devin" :umur='15'/>
      <PengulanganComponentVue/>
  </div>  
</template>

<script >
// import MyComponent from './MyComponent.vue';
// import Aritmatika from './Aritmatika.vue';
import CekumurComponent from './CekumurComponent.vue';
import PengulanganComponentVue from './PengulanganComponent.vue';
import Latihan from './Latihan.vue';
export default {
  components: { 
    // MyComponent,Hobi
    // Aritmatika
    Latihan,
    CekumurComponent,PengulanganComponentVue
  },
}
</script>



