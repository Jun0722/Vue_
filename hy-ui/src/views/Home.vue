<template>
  <div class="page">
    <h2>Home Page</h2>
    <!-- <Button type="primary" @click="testAxios()">测试axios调用</Button> -->
    <Button type="primary" @click="getUser()">获取用户信息</Button>
    <Button type="primary" @click="getMenu()">获取菜单信息</Button>
  </div>
</template>

<script>
import axios from 'axios';
import mock from '@/mock/index.js';
export default {
  name: 'Home',
  methods: {
    //   testAxios(){
    //       axios.get('http://localhost:8080')
    //       .then(function(res)
    //       {
    //           alert(res.data);
    //       }).catch(function(res){
    //           alert(res.data);
    //       });
    //   }
    getUser(){
        axios.get('http://localhost:8080/user')
        .then(function(res){
            alert(JSON.stringify(res.data));
        }).catch(function(res){
            alert(res);
        });
    },
     getMenu(){
        axios.get('http://localhost:8080/menu')
        .then(function(res){
            alert(JSON.stringify(res.data));
        }).catch(function(res){
            alert(res);
        });
    }
  },
}
</script>