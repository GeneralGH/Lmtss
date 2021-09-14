<template>
  <video autoplay="autoplay" loop class="bg_video" muted="muted">
    <source src="../../assets/video/A9A.webm" />
  </video>
  <div class="time">
    <span class="hour">
      {{ hour }}
    </span>
    :
    <span class="hour">
      {{ minute }}
    </span>
  </div>
  <Search />
  <BeiAn />
</template>

<script>
import Search from "./Search";
import BeiAn from "../../components/BeiAn.vue";

export default {
  name: "Home",
  components: { Search,BeiAn },
  data: function () {
    return {
      hour: new Date(),
      minute: new Date(),
    };
  },
  created() {},
  mounted() {
    let that = this;
    this.timer = setInterval(function () {
      that.hour = new Date().getHours();
      that.minute = new Date().getMinutes();
    });
  },
  beforeUnmount: function () {
    if (this.timer) {
      clearInterval(this.timer);
    }
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@import "../../style/reset.scss";

.time {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 80px;
  font-size: 100px;
  font-family: xiaoBaiTi;
  color: white;
}

video {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  height: auto;
  width: auto;
  z-index: -11;
}

source {
  min-height: 100%;
  min-width: 100%;
  height: auto;
  width: auto;
}
</style>