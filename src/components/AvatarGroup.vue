<template>
  <div>
    <!-- :size=[x,y] -->
    <n-space :size="[100,30]" >
      <n-badge value="999+">
        <n-avatar round>App</n-avatar>
      </n-badge>
      <n-badge value="999+">
        <n-avatar src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg" round />
      </n-badge>
      <n-avatar-group :options="options" :size="40" :max="4" />
      <n-avatar-group :options="options" :size="40" :max="3">
        <template #avatar="{ option: { name, src } }">
          <n-tooltip>
            <template #trigger>
              <n-avatar :src="src" />
            </template>
            {{ name }}
          </n-tooltip>
        </template>
        <!-- restOptions 多的options rest:多的數量-->
        <template #rest="{ options: restOptions, rest }">
          <n-dropdown :options="createDropdownOptions(restOptions)" placement="top">
            <n-avatar>+{{ rest }}</n-avatar>
          </n-dropdown>
        </template>
      </n-avatar-group>
    </n-space>
  </div>
</template>
<script lang="ts">
export default {
  setup() {
    return {
      options: [
        {
          name: 'Leonardo DiCaprio',
          src: 'https://gw.alipayobjects.com/zos/antfincdn/aPkFc8Sj7n/method-draw-image.svg'
        },
        {
          name: 'Jennifer Lawrence',
          src: 'https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg'
        },
        {
          name: 'Audrey Hepburn',
          src: 'https://gw.alipayobjects.com/zos/antfincdn/aPkFc8Sj7n/method-draw-image.svg'
        },
        {
          name: 'Anne Hathaway',
          src: 'https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg'
        },
        {
          name: 'Taylor Swift',
          src: 'https://gw.alipayobjects.com/zos/antfincdn/aPkFc8Sj7n/method-draw-image.svg'
        }
      ],
       createDropdownOptions: (options: Array<{ name: string; src: string }>) =>
        options.map((option) => ({
          key: option.name,
          label: option.name
        }))
    }
  }
};
</script>
