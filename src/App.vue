<template>
  <div id="app" class="grid grid-cols-1 justify-items-center">
    <Card v-for="card in 3" :key="card" class="flex-initial m-2">
      <div slot="back">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste quos
        beatae quisquam qui, possimus minus vel officiis, magnam, tenetur odio
        sed fuga a quidem eius dolorum praesentium facilis. Beatae rem
        blanditiis nobis quam soluta expedita, reprehenderit nostrum ratione
        eaque accusamus repellendus cum facere ad aliquid non voluptas rerum
        delectus? Nobis minima possimus mollitia quasi, veritatis perspiciatis
        alias placeat ipsum laboriosam voluptatem ullam totam explicabo
        aspernatur amet quisquam aliquam ipsa repellendus!
      </div>
      <div slot="front">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ea officia
        modi quod iste, odio quibusdam debitis consectetur corrupti? Ut
        veritatis labore rem cum mollitia illum?
      </div>
    </Card>
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "App",
  components: {
    Card,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
