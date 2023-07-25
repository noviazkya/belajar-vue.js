<template>
    <div v-if=" age > 18 " >
        <p> selamat datang {{ name }} </p>
    </div>
    <div v-else>
        <p> maaf kamu belum cukup umur </p>
    </div>
    <button @click="greet"> sapa </button>

</template>

<script>  
export default {
    props : ['name', 'age'],
    methods : {
        greet () {
            alert ("hallo" + this.name);
        }
    },
}
</script>