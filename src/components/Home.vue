<template>
	<div class="hero min-h-screen home">
		<div class="hero-overlay"></div>
		<div class="hero-content text-neutral-content text-center" ref="title">
			<h1 class="text-8xl font-bold" style="font-family: EDIX">Flyunion Studio</h1>
		</div>
	</div>
	<div ref="about" class="animate__animated opacity-0">
		<About />
	</div>
	<div ref="people" class="animate__animated opacity-0">
		<People />
	</div>
	<div ref="product" class="animate__animated opacity-0">
		<Product />
	</div>
	<div ref="productList" class="animate__animated opacity-0">
		<ProductList />
	</div>
	<div ref="platform" class="animate__animated opacity-0">
		<Platform />
	</div>
	<div ref="footer" class="animate__animated opacity-0">
		<Footer />
	</div>
</template>

<script>
import ProductList from './ProductList.vue'
import About from "./About.vue";
import 'animate.css';
import People from "./People.vue";
import Platform from "./Platform.vue";
import Product from "./Product.vue";
import Footer from "./Footer.vue";
import gsap from 'gsap';
import {ScrollTrigger} from 'gsap/ScrollTrigger';
import title from "./Title.vue";
gsap.registerPlugin(ScrollTrigger);

export default {
	components: {
		ProductList,
		About,
		People,
		Platform,
		Product,
		Footer,
		title
	},
	data() {
		return {
			isAnimated: false
		};
	},
	mounted() {
		this.setupAnimations();
	},
	methods: {
		setupAnimations() {
			// 标题动画
			gsap.to(this.$refs.title, {
				scrollTrigger: {
					trigger: this.$refs.title,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			// 其他部分动画
			gsap.to(this.$refs.about, {
				scrollTrigger: {
					trigger: this.$refs.about,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			gsap.to(this.$refs.people, {
				scrollTrigger: {
					trigger: this.$refs.people,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			gsap.to(this.$refs.product, {
				scrollTrigger: {
					trigger: this.$refs.product,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			gsap.to(this.$refs.productList, {
				scrollTrigger: {
					trigger: this.$refs.productList,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			gsap.to(this.$refs.platform, {
				scrollTrigger: {
					trigger: this.$refs.platform,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});

			gsap.to(this.$refs.footer, {
				scrollTrigger: {
					trigger: this.$refs.footer,
					start: "top 80%",
					end: "bottom 20%",
					toggleActions: "restart none reverse none",
				},
				y: 0,
				opacity: 1,
				scale: 1,
				rotation: 0,
				duration: 1,
				ease: "power1.out"
			});
		}
	},
	beforeDestroy() {
		ScrollTrigger.getAll().forEach(t => t.kill());
	}
}
</script>

<style scoped>
.home{
	background-image: url('../assets/paperwall_6.jpg')
}
.font-inter {
	font-family: 'EDIX', sans-serif;
}

/* 确保背景颜色铺满整个屏幕 */
.bg-base-200 {
	background-color: #000000; /* 替换为你需要的背景颜色 */
	height: 100vh;
	width: 100vw;
	margin: 0;
	padding: 0;
	overflow-y: auto; /* 允许垂直滚动 */
}

/* 初始状态设置为不可见 */
.opacity-0 {
	opacity: 0;
	transform: scale(0.9) rotate(-10deg);
	transition: opacity 1s, transform 1s; /* 添加过渡效果 */
}
</style>
