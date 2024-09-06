<template>
    <div class="conteiner">
        <SideBar></SideBar>
        <div class="content">
            <router-view></router-view>
        </div>
    </div>
</template>

<script setup>
    import SideBar from '../components/SideBar.vue';
</script>

<style>

.conteiner {
    display: flex;
}
.content {
    flex: 1;
    padding: 20px;
}
</style>