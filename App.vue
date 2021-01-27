<template>
  <view class="container">
    <text class="text-color-primary">{{ message }}</text>
    <button
      class="learnMore"
      :on-press="onPressLearnMore"
      title="Learn More"
      color="#841584"
      :style="{margin:10}"
      accessibility-label="Learn more about the app by clicking this purple button"
    />
  <image/>
  </view>
</template>

<script>
import image from "./image"
export default {
  components: { image },
  data() {
    return {
      message: "Hello World",
    };
  },
  methods: {
    exclaim() {
      this.message += "!";
    },
    onPressLearnMore: function () {
      alert("Learn More!");
    },
  },
};
</script>

<style>
.container {
  flex: 1;
  background-color: rgb(185, 143, 190);
  color: rgb(30, 41, 38);
  align-items: center;
  justify-content: center;
}
.text-color-primary {
  color: rgb(30, 41, 38);
  font-size: 30;
}
</style>