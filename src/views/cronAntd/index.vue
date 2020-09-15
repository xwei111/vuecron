<template>
  <div style="marginBottom: 50px;">
    <p>cron-antd:</p>
    <a-input v-model="cronVal" style="width: 400px;marginRight: 20px;" placeholder="请填写cron表达式" />
    <a-button type="primary" @click="selectHanlde">选择cron-antd表达式</a-button>
    <cron-antd ref="cronAntdRef" @ok="okHandle" />
  </div>
</template>
<script>
import cronAntd from '@/components/cron-antd/index.vue';

export default {
  data() {
    return {
      cronVal: ''
    }
  },
  components: {
    cronAntd
  },
  methods: {
    selectHanlde() {
      this.$refs['cronAntdRef'].show()
    },
    okHandle(val) {
      this.cronVal = val
    }
  }
};
</script>

