<template>
    <n-grid x-gap="12" :cols="4">
        <n-gi>
            <n-card title="Card" hoverable>
                Card Content
            </n-card>
        </n-gi>
        <n-gi>
            <n-card title="Card" closable @close="handleClose" embedded >
                Card Content
            </n-card>
        </n-gi>
        <n-gi>
            <n-card class="mb-3">
                <template #header>
                    <n-skeleton v-if="loading" text width="60%" />
                    <template v-else>
                        Lorem Ipsum
                    </template>
                </template>
                <n-skeleton v-if="loading" text :repeat="6" />
                <template v-else>
                    Lorem ipsum dolor sit amet,<br>
                    consectetur adipiscing elit,<br>
                    sed do eiusmod tempor incididunt<br>
                    ut labore et dolore magna aliqua.<br>
                    Ut enim ad minim veniam,<br>
                    quis nostrud exercitation ullamco
                </template>
            </n-card>
            <n-switch v-model:value="loading" />
        </n-gi>
        <n-gi>
            <n-card content-style="padding: 0;">
    <n-tabs
      type="line"
      size="large"
      :tabs-padding="20"
      pane-style="padding: 20px;"
    >
      <n-tab-pane name="PARKLIFE">
        PARKLIFEsdklmloremsmxwom;lml Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae cumque nihil, eos assumenda adipisci similique deserunt quasi, consequuntur iste corporis sit minima voluptatum, maiores rerum suscipit veritatis. Assumenda, ratione deleniti?    
      </n-tab-pane>
      <n-tab-pane name="ROCKLIFE">
        ROCKLIFE
      </n-tab-pane>
    </n-tabs>
  </n-card>
        </n-gi>
    </n-grid>
</template>
<script setup lang="ts">
import { ref } from 'vue';
import { useMessage } from 'naive-ui'
const message = useMessage()
function handleClose() {
    message.info('Card Close')
}

const loading = ref(true);
</script>