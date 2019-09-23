<template>
  <div class="home">
    <Door/>
  </div>
</template>

<script>
// @ is an alias to /src
import Door from '@/components/Door.vue'

export default {
  name: 'home',
  components: {
    Door
  }
}
</script>
