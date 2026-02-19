---
layout: ../../layouts/MarkdownPostLayout.astro
title: "由reactRouter的官网实例产生的一些小思考"
pubDate: 2026-02-19
description: "初次学习reactRouter,有些看不懂的地方"
author: "KEee"
image:
  url: "https://docs.astro.build/assets/rose.webp"
  alt: "The Astro logo on a dark background with a pink glow."
tags: ["react","react-router","路由"]
---

## 我貌似发现两种获取react router路由的属性的方法
### 第一种:使用loader函数获取
```
//先获取路由属性
export async function loader({ params }: Route.LoaderArgs) {
  let team = await fetchTeam(params.teamId);
  return { name: team.name };
}
//再传进去
export default function Team({ loaderData }: Route.ComponentProps) {
  return (
    <div>
      <h1>Welcome to My Route with Props!</h1>
      <p>Loader Data: {loaderData.name}</p>
    </div>
  );
}
```
### 第二种:直接在组件参数中解构出 loaderData、params
```
//直接写在组件函数中
export default function Team({ loaderData, params }: Route.ComponentProps) {
  return (
    <div>
      <h1>Welcome to My Route with Props!</h1>
      <p>Loader Data: {loaderData.name}</p>
      <p>Route Parameters: {params.teamId}</p>
    </div>
  );
}
```
## 这可能是版本的问题,
### AI说:使用loader函数是推荐的标准做法，不是多余的。如果只是简单页面，当然可以在组件里直接用参数获取数据，但在实际项目和最佳实践中，建议用 loader。
### 但是,当我把另一段官网给的实例代码(在组件参数中结构的)发给它,它又说:"这是新版 React Router/Remix 推荐的写法，更加简洁和类型安全"
