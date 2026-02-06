---
layout: ../../layouts/MarkdownPostLayout.astro
title: "二叉树的遍历"
pubDate: 2026-02-06
description: "二叉树的初步了解。"
author: "KEee"
image:
  url: "https://labuladong.online/images/algo/binary-tree-summary/2.jpeg"
  alt: "img from labuladong.online"
tags: ["数据结构","算法","二叉树"]
---
## 二叉树的常见的类型
### 满二叉树
满二叉树就是**每一层**节点都是满的，整棵树像一个正三角形

满二叉树有个优势，就是它的节点个数很好算。假设深度为 h，那么总节点数就是** 2^h - 1**
### 完全二叉树
完全二叉树是指，二叉树的每一层的节点都紧凑靠左排列，**且除了最后一层，其他每层都必须是满的**

### 二叉搜索树
二叉搜索树（Binary Search Tree，简称 BST）是一种很常见的二叉树，它的定义是：

对于树中的每个节点，其左子树的每个节点的值都要小于这个节点的值，右子树的每个节点的值都要大于这个节点的值。你可以简单记为「左小右大」。

**BST 是非常常用的数据结构。因为左小右大的特性，可以让我们在 BST 中快速找到某个节点，或者找到某个范围内的所有节点，这是 BST 的优势所在。**
