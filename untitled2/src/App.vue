<script setup>

import {ref} from "vue";

const numero1 = ref(0);
const numero2 = ref(0);
const resultado = ref(0);

const suma = () => {
    resultado.value = numero1.value + numero2.value;
}

const resta = () => {
    resultado.value = numero1.value - numero2.value;
}

const multiplicacion = () => {
    resultado.value = numero1.value * numero2.value;
}

const division = () => {
    resultado.value = numero1.value / numero2.value;
}

</script>

<template>
    <h1> Calculadora</h1>
    <div class="botones">
        <button @click="suma" style="margin: 10px">Sumar </button>
        <button @click="resta">Restar</button>
        <button @click="division" style="margin: 10px">Dividir</button>
        <button @click="multiplicacion">Multiplicar</button>

    </div>
    <div class="inputs">
        <input type="number" v-model="numero1" >
        <input type="number" v-model="numero2" style="margin: 10px">
        <p>El resultado de la operación es: {{ resultado }}</p>
    </div>


</template>

<style>

h1{
    text-align: center;
    color: darkseagreen;
}
input{
    text-align: center;
    width: 50px;
}
.inputs{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 80px;

}
.botones{
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>