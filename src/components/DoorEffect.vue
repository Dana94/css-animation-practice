<template>
  <div class="hello">
    <div class="square red">
      <!-- <div class="panel">
        <div class="side1">
          <div class="inner"></div>
        </div>
        <div class="side2"></div>
        <div class="side3">

        </div>
      </div>-->
      <div class="door">
        <div class="latch">
          <div class="button"></div>
        </div>
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
  width: 400px;
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

.panel {
  position: absolute;
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    ". . ."
    "p1 p2 p3";
  border-top: 32px solid transparent;
}

.blue1 {
  height: 318px;
  border-top: 50px solid transparent;
  width: 100%;
  grid-area: col1;
  background-color: #e21708;
}

.side1 {
  grid-area: p1;
  border-top: 58px solid transparent;

  .inner {
    background-color: #e21708;
    height: 100%;
  }
}

.blue2 {
  grid-area: col2;
  border-left: 134px solid #e21708;
  border-top: 57px solid transparent;
}

.side2 {
  grid-area: p2;
  border-right: 134px solid #e21708;
  border-top: 57px solid transparent;
}

.blue3 {
  grid-area: col3;
  border-top: 58px solid transparent;
  .inner {
    background-color: #e21708;
    height: 100%;
  }
}

.side3 {
  height: 318px;
  border-top: 50px solid transparent;
  width: 100%;
  grid-area: p3;
  background-color: #e21708;
}

.red {
  background-color: red;
}

.latch {
  position: absolute;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  top: 40%;
  background-color: yellow;

  .button {
    width: 30px;
    height: 30px;
    background-color: purple;
  }
}

@keyframes open {
  0% {
    transform: rotateY(180deg);
  }
  100% {
    transform: translateX(400px);
  }
}
</style>
