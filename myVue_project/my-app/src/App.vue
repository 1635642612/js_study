<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
	<h1>{{msg}}</h1>
	<div>
		<input v-model="info"/>
		<button @click="handAdd">添加</button>
		
		<ul>
			<Toitem v-for="item in dolist" :key="item" :item="item"></Toitem>
		</ul>
	</div>
	<hr />
	<p>
		1:安装脚手架  npm install --global vue-cli     vue -v 查看版本
		2:创建工程 vue create 项目名
		3:切换至目录 执行： npm run serve
	</p>
  </div>
</template>

<script>
import Toitem from './components/Todo-item.vue'

export default {
  name: 'App',
  data(){
  	return{
  		msg:"hello world",
  		info:"",
  		dolist:[]
  	}
  },
  methods:{
  	handAdd(){
  		this.dolist.push((this.info));
  		this.info="";
  	}
  },
  components: {
    Toitem
  }
}
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
