<template>
  <div class="py-[100px] px-[50px]">
    <n-space :size="[300,100]" vertical>
      <AvatarGroup/>
      <MyCard/>
      <MyCarousel/>
      <MyCollapse/>
      <MyDropdown/>
      <MyEllipsis/>
    </n-space>
  </div>
</template>
<script lang="ts">
import AvatarGroup from '@/components/AvatarGroup.vue';
import MyCard from '@/components/MyCard.vue';
import MyCarousel from '@/components/MyCarousel.vue';
import MyCollapse from '@/components/MyCollapse.vue';
import MyDropdown from '@/components/MyDropdown.vue';
import MyEllipsis from '@/components/MyEllipsis.vue'
export default {
  name: 'Home',
  components: { AvatarGroup, MyCard, MyCarousel, MyCollapse,MyDropdown,MyEllipsis },
  setup() {
    
    
  }


}
</script>
<style scoped lang="postcss">

</style>
