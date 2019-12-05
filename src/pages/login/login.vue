<template>
      <button type="submit" @click = loginIM class=".login_btn">登陆</button>
</template>

<script>
let WebIM = require("../../utils/WebIM")["default"]

export default {
  data () {
    return {
      username : "1n1n",
      password : "111"
    }
  },
  components: {
    WebIM
  },
  methods: {
    loginIM: function() {
      var options = {
        apiUrl: WebIM.config.apiURL,
        user: this.username,
        pwd: this.password,
        appKey: WebIM.config.appkey
      };
      WebIM.conn.open(options);
    }
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style>
.login_btn{
  margin-top: 50rpx;
  border: 1px solid #405f80;
  height: 80rpx;
  width: 460rpx;
  border-radius: 5px;
  background-color: dodgerblue;
}
</style>
