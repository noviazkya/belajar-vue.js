<template>
    <div>
      <p> watchers vue js </p>
      <h2 v-if="umur >= 18">{{ pesanSelamat }}</h2>
      <p v-else> kamu belum cukup umur.</p>
      <button @click="greet"> sapa bro ! </button>
    </div>
  </template>

<script>
export default {
  props: ['nama', 'umur'],
  data() {
    return {
      pesan: 'halo, ' + this.nama + '!'
    };
  },
  methods: {
    greet() {
      console.log('halo, bro!');
    }
  },
  computed: {
    pesanSelamat() {
      return 'selamat datang, ' + this.nama + '!';
    }
  },
  watch: {
    umur(newUmur, oldUmur) {
      console.log('umur berubah dari', oldUmur, 'menjadi', newUmur);
      // lakukan tindakan responsif lainnya
    }
  }
}
</script>  
