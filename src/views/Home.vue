<template>
  <div class="home">
    <div class="square red">
      <InnerPanel/>
      <Door/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import InnerPanel from "@/components/InnerPanel.vue";
import Door from '@/components/Door.vue'

export default {
  name: 'home',
  components: {
    InnerPanel,
    Door
  }
}
</script>

<style lang="scss" scoped>
.square {
  height: 400px;
  width: 400px;
  border-radius: 15px;
  &.red {
    background-color: red;
  }
}
</style>
