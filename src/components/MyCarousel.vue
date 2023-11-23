<template>
    <div>
        <n-grid x-gap="12" :cols="4">
            <n-gi>
                <n-carousel class="overflow-hidden" dot-type="line"  draggable :loop="false" centered-slides>
                    <img v-for="(i, index) in 3" :key="index" class="carousel-img"
                        :src="`https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel${index + 2}.jpeg`">
                </n-carousel>
            </n-gi>
            <n-gi>
                <n-carousel class="overflow-hidden" dot-type="line"  draggable :loop="false" effect="fade" autoplay centered-slides>
                    <img v-for="(i, index) in 3" :key="index" class="carousel-img"
                        :src="`https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel${index + 2}.jpeg`">
                </n-carousel>
            </n-gi>
            <n-gi>
                <n-carousel show-arrow class="overflow-hidden" dot-type="dot" :slides-per-view="1.5" :space-between="20" draggable :loop="false" centered-slides>
                    <img v-for="(i, index) in 3" :key="index" class="carousel-img"
                        :src="`https://naive-ui.oss-cn-beijing.aliyuncs.com/carousel-img/carousel${index + 2}.jpeg`">
                </n-carousel>
            </n-gi>
        </n-grid>
    </div>
</template>
<style scoped>
.carousel-img {
    width: 100%;
    height: 240px;
    object-fit: cover;
}
</style>