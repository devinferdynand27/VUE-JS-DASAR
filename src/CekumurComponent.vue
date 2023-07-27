<template>
    <div>
        <span v-if="umr > 17">
            Selamat {{ nama }} kamu Menjelang Dewasa {{ umr }}  
            {{ show }}
            <button @click="kurang">kurang Umur</button>
        </span>
        <div v-else>
           Kamu Masi Kecil  {{ umr }}
           <button @click="cekumur">Tambah Umur</button>
        </div>
    </div>

    <slot name="footer"></slot>

    <!-- {{ show }} -->
</template>

<script>
export default {
    props : ['nama','umur'],
    data(){
        return{
            umr : this.umur,
            nama : this.nama
        }
    },
    methods:{
        cekumur(){
           return this.umr+=10
        //    bisa kaya di bawah
        //    this.umr = this.umr + 10
        },
        kurang(){
           return this.umr--
        }
    },
    computed:{
        show(){
            alert('hallo bro')
        }
    }
}
</script>

