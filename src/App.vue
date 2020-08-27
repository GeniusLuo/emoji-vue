<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <el-input
      v-model="textarea"
      resize="none"
      type="textarea"
      id="myId"
      rows="5"
      @keyup.enter.native="sendInfo"
    />
    <div :style="{textAlign: 'right'}">
      <Emoji :textAreaId="'myId'">
        <button>表情</button>
      </Emoji>
    </div>
  </div>
</template>

<script>
import Emoji from "./components/Emoji/Emoji.vue";

export default {
  name: "App",
  components: {
    Emoji,
  },
  data() {
    return {
      textarea: "",
    };
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
