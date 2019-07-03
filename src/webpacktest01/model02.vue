<!DOCTYPE html>
<html lang="en" xmlns:v‐on="http://www.w3.org/1999/xhtml">
<head>     
  <metacharset="UTF‐8">
  <title>vue.js入门程序</title>  
</head>
<body>
  <div id="app">     
     <a v-bind:href="url"><span v-text="name"></span></a> <input type="text" v-model="num1"> + <input type="text" v-model="num2"> = <span v-text="result"></span>    
     <button v-on:click="change">计算</button>
  </div>
</body>
<script src="/js/vue/vue.min.js"></script>
<script>
  var VM = new Vue({
    el:"#app",//表示当前vue对象接管app的div区域
    data:{
      name:'slq',
      num1:0,
      num2:0,
      result:0,
      url:'xiayu.com'
    },
    method:{
      change:function(){
        this.result = Number.parseInt(this.num1) + Number.parseInt(this.num2)
        alert(this.result)
      }
    }
  });
</script>
</html>
    
