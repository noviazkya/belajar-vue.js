<template>
    <div>
        <!-- <h1> hallo dunia </h1> -->
        <!--<p> ini komponen gue </p> -->

        <h2> nama {{ nama }}</h2>
        <h2> umur {{ umur }}</h2>

    </div> 
</template>

<script>
export default {
    name : "MyComponent", 
    props : ['nama', 'umur',],
    data () { 
        return {
            message : "ini pesan dari component"
        }
    },
    methods : {
        greet () {
            console.log ("hallo");
        }
    },
}
</script>

<style>
h1 {
    color : blue;
} 
p {
    font-size : 16px;
}
</style>