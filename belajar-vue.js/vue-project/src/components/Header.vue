<template>
    <div>
     <header></header>   
    <my-component nama = "novi" umur = "17"></my-component>
    </div>
    
</template>
<script setup>

import MyComponent from './MyComponent.vue';

// export default {
//     components : {
//         MyComponent,
//     }
// }

// export default {
//     name : "header", 
//     props : ['text'],
// }

</script>
<style>
h3 {
    color : black;
    background-color: aqua;
    text-align: center;
} 
</style>