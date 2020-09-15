<template>
  <div class="app">
    <cron-antd />
    <cron-ele />
  </div>
</template>
<script>
import cronAntd from './views/cronAntd';
import cronEle from './views/cronEle';

export default {
  components: {
    cronAntd,
    cronEle
  }
};
</script>
<style lang="css">
.app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 100px;
}
</style>

