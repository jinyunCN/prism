<template>
  <main>
   <a-space direction="vertical">
     <a-page-header
       style="border: 1px solid rgb(235, 237, 240)"
       title="拍照翻译"
       sub-title="让我做你的眼睛"
     />

     <a-card>
       <p style="text-align: center;font-size: large;font-weight: bold;">点击下方按钮即可拍照翻译</p>
       <p style="text-align: center;">
       <a-button type="primary" shape="circle" size="large" style="height: 120px;width: 120px;">
         <template #icon>
           <CameraOutlined />
         </template>
       </a-button>
     </p>
     </a-card>

     <a-collapse v-model:activeKey="activeKey" :bordered="false">
      <a-collapse-panel key="1" header="必应翻译">
       <p>{{ bing }}</p>
      </a-collapse-panel>
      <a-collapse-panel key="2" header="网易翻译">
       <p>{{ wangyi }}</p>
      </a-collapse-panel>
      <a-collapse-panel key="3" header="离线翻译">
       <p>{{ lixian }}</p>
      </a-collapse-panel>
     </a-collapse>
   </a-space>
  </main>
</template>

<script lang="ts" setup>
import { ref } from 'vue';
const activeKey = ref(['1','2','3']);
const bing = `has not finished`;
const wangyi = `has not finished`
const lixian = `has not finished`
</script>

