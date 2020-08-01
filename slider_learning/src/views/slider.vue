<template>
  <div class="flex">
    <vue-slider v-model="value"></vue-slider>
    <vue-slider v-model="value" direction="rtl"></vue-slider>
    <vue-slider
      v-model="value"
      direction="btt"
      :height="300"
      style="display: inline-block; margin: 30px;"
    ></vue-slider>
    <vue-slider
      v-model="value"
      direction="ttb"
      style="display: inline-block; margin: 30px 0; height: 300px;"
    ></vue-slider>
  </div>
</template>

<script>
// @ is an alias to /src
import $ from "jquery";
import VueSlider from "vue-slider-component";
import "vue-slider-component/theme/antd.css";

export default {
  name: "slider",
  components: { VueSlider },
  data() {
    return {
      value: [0,0],
    };
  },
};
$(function () {
  $("#btn").on("click", function () {
    alert("你点击了按钮");
  });
});
</script>