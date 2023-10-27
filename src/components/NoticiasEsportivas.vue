<script setup>
defineProps(['title','news','rate'])
defineEmits('aumentarFonte','diminuirFonte')

function aumentarFont(){
emit('aumentarFonte')
}
function diminuirFont(){
emit('diminuirFonte')
}
</script>
<template>
<div class="noticia">
<h4>{{ title }}</h4>
<p>{{ news }}</p>
<p>{{ rate }}</p>
<button @click="aumentarFont()">+</button>
<button @click="diminuirFont()">-</button>
</div>
</template>
<style scoped>
.noticia{
    border: 1px solid silver;
    background-color: aqua;
    margin: 10px;
}
</style>