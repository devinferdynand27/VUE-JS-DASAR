<template>

<h1>Biodata {{ nama    }} </h1>
  <div>
     <span> Nama : {{nama }}</span> <br>
     <span> Tanggal Lahir : {{tanggal_lahir }}</span> <br> 
     <span> Jenis Kelamin  : {{jk }}</span> <br>
     <span> Agama : {{agama }}</span> <br>
     <span> Alamat : {{alamat }}</span> <br>
      <span>{{pesan}}</span>
  </div>
<br>

</template>

<script>
   export default {
    props: ['nama', 'umur','tanggal_lahir','jk','agama','alamat'],
       data() {
          return {
             pesan: ' Hallo nama saya : ' + this.nama
      };
    }
}
</script>
