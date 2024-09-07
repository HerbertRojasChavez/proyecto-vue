<template>
    <div>
        <h2>Lista de Tereas</h2>
        <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea">
        <!-- <table>
            <tr>
                <td>categoria</td>
                <td>cantidad</td>
                <td>P/U</td>
                <td>boton</td>
            </tr>
            <tr v-for="(tarea, index) in tareas" :key="index">
                <td>{{ tarea }}</td>
                <td><input type="text"></td>
                <td><input type="text"></td>
                <td><button @click="borrarTarea">X</button></td>
            </tr>   
        </table> -->
        <ul>
            <li v-for="(tarea, index) in tareas" :key="index">
                {{ tarea }}
                <button @click="borrarTarea">Borrar</button>
            </li>
        </ul>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    const tareas = ref([]);
    const nuevaTarea = ref('');
    const addTarea = () => {
        tareas.value.push(nuevaTarea.value);
        nuevaTarea.value = '';
    }
    const borrarTarea = (index) => {
        tareas.value.splice(index,1);
    }

</script>

<style>

</style>