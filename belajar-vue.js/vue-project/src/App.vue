<template>
  <div>
    <header text = "ini adalah header "></header>
    <!-- <h2> hallo ini adalah komponen utama </h2> -->
    <my-component nama = "novi" umur = "17"></my-component>
    <latihan-component name ="novi azkya" age ="20 "></latihan-component>
    <latihan2-component></latihan2-component>
    <whatchers-component nama ="novi" umur="18"></whatchers-component>
    <event-component :nama="nama" :umur="umur" @greeted="onGreeted">
      <template #footer>
      <div>
        <p> ini adalah footer event </p>
      </div>
    </template>
    <template #header>
      <div>
        <p> ini adalah header event </p>
      </div>
    </template>
    </event-component>
  </div>
</template>

<script setup>
import MyComponent from './components/MyComponent.vue';
import Header from './components/Header.vue';
import LatihanComponent from './components/LatihanComponent.vue';
import Latihan2Component from './components/Latihan2Component.vue';
import WhatchersComponent from './components/WhatchersComponent.vue';
import EventComponent from './components/EventComponent.vue';

// event
import { ref } from 'vue';
const nama = ref ('novi');
const umur = ref (20);

const onGreeted = () => {
  console.log ('kamu udah disapa bro !');
};

// export default {
//   name : "App",
//   components : {
//     MyComponent,
//     Header
//   }
// }
</script> 
