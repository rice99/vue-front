<template>
  <div>
    <h2>users</h2>
    <div>sdkljflksljfl</div>
    <h3>啊啊啊啊啊</h3>
    <div>使用打包后的文件运行</div>
    <p>ppppppp</p>
    <span>一键启动</span>
    <ul>
      <li v-for="(user) in users" :key="user.id">{{user.id}}:{{user.name}}</li>
    </ul>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "app",
  data() {
    return {
      users: []
    };
  },
  mounted() {
    axios.get("http://81.70.4.241:3005/api/users").then(response => {
      this.users = response.data;
    });
  }
};
</script>

<style>
</style>
