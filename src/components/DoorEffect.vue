<template>
  <div class="hello">
    <div class="square red">
      <div class="panel">
        <div class="side1">
          <div class="screen"></div>
          <div class="inner"></div>
        </div>
        <div class="side2"></div>
        <div class="side3"></div>
      </div>

      <div class="door" :class="{open: isOpen}">
        <div class="latch" @click="openDoor">
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
  },
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    openDoor() {
      this.isOpen = true;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.square {
  height: 400px;
  width: 400px;
  border-radius: 15px;
}

.door {
  transform: rotateY(180deg);
  position: relative;
  display: grid;
  grid-template-rows: auto auto;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-areas:
    ". . ."
    "col1 col2 col3";
  border-top: 32px solid transparent;

  &.open {
    animation: open 2s linear forwards;
  }
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
  border-left: 1px solid;
}

.side1 {
  grid-area: p1;
  border-top: 58px solid transparent;
  position: relative;
  .screen {
    height: 140px;
    width: 140px;
    background-color: grey;
    position: absolute;
    top: 20px;
    left: 20px;
  }

  .inner {
    background-color: #e21708;
    height: 100%;
    border-radius: 0 0 0 15px;
  }
}

.blue2 {
  grid-area: col2;
  border-left: 134px solid #e21708;
  border-top: 57px solid transparent;
}

.side2 {
  grid-area: p2;
  border-right: 133px solid #e21708;
  border-top: 57px solid transparent;
}

.blue3 {
  grid-area: col3;
  border-top: 58px solid transparent;
  .inner {
    background-color: #e21708;
    height: 100%;
    border-radius: 0 0 15px 0px;
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
  top: 50%;
  background-color: yellow;
  right: 10px;

  .button {
    height: 0;
    border-top: 15px solid transparent;
    border-left: 15px solid purple;
    border-bottom: 15px solid transparent;
    position: absolute;
    right: 10px;
    top: 5px;
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
