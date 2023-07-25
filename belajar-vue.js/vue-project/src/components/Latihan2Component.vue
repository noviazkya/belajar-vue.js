<template>
    <div>
  <input type="v-model" v-model="cari" placeholder="cari data">
  <ul>
    <li v-for="item in cariData" :key="item.id">
         {{ item.title }} - {{ item.price }}   
    </li>
  </ul>
    </div>
    <div v-if="cariData.length === 0">
        <p> maaf, tidak ada hasil pencarian </p>
    </div>
  </template>
  
  <script>
  export default {
    data(){
      return{
        cari: '',
        products: []
      } 
    },
      created() {
        this.products = [
          {id: 1, title: "baju anak",  price: 25000},
          {id: 2, title: "susu anak",  price: 75000},
          {id: 3, title: "topi",  price: 10000},
          {id: 4, title: "balon",  price: 1000},
          {id: 5, title: "kinder joy",  price: 15000}
        ]
      },
      computed: {
        cariData(){
          return this.products.filter((item)=>{
             return item.title.match(this.cari);
          });
        }
      },
    }
  </script>