<template>
  <div class="hello">
    <div class="square red">
      <div class="square blue"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DoorEffect",
  props: {
    msg: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.square {
  height: 200px;
  width: 200px;
}

.blue {
  background-color: blue;
  animation: open 2s linear forwards;
}

.red {
  background-color: red;
  margin: 0 auto;
}

@keyframes open {
  0% {
    transform: rotateY(180deg);
  }

  100% {
    transform: translateX(200px);
    background-color: pink;
  }
}
</style>
