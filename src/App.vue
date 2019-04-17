<template>
	<div id="app">
		<div id="nav">
			<van-nav-bar title="标题" left-text="返回" right-text="按钮" left-arrow @click-left="onClickLeft" @click-right="onClickRight" />
		</div>
		<div id="router">
			<van-button type="default">默认按钮</van-button>
			<van-button type="primary">主要按钮</van-button>
			<van-button type="info">信息按钮</van-button>
		</div>
		<!-- 使用 router-link 组件来导航. -->
		<!-- 通过传入 `to` 属性指定链接. -->
		<!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
		<router-link to="/home">Go to Foo</router-link>
		<router-link to="/about">Go to About</router-link>
		<router-link to="/list">Go to list</router-link>
		</p>
		<!-- 路由出口 -->
		<!-- 路由匹配到的组件将渲染在这里 -->
		<router-view></router-view>
	</div>
</template>

<script>
	// import HelloWorld from './components/HelloWorld.vue'
	import {
		NavBar,
		Toast,
		Button
	} from 'vant';

	export default {
		name: 'app',
		components: {
			NavBar,
			Toast,
			Button
		},
		methods: {
			onClickLeft() {
				Toast('返回');
			},
			onClickRight() {
				Toast('按钮');
			}
		}
	}
</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		/* margin-top: 60px; */
	}
</style>
