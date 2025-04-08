<template>
	<div class="hero bg-base-200 min-h-screen">
		<div class="hero-content flex-col lg:flex-row-reverse">
			<img
				src="../assets/impes.png"
				class="max-w-xl rounded-lg shadow-2xl" />
			<div>
				<h1 class="text-5xl font-bold gradient-text">定制综合管理平台</h1>
				<p class="py-6">
					这是一款专业级的飞行模拟管理系统，为大家提供活动报名，数据查询等。
					<br>
					Aerion-Integrated-Management-Platform™
				</p>
				<button class="btn btn-primary" @click="goto">查看实际使用平台</button>
			</div>
		</div>
	</div>
</template>

<style scoped>
/* 调整浏览器模型的最大宽度 */
.mockup-browser {
	max-width: 100%;
}

/* 可选：如果需要进一步自定义样式 */
.mockup-browser .grid {
	font-size: 2rem; /* 增大字体大小以匹配更大的模型 */
}
.gradient-text {
	background-image: linear-gradient(120deg, #84fab0 0%, #8fd3f4 100%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}
</style>
<script>
export default {
	name: "Product",
	methods:{
		goto(){
			window.location.href='https://www.impes.net/'
		}
	}
}
</script>