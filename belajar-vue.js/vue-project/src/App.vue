<template>
  <div>
    <h2>Formulir siswa</h2>
    <form @submit.prevent="submitForm"> 
    <label for="">Nama</label>
    <input type="text" v-model="siswa.nama"><br>
    <label for="">Kelas</label>
    <input type="text" v-model="siswa.kelas"><br>
    <label for="">Alamat</label>
    <textarea v-model="siswa.alamat" cols="20" rows="5"></textarea><br>
    <label for="">nilai matematika</label>
    <input type="number" v-model="siswa.mtk" id="mtk"><br>
    <label for="">nilai b.indonesia</label>
    <input type="number" v-model="siswa.bhs" id="bhs"><br>
    <label for="">nilai ipa</label>
    <input type="number" v-model="siswa.ipa" id="ipa"><br>
    <button type="submit">Simpan</button>
    </form>
    <div v-if="showResult">
      nama : {{ name }} <br>
      kelas : {{ kelas }} <br>
      alamat : {{ alamat }}<br>
      nilaiMtk: {{ mtk }}<br>
      nilaibhs: {{ bhs }}<br>
      nilaiipa: {{ ipa }} <br>
      Total nilai: {{ total }} <br>
      keterangan: {{ keterangan }}
    </div>
  </div>
</template>
<script>
import { ref } from 'vue';

export default {
// logika
  

  data() {
    return {
    siswa: {
     nama: '',
     kelas: '',
     alamat: '',
     mtk: '',
     bhs: '',
     ipa: ''
    },
    showResult: ref(false),
      name: ref(''),
      kelas: ref(''),
      alamat: ref(''),
      mtk: ref(''),
      bhs: ref(''),
      ipa: ref(''),
      total: 0,
      keterangan : ref('')
    };
  },
  methods: {
    submitForm() {
      this.name = this.siswa.nama;
      this.kelas = this.siswa.kelas;
      this.alamat = this.siswa.alamat;
      this.mtk = this.siswa.mtk;
      this.bhs = this.siswa.bhs;
      this.ipa = this.siswa.ipa;
      this.total = parseInt(this.mtk) + parseInt(this.bhs) + parseInt(this.ipa);
      if (this.total > 240) {
        this.keterangan = "lulus"
      } else {
        this.keterangan = "tidak lulus"
      } 
      this.showResult = true;
    },
    
  },
}
</script>