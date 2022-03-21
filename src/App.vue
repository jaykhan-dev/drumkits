<template>
  <div>
    <h1>Vue Drumkit</h1>
    <div class="keys">
      <Key v-for="(key, i) in keys" :sound="key" :key="i" />
    </div>
  </div>
</template>

<script>
import Key from "./components/Key-component.vue";
export default {
  name: "App",
  data() {
    return {
      keys: [
        {
          name: "boom",
          // eslint-disable-next-line no-undef
          audio: "./src/assets/sounds/boom.wav",
          letter: "A",
        },
        {
          name: "clap",
          audio: "./src/assets/sounds/clap.wav",
          letter: "S",
        },
        {
          name: "hihat",
          audio: "./src/assets/sounds/hihat.wav",
          letter: "D",
        },
        {
          name: "kick",
          audio: "./src/assets/sounds/kick.wav",
          letter: "F",
        },
        {
          name: "openhat",
          audio: "./src/assets/sounds/openhat.wav",
          letter: "G",
        },
        {
          name: "ride",
          audio: "./src/assets/sounds/ride.wav",
          letter: "H",
        },
        {
          name: "snare",
          audio: "./src/assets/sounds/snare.wav",
          letter: "J",
        },
        {
          name: "tink",
          audio: "./src/assets/sounds/tink.wav",
          letter: "K",
        },
        {
          name: "tom",
          audio: "./src/assets/sounds/tom.wav",
          letter: "L",
        },
      ],
    };
  },
  components: {
    Key,
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
.keys {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
