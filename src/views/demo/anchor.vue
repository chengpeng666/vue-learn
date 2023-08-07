<template>
  <div class="container">
    <cy-anchor v-model="anchor">
      <cy-anchor-item v-for="(item) in forms" :key="item.formId" :label="item.title" :name="item.formId" class="anchor-item">
        <form-demo />
      </cy-anchor-item>
    </cy-anchor>
  </div>
</template>

<script>

import FormDemo from '@/views/demo/formDemo.vue'

export default {
  name: 'Anchor',
  components: { FormDemo },
  data() {
    return {
      anchor: '',
      forms: [
        {
          title: '表单1',
          formId: 'form1'
        },
        {
          title: '表单2',
          formId: 'form2'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.anchor-item {
  margin-bottom: 15px;
  background-color: #fff;

  .text {
    padding: 20px;
    white-space: pre-line;
  }
}
</style>
