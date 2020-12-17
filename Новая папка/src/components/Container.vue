<template>
  <div class="informer-container">
    <Temperature
      v-bind:real="weather.temp_real"
      v-bind:feel="weather.temp_feel"
    ></Temperature>
    <Flex />
    <Humidity v-bind:hum="weather.humidity" />
    <Vert />
    <Wind v-bind:wind="weather.wind" />
  </div>
</template>

<script>
import Temperature from "./Temperature.vue";
import Humidity from "./Humidity.vue";
import Wind from "./Wind.vue";
import Flex from "./Flex.vue";
import Vert from "./Vert.vue";
export default {
  name: "Container",
  props: ["weather"],
  components: {
    Temperature,
    Humidity,
    Wind,
    Flex,
    Vert,
  },
};
</script>

<style>
.informer-container {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 400px;
  padding: 30px;
  background-image: url("/img/forest.png");
  background-size: cover;
  background-position: center center;
  border-radius: 20px;
  box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.75);
  background-color: aqua;
}
</style>