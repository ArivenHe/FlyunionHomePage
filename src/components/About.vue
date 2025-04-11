<template>
	<div class="hero bg-base-200 min-h-screen">
		<div class="hero-content flex-col lg:flex-row-reverse">
			<div>
				<h1 class="text-5xl font-bold custom-letter-spacing gradient-text">关于我们</h1>
				<h2 ref="h2Element" class="py-6 text-4xl custom-letter-spacing custom-line-height opacity-0" style="transform: translateX(-100px); color: #000;">
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

<script>
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';

gsap.registerPlugin(ScrollTrigger);

export default {
	mounted() {
		this.setupAnimations();
	},
	methods: {
		setupAnimations() {
			// 动画1：H2标签从左侧滑入并改变颜色
			gsap.to(this.$refs.h2Element, {
				scrollTrigger: {
					trigger: this.$refs.h2Element,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				x: 0, // 水平移动到原位
				opacity: 1, // 透明度变为1
				color: "#ffffff", // 改变颜色为红色
				scale: 1, // 缩放比例变为1
				rotation: 0, // 旋转角度变为0
				duration: 2, // 动画持续时间为2秒
				ease: "power1.out" // 缓动效果
			});

		},
		goto() {
			window.location.href = "http://qm.qq.com/cgi-bin/qm/qr?_wv=1027&k=9LN2BzklVawtrMOc7ts6V2gWY8ax5PO-&authKey=dDym3UH7JkYUomI67zkraVUbFlmyhQLK1%2FETFPGSPb4jVq5c4lxsTfJYbuWcZp%2FT&noverify=0&group_code=805902191";
		}
	},
	beforeDestroy() {
		ScrollTrigger.getAll().forEach(t => t.kill());
	}
};
</script>

<style scoped>
.custom-letter-spacing {
	letter-spacing: 2px; /* 字母间距 */
}

.custom-line-height {
	line-height: 1.6; /* 行高 */
}

.gradient-text {
	background-image: radial-gradient(circle 248px at center, #16d9e3 0%, #30c7ec 47%, #46aef7 100%);
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}

/* 初始状态设置 */
.opacity-0 {
	opacity: 0;
	transform: translateX(-100px);
	color: #000;
}

/* 按钮样式 */

</style>
