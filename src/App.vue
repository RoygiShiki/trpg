<template>
	<div id="app">
		<div id="nav">
			<router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link>
		</div>
		<router-view />
	</div>
</template>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		/* text-align: center; */
		color: #2c3e50;
	}

	.el-row {
		margin-bottom: 20px;
	}
	
	.radius {
		border: 1px solid #d7dae2;
		border-radius: 0;
	}
	
	.mb-20 {
		margin-bottom: 20px;
	}
	
	.mb-0 {
		margin-bottom: 0;
	}
	
	.sub-title {
		font-size: 14px;
		color: #8492a6;
	}
</style>
