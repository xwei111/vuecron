<template>
    <div>
        <p>cron-element:</p>
        <a-input v-model="cronVal" style="width: 400px;marginRight: 20px;" placeholder="请填写cron表达式" />
        <a-button type="primary" @click="selectHanlde">选择cron-ele表达式</a-button>
        <cron-ele ref="cronEleRef" @ok="okHandle" />
    </div>
</template>
<script>
import cronEle from '@/components/cron-ele/index.vue'

export default {
    data() {
        return {
            cronVal: ''
        }
    },
    components: {
        cronEle
    },
    methods: {
        selectHanlde() {
            this.$refs['cronEleRef'].show()
        },
        okHandle(val) {
            this.cronVal = val
        }
    }
}
</script>