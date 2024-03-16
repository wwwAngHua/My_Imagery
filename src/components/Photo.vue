<script setup lang="ts">
import { ref } from 'vue'
interface Photo {
    url: string
    title: string
}

const photos = ref<Array<Photo>>([
    {
        url: 'https://img.t1ykf.com/file/f7b19f972774213dabff5.jpg',
        title: 'Photo 1',
    },
    {
        url: 'https://img.t1ykf.com/file/b8286d1d920f2843d794f.jpg',
        title: 'Photo 2',
    },
    {
        url: 'https://img.t1ykf.com/file/c665df4d4f90aca9fbf4a.jpg',
        title: 'Photo 3',
    },
    {
        url: 'https://img.t1ykf.com/file/1f9598fa187c42868aadc.jpg',
        title: 'Photo 4',
    },
    {
        url: 'https://img.t1ykf.com/file/86bc8c088219abf08a6d3.jpg',
        title: 'Photo 5',
    },
    {
        url: 'https://img.t1ykf.com/file/624f259693157e5f21ee6.jpg',
        title: 'Photo 6',
    },
    {
        url: 'https://img.t1ykf.com/file/6aca947249ac58c2c43e3.jpg',
        title: 'Photo 7',
    },
    {
        url: 'https://img.t1ykf.com/file/c13bad6d39bd4fda6a503.jpg',
        title: 'Photo 8',
    },
])
const photoUrls = photos.value.map((photo) => photo.url)
</script>

<template>
    <div>
        <el-row :gutter="20">
            <el-col
                class="photo"
                :xs="24"
                :sm="12"
                :md="6"
                :lg="6"
                :xl="6"
                lazy
                v-for="(data, index) in photos"
                :key="index">
                <el-image
                    style="width: auto; height: auto"
                    :src="data.url"
                    :zoom-rate="1.2"
                    :max-scale="7"
                    :min-scale="0.2"
                    :preview-src-list="photoUrls"
                    :initial-index="index"
                    fit="contain" /><el-text class="mx-1" size="small">{{
                    data.title
                }}</el-text></el-col
            ></el-row
        >
    </div>
</template>

<style scoped>
.photo {
    text-align: center;
    margin-top: 10px;
    margin-bottom: 10px;
}
</style>
