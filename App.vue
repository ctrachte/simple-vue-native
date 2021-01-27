<template>
  <view class="container">
    <text class="text-color-primary">{{ message }}</text>
    <button title="Press me!" @press="exclaim" />
    <button class="alert" v-bind:title="message" v-bind:on-press="handleBtnPress"/>
  </view>
</template>

<script>
export default {
  data() {
    return {
      message: "Hello World"
    };
  },
  methods: {
    exclaim() {
      this.message += "!";
    },
    handleBtnPress: function() {
      alert('Btn Press');
    }
  },
};
</script>

<style>
.container {
  flex: 1;
  background-color: white;
  align-items: center;
  justify-content: center;
}
.text-color-primary {
  color: blue;
  font-size: 30;
}
button {
  margin:10%;
}
</style>