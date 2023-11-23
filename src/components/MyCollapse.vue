<template>
    <div>
        <n-grid x-gap="12" :cols="4">
            <n-gi>
                <!-- accordion 只允許打開一個 -->
                <n-collapse default-expanded-names="1" accordion arrow-placement="right">
                    <n-collapse-item title="动态类型" name="1">
                        <div>Python</div>
                    </n-collapse-item>
                    <n-collapse-item title="静态类型" name="2">
                        <div>Java</div>
                    </n-collapse-item>
                </n-collapse>
            </n-gi>
            <n-gi>
                <n-collapse :default-expanded-names="['1', '2']">
                    <n-collapse-item title="green light" name="1">
                        <n-collapse>
                            <n-collapse-item title="on" name="1">
                                <div>pass</div>
                            </n-collapse-item>
                            <n-collapse-item title="flashing" name="2" disabled>
                                <div>pass fastly</div>
                            </n-collapse-item>
                        </n-collapse>
                    </n-collapse-item>
                    <n-collapse-item title="red light" name="2">
                        <div>stop</div>
                    </n-collapse-item>
                    <n-collapse-item title="amber light" name="3">
                        <div>warn</div>
                    </n-collapse-item>
                </n-collapse>
            </n-gi>
            <n-gi>
                <n-collapse>
                    <template #header-extra>
                        <n-icon><add-icon /></n-icon>
                    </template>
                    <template #arrow>
                        <n-icon>
                            <cash-icon />
                        </n-icon>
                    </template>
                    <n-collapse-item title="Bronze" name="1">
                        <div>good</div>
                    </n-collapse-item>
                    <n-collapse-item title="Silver" name="2">
                        <div>nice</div>
                    </n-collapse-item>
                    <n-collapse-item title="Gold" name="3">
                        <div>very good</div>
                    </n-collapse-item>
                </n-collapse>
            </n-gi>
        </n-grid>
    </div>
</template>
<script setup lang="ts">
import { CashOutline as CashIcon,AddCircleOutline as AddIcon } from '@vicons/ionicons5';
</script>