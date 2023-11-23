<template>
    <div class="pb-20">
        <n-dropdown trigger="hover" :options="options" @select="handleSelect" placement="bottom-start">
            <n-button>Go For a Trip</n-button>
        </n-dropdown>
    </div>
</template>
  
<script lang="ts" setup>
import { h, ref } from 'vue'
import type { Component } from 'vue'
import { NIcon } from 'naive-ui';
import {
  PersonCircleOutline as UserIcon,
  Pencil as EditIcon
} from '@vicons/ionicons5';
import { useMessage } from 'naive-ui';
const message = useMessage();

const renderIcon = (icon: Component) => {
  return () => {
    return h(NIcon, null, {
      default: () => h(icon)
    })
  }
}
const options = ref([
    {
        label: 'Marina Bay Sands',
        key: 'marina bay sands',
        icon: renderIcon(UserIcon),
        disabled: true
    },
    {
        label: "Brown's Hotel, London",
        key: "brown's hotel, london",
        icon: renderIcon(EditIcon),
        children: [
            {
              label: '鸡肉',
              key: 'chicken',
              props: {
                onClick: () => {
                  message.info('Okay')
                }
              }
            },]
    },
    {
        label: 'Atlantis Bahamas, Nassau',
        key: 'atlantis nahamas, nassau'
    },
    {
        label: 'The Beverly Hills Hotel, Los Angeles',
        key: 'the beverly hills hotel, los angeles'
    }
]);
const handleSelect = (key: string | number) => {
    message.info(String(key))
}
const handleSelect1 = (key: string | number) => {
    message.info(String(key))
};

</script>