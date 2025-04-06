<template>
	<div class="hero bg-base-200 min-h-screen">
		<h1>我们的客户</h1>
		<div class="carousel-label">
			<span>轮播</span>
		</div>
		<div class="carousel-container relative w-full">
			<!-- 轮播内容 -->
			<div class="carousel w-full" ref="carousel">
				<div id="slide1" class="carousel-item relative w-full">
					<img
						src="https://img.daisyui.com/images/stock/photo-1625726411847-8cbb60cc71e6.webp"
						class="w-full" />
				</div>
				<div id="slide2" class="carousel-item relative w-full">
					<img
						src="https://img.daisyui.com/images/stock/photo-1609621838510-5ad474b7d25d.webp"
						class="w-full" />
				</div>
				<div id="slide3" class="carousel-item relative w-full">
					<img
						src="https://img.daisyui.com/images/stock/photo-1414694762283-acccc27bca85.webp"
						class="w-full" />
				</div>
				<div id="slide4" class="carousel-item relative w-full">
					<img
						src="https://img.daisyui.com/images/stock/photo-1665553365602-b2fb8e5d1707.webp"
						class="w-full" />
				</div>
			</div>
		</div>

	</div>
</template>

<script>
export default {
	name: "Platform",
	data() {
		return {
			currentSlide: 1,
			slideInterval: null,
		};
	},
	mounted() {
		this.startAutoSlide();
		this.startScrollText(); // 启动文字滚动
	},
	beforeDestroy() {
		this.stopAutoSlide();
		this.stopScrollText(); // 停止文字滚动
	},
	methods: {
		startAutoSlide() {
			this.slideInterval = setInterval(() => {
				this.nextSlide();
			}, 3000); // 每3秒切换一次
		},
		stopAutoSlide() {
			clearInterval(this.slideInterval);
		},
		nextSlide() {
			this.currentSlide = this.currentSlide === 4 ? 1 : this.currentSlide + 1;
			this.updateSlide();
		},
		prevSlide() {
			this.currentSlide = this.currentSlide === 1 ? 4 : this.currentSlide - 1;
			this.updateSlide();
		},
		updateSlide() {
			const carousel = this.$refs.carousel;
			const slides = carousel.querySelectorAll('.carousel-item');
			slides.forEach((slide, index) => {
				slide.style.display = index + 1 === this.currentSlide ? 'block' : 'none';
			});
		},
		startScrollText() {
			const scrollingTexts = document.querySelectorAll('.scrolling-text p');
			scrollingTexts.forEach((text) => {
				text.scrollLeft = 0; // 初始化滚动位置
				const scrollInterval = setInterval(() => {
					text.scrollLeft += 1; // 每次滚动1像素
				}, 20); // 每20毫秒滚动一次
				text.dataset.intervalId = scrollInterval; // 存储定时器ID
			});
		},
		stopScrollText() {
			const scrollingTexts = document.querySelectorAll('.scrolling-text p');
			scrollingTexts.forEach((text) => {
				clearInterval(text.dataset.intervalId); // 停止滚动
			});
		},
	},
};
</script>

<style scoped>
.carousel-item {
	display: none;
}
.carousel-item:first-child {
	display: block;
}
.carousel-label {
	background-color: rgba(0, 0, 0, 0.5); /* 背景颜色和透明度 */
	color: white; /* 文字颜色 */
	padding: 10px 20px; /* 内边距 */
	border-radius: 5px; /* 圆角 */
	display: inline-block; /* 使背景只包裹文字 */
	margin-bottom: 20px; /* 底部外边距 */
}

/* 轮播容器样式 */
.carousel-container {
	position: relative;
	overflow: hidden;
	height: 500px; /* 设置轮播图高度 */
}

.scrolling-text {
	display: flex;
	animation: scroll 10s linear infinite; /* 使用CSS动画实现滚动 */
}

@keyframes scroll {
	0% {
		transform: translateX(100%);
	}
	100% {
		transform: translateX(-100%);
	}
}
</style>
