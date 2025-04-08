<script >
export default {
	methods: {
		goto() {
			window.location.href = "http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=9LN2BzklVawtrMOc7ts6V2gWY8ax5PO-&authKey=dDym3UH7JkYUomI67zkraVUbFlmyhQLK1%2FETFPGSPb4jVq5c4lxsTfJYbuWcZp%2FT&noverify=0&group_code=805902191";
		}
	}
};
</script>

<template>
	<div class="hero bg-base-200 min-h-screen">
		<div class="hero-content flex-col lg:flex-row-reverse">

			<div>
				<h1 class="text-5xl font-bold custom-letter-spacing gradient-text">关于我们</h1>
				<h2 class="py-6 text-4xl custom-letter-spacing custom-line-height">
					我们是一家专门为模拟飞行平台提供软件开发的公司。<br>
					我们拥有 experienced 开发人员，他们拥有丰富的开发经验，<br>
					并且拥有良好的沟通 skills，<br>
					并且能够很好的与客户进行沟通。
				</h2>
				<button class="btn btn-primary" @click="goto">联系我们</button>
			</div>
		</div>
	</div>
</template>

<style scoped>
.custom-letter-spacing {
	letter-spacing: 2px; /* 你可以根据需要调整这个值 */
}

.custom-line-height {
	line-height: 1.6; /* 你可以根据需要调整这个值 */
}

.gradient-text {
	background-image: radial-gradient(circle 248px at center, #16d9e3 0%, #30c7ec 47%, #46aef7 100%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}
</style>
