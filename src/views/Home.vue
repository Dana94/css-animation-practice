<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <DoorEffect/>
  </div>
</template>

<script>
// @ is an alias to /src
import DoorEffect from '@/components/DoorEffect.vue'

export default {
  name: 'home',
  components: {
    DoorEffect
  }
}
</script>
