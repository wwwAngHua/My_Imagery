<script setup lang="ts">
import Photo from './components/Photo.vue'
</script>

<template>
    <div class="container">
        <div class="title">
            <el-text class="mx-1" size="large" style="color: black"
                >My Imagery</el-text
            >
            <br />
            <el-text class="mx-1"
                >Life is about capturing the moment in its beauty, and telling a
                story to every beautiful moment. - Blanca Acosta</el-text
            >
            <br />
            <el-text class="mx-1"
                >Photographer:
                <a href="https://github.com/wwwanghua" target="_blank"
                    >WangHua</a
                >, Email:
                <a href="mailto: wwwanghua@outlook.com" target="_blank"
                    >wwwanghua@outlook.com</a
                ></el-text
            >
        </div>
        <Photo />
    </div>
</template>

<style scoped>
.container {
    margin: 20px;
}
.title {
    text-align: center;
    margin-top: 50px;
    margin-bottom: 50px;
}
</style>
