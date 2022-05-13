<template>
  <div @click="flipper" class="main">
    <transition mode="out-in" :name="test">
      <div
        key="f"
        v-if="!flipped"
        class="front w-96 h-full m-5 bg-red-500 rounded-lg cursor-pointer"
      >
        <h1>Hi</h1>
        <slot name="front"></slot>
      </div>

      <div
        key="b"
        v-if="flipped"
        class="back w-96 h-full m-5 bg-green-500 rounded-lg cursor-pointer"
      >
        <h1>Not Hi</h1>
        <slot name="back"></slot>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: "Card",
  data() {
    return { flipped: false, show: false, test: "right" };
  },
  methods: {
    flipper() {
      this.flipped = !this.flipped;
      if (this.test == "left") {
        this.test = "right";
      } else {
        this.test = "left";
      }
    },
  },
};
</script>

<style >
.right-enter-active,
.right-leave-active {
  transition: 0.3s linear;
}

.right-enter {
  transform: rotateY(90deg);
}
.right-leave-to {
  transform: rotateY(-90deg);
}
.main {
  perspective: 1000px;
  transform-style: preserve-3d;
}

.left-enter-active,
.left-leave-active {
  transition: 0.3s linear;
}

.left-enter {
  transform: rotateY(-90deg);
}
.left-leave-to {
  transform: rotateY(90deg);
}
</style> 
