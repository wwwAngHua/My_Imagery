<script setup lang="ts">
const photos = [
    'https://fuss10.elemecdn.com/a/3f/3302e58f9a181d2509f3dc0fa68b0jpeg.jpeg',
    'https://fuss10.elemecdn.com/1/34/19aa98b1fcb2781c4fba33d850549jpeg.jpeg',
    'https://fuss10.elemecdn.com/0/6f/e35ff375812e6b0020b6b4e8f9583jpeg.jpeg',
    'https://fuss10.elemecdn.com/9/bb/e27858e973f5d7d3904835f46abbdjpeg.jpeg',
    'https://fuss10.elemecdn.com/d/e6/c4d93a3805b3ce3f323f7974e6f78jpeg.jpeg',
    'https://fuss10.elemecdn.com/3/28/bbf893f792f03a54408b3b7a7ebf0jpeg.jpeg',
    'https://fuss10.elemecdn.com/2/11/6535bcfb26e4c79b48ddde44f4b6fjpeg.jpeg',
]
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
                v-for="(src, index) in photos"
                :key="index">
                <el-image
                    style="width: auto; height: auto"
                    :src="src"
                    :zoom-rate="1.2"
                    :max-scale="7"
                    :min-scale="0.2"
                    :preview-src-list="photos"
                    :initial-index="index"
                    fit="contain" /><el-text class="mx-1" size="small"
                    >Small</el-text
                ></el-col
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
