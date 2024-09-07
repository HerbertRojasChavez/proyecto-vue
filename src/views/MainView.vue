<template>
    <div class="conteiner">
        <SideBar></SideBar>
        <div class="content">
            <router-view></router-view>
        </div>
    </div>
</template>

<script setup>
    import SideBar from '../components/Sidebar.vue';
</script>

<style scoped>

.conteiner {
    display: flex;
}
.content {
    flex: 1;
    padding: 20px;
}
</style>