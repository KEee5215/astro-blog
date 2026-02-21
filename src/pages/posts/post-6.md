---
layout: ../../layouts/MarkdownPostLayout.astro
title: "react router 的路由跳转"
pubDate: 2026-02-21
description: "学了一些其他的路由知识"
author: "KEee"
image:
  url: "https://docs.astro.build/assets/rose.webp"
  alt: "The Astro logo on a dark background with a pink glow."
tags: ["react","react-router","路由"]
---
### 组件配置路由
```js
function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<AppLayout />}>
          <Route path="/home" element={<Home />} />
          <Route path="/about" element={<About />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
}
```
### 嵌套路由设置出口
```js
    <>
      <button onClick={toggle}>切换路由</button>
      <Outlet></Outlet>
    </>
```
### useNavigate(),切换路由api
```js
  const navigate = useNavigate();
  function toggle() {
    if (pathname === "/") {
      navigate("/about");
      return;
    }
    navigate("/");
  }
```
### useLocation(),路由路径api
```js
  const { pathname } = useLocation();//结构出来pathname,就是路径
```
### ok就说这么多




