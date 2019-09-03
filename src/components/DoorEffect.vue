<template>
  <div class="hello">
    <div class="square red">
      <div class="door">
        <div class="blue1"></div>
        <div class="blue2"></div>
        <div class="blue3">
          <div class="inner"></div>
        </div>
      </div>
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
  height: 400px;
  width: 200px;
}

.door {
  animation: open 2s linear forwards;
  position: relative;
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    ". . ."
    "col1 col2 col3";
  border-top: 32px solid transparent;
}

.blue1 {
  height: 318px;
  border-top: 50px solid transparent;
  width: 100%;
  grid-area: col1;
  background-color: purple;
}

.blue2 {
  grid-area: col2;
  border-left: 67px solid purple;
  border-top: 58px solid transparent;
}

.blue3 {
  grid-area: col3;
  border-top: 58px solid transparent;
  .inner {
    background-color: purple;
    height: 100%;
  }
}

.red {
  background-color: red;

}

@keyframes open {
  0% {
    transform: rotateY(180deg);
  }

  100% {
    transform: translateX(200px);
    //background-color: pink;
  }
}
</style>
