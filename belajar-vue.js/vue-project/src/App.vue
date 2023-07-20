<script setup>
import { ref } from 'vue'

const msg = ref ("hello world")
const rawHtml = ref ("<li> portal masuk isekai </li>")

let  a = 10;
let b = 5;
let c = a + b;
let d = a - b;
let e = a / b;
let f = a * b;

</script>

<template>
  <div id="app">
  <span>{{ msg }}</span> <br>
  <span v-html="rawHtml"></span>
  <div>yakin akan masuk ? {{ }}</div>

<input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
<label for="jack"> masuk </label><br>

<input type="checkbox" id="john" value="John" v-model="checkedNames">
<label for="john"> keluar </label><br>
<button v-bind:disabled="isButtonDisabled" onclick="alert('berhasil masuk isekai, menikahlah dengan gojo')"> start </button>
<br>

bil1 = {{ a }} <br>
bil2 = {{ b }} <br>
hasil = b1 + b2 = {{ c }} <br>
hasil = b1 - b2 = {{ d }} <br>
hasil = b1 / b2 = {{ e }} <br>
hasil = b1 * b2 = {{ f }}
  </div>

</template> 