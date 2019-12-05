<template>

      <button type="submit" @click = loginIM >登陆</button>
  
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

<style scoped>

</style>
