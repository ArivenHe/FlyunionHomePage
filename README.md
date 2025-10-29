# 🚀 Vue 3 + Vite + GSAP + DaisyUI 项目模板

这是一个基于 **Vue 3 + Vite** 构建的现代前端项目模板，集成了动画库 **GSAP** 和 UI 框架 **DaisyUI**，助你快速搭建美观且动态的前端应用。

---

## 📦 技术栈

| 技术 | 说明 |
| :-- | :-- |
| [Vue 3](https://vuejs.org/) | 渐进式 JavaScript 框架 |
| [Vite](https://vitejs.dev/) | 极速的前端构建工具 |
| [GSAP](https://greensock.com/gsap/) | 高性能动画库 |
| [DaisyUI](https://daisyui.com/) | 基于 Tailwind CSS 的现代 UI 组件库 |
| [Tailwind CSS](https://tailwindcss.com/) | 原子化 CSS 框架 |

---

## 🧩 项目结构

```
├── src/
│   ├── assets/         # 静态资源
│   ├── components/     # 组件
│   ├── views/          # 页面
│   ├── App.vue         # 根组件
│   └── main.js         # 入口文件
├── index.html
├── package.json
├── vite.config.js
└── README.md
```

---

## ⚙️ 安装与运行

### 1️⃣ 克隆项目
```bash
git clone https://github.com/yourname/vue3-vite-gsap-daisyui.git
cd vue3-vite-gsap-daisyui
```

### 2️⃣ 安装依赖
```bash
npm install
```

### 3️⃣ 启动开发服务器
```bash
npm run dev
```
启动后访问：
👉 [http://localhost:5173](http://localhost:5173)

### 4️⃣ 构建生产环境
```bash
npm run build
```
构建完成后会生成 `dist` 文件夹，可直接部署到静态服务器。

---

## 🌈 示例动画

使用 **GSAP** 创建炫酷动画效果，例如：

```js
import { onMounted } from 'vue'
import { gsap } from 'gsap'

onMounted(() => {
  gsap.from('.title', {
    duration: 1.2,
    y: -50,
    opacity: 0,
    ease: 'bounce.out'
  })
})
```

```html
<h1 class="title text-4xl font-bold text-primary">Welcome to Vue 3 + GSAP!</h1>
```

---

## 💅 使用 DaisyUI 组件

```html
<button class="btn btn-primary">点击我</button>
<div class="card bg-base-200 shadow-xl p-4">
  <p>这是一个 DaisyUI 卡片组件。</p>
</div>
```

---

## 📖 学习资源

- [Vue 3 官方文档](https://vuejs.org/guide/introduction.html)
- [Vite 官方文档](https://vitejs.dev/guide/)
- [GSAP 官方文档](https://greensock.com/docs/)
- [DaisyUI 官方文档](https://daisyui.com/components/)

---

## 🧑‍💻 开发命令速查表

| 命令 | 说明 |
|------|------|
| `npm install` | 安装依赖 |
| `npm run dev` | 启动开发环境 |
| `npm run build` | 构建生产版本 |

---



## 📝 License

本项目基于 [MIT License](LICENSE) 开源，欢迎自由使用与修改。

---

## 🌍 GitHub 仓库

📦 访问项目仓库查看更多代码示例与更新日志：  
👉 [https://github.com/yourname/vue3-vite-gsap-daisyui](https://github.com/yourname/vue3-vite-gsap-daisyui)

---
**🎉 Happy Coding with Vue 3 + GSAP + DaisyUI + Vite!**

**©️ Copyright © 2025 AerionStudio. All Rights Reserved.**

