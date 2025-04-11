<script>
import arivenImg from "../assets/ariven.jpg"
import WilliamHeImg from "../assets/WilliamHe.jpg"
import XLiaovoImg from "../assets/XLiaovo.jpg"
import desuImg from "../assets/desu.jpg"
export default {
	name: "People",
	data() {
		return {
			peopleList: [
				{
					name: "Ariven",
					avatar: arivenImg,
					qq: "3208629021",
					email: "qq3208629021@outlook.com",
					introduction: "前端开发，软件开发工程师"
				},
				{
					name: "William He",
					avatar: WilliamHeImg,
					qq: "2084791301",
					email: "2084791301@qq.com",
					introduction: "FSD服务器，机载调频开发工程师"
				},
				{
					name: "XLiaovo",
					avatar: XLiaovoImg,
					qq: "2456666787",
					email: "2456666787@qq.com",
					introduction: "后端开发工程师"
				},
				{
					name: "空崎ヒナdesu",
					avatar: desuImg,
					qq: "850824385",
					email: "850824385@qq.com",
					introduction: "虚拟航司系统开发工程师"
				}
			]
		};
	}
};
</script>

<template>
	<div class="hero bg-base-200 min-h-screen">
		<div class="hero-content flex-col lg:flex-row-reverse">
			<div class="people-list">
				<h1 class="text-5xl font-bold custom-letter-spacing gradient-text mb-8">我们的成员</h1>
				<br>
				<div class="cards-container">
					<div v-for="(person, index) in peopleList" :key="index" class="person-card card bg-base-100 shadow-xxl">

						<br><figure>
							<img :src="person.avatar" :alt="person.name" class="avatar" />
						</figure>
						<div class="card-body">
							<h2 class="card-title">{{ person.name }}</h2>
							<p>QQ: {{ person.qq }}</p>
							<p>Email: {{ person.email }}</p>
							<p>{{ person.introduction }}</p>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<style scoped>
.people-list {
	display: flex;
	flex-direction: column; /* 确保内容按列排列 */
	align-items: center; /* 水平居中对齐 */
	padding: 20px;
}

.cards-container {
	display: flex;
	flex-wrap: wrap;
	gap: 20px;
	justify-content: center; /* 水平居中对齐卡片 */
}

.person-card {
	flex: 0 0 calc(25% - 20px); /* 每个卡片占25%宽度，减去间隔 */
	max-width: 300px; /* 最大宽度 */
	transition: transform 0.3s ease; /* 添加过渡效果 */
}

.person-card:hover {
	transform: scale(1.05); /* 鼠标悬停时放大 */
}

.avatar {
	width: 100px;
	height: 100px;
	border-radius: 50%;
	object-fit: cover;
	margin-right: 20px;
}

.custom-letter-spacing {
	letter-spacing: 2px; /* 你可以根据需要调整这个值 */
}

.gradient-text {
	background: linear-gradient(90deg, #ff7e5f, #feb47b); /* 你可以根据需要调整渐变颜色 */
	-webkit-background-clip: text;
	-webkit-text-fill-color: transparent;
}
</style>
