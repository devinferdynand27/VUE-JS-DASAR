 <script>
    export default {
        props : ['angka1','angka2'],
        data(){
            return{
                a : this.angka1,
                b : this.angka2,
                hasil : parseInt(this.angka1) + parseInt(this.angka2)
            }
        }
    }
</script>
<template>
    <div>
          <span>Nilai a : {{this.angka1}}</span><br>
          <span>Nilai b : {{this.angka2}}</span><br>
          <span>Hasil : {{ hasil }}</span>
    </div>
</template>