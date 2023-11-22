<template>
  <div class="py-[100px] px-[50px]">
    <n-space :size="[300,100]" vertical>
      <AvatarGroup/>
      <MyCard/>
      <MyCarousel/>
    </n-space>
  </div>
</template>
<script lang="ts">
import AvatarGroup from '@/components/AvatarGroup.vue';
import MyCard from '@/components/MyCard.vue';
import MyCarousel from '@/components/MyCarousel.vue';
export default {
  name: 'Home',
  components: { AvatarGroup, MyCard, MyCarousel },
  setup() {
    
    
  }


}
</script>
<style scoped lang="postcss">

</style>
