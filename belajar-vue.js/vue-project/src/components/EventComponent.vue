<template>
    <div>
      <p> watchers vue js </p>
      <h2 v-if="umur > 18">{{ pesanSelamat }}</h2>
      <p v-else> kamu belum cukup umur </p>
      <button @click="greet"> sapa bro ! </button>
      <slot name ="footer"></slot>
      <slot name ="header"></slot>
    </div>
  </template>

<script>
export default {
  props: ['nama', 'umur'],
  data() {
    return {
      pesan: 'Halo, ' + this.nama + '!'
    };
  },
  methods: {
    greet() {
      console.log('Halo, bro!');
      this.$emit('greeted'); // Memancarkan event 'greeted'
    }
  },
  computed: {
    pesanSelamat() {
      return 'selamat datang, ' + this.nama + '!';
    }
  },
  watch: {
    umur(newUmur, oldUmur) {
      console.log('Umur berubah dari', oldUmur, 'menjadi', newUmur);
      // Lakukan tindakan responsif lainnya...
    }
  }
}
</script>