<template>
	<div
		class="hero min-h-screen "
		style="background-image: url('src/assets/paperwall_6.jpg')" >
		<div class="hero-overlay"></div>
		<div class="hero-content text-neutral-content text-center">
			<h1 class=" text-8xl font-bold" style="font-family: EDIX">Flyunion</h1>
		</div>
	</div>
	<div ref="productList" class="animate__animated ">
		<About />
	</div>
	<div ref="productList" class="animate__animated " >
		<People />
	</div>
	<div ref="productList" class="animate__animated " >
		<Product />
	</div>
	<div ref="productList" class="animate__animated " >
		<Platform />
	</div>
</template>

<script>
import ProductList from './ProductList.vue'
import About from "./About.vue";
import 'animate.css';
import People from "./People.vue";
import Platform from "./Platform.vue";
import Product from "./Product.vue";

export default {
	components: {
		ProductList,
		About,
		People,
		Platform,
		Product
	},
	data() {
		return {
			isAnimated: false
		};
	},
	methods: {
		handleScroll() {
			const productList = this.$refs.productList;
			const rect = productList.getBoundingClientRect();
			if (rect.top < window.innerHeight && rect.bottom > 0) {
				this.isAnimated = true;
			}
		}
	},
	mounted() {
		window.addEventListener('scroll', this.handleScroll);
	},
	beforeDestroy() {
		window.removeEventListener('scroll', this.handleScroll);
	}
}
</script>

<style scoped>
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
</style>
