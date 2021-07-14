---
layout:     post
title:      树上启发式合并
subtitle:   简单的例题及知识点
date:       2021-6-3
author:     weixi zhang
header-img: img/IMG_2830.JPG
catalog: false
tags:
    - 图论
---



<h3> 树上启发式合并-dsu on tree</h3>

<h5>前言：</h5>

处理子树统计问题的利器，时间复杂度<b>O(nlogn)</b>，以前学过一点，知道大概是用来处理什么东西的，但是在<b>2020CCPC长春站</b>

一道银(铜)牌题，知道大概怎么做，但是不会写，照着模板估计都得写很久，所以觉得应该系统的再复习复习。



先思考这样一个问题:

给定一棵有根树，1e5个点，每个节点上面都有颜色，你需要统计每个点的子树的不同颜色的个数。如果暴力的去统计每个点的子树，每统计完一个点的时候，都需要清空，那么时间复杂度是<b>O(n^2)</b>的。<u>对于某个节点<b>k</b>来说，当我们在统计它的儿子节点的时候，如果统计完了过后，再统计节点<b>k</b>的时候，其实对于刚才最后处理的儿子节点来说，其实没有必要清空，因为我们接下来要统计它的父亲<b>k</b>了。</u>这是没必要清空一遍了。很显然可以得出，我们最后处理儿子节点最大的那个<!--也就是重儿子-->的时候，是最优的。所以我们应该先处理轻儿子，然后清空，在处理重儿子。然后不清空，再把轻儿子的答案算上去。

$$
asdsad^2
$$

$$
\min \quad (\sum d_ef_e+P)/m\\
s.t. \quad \sum_{(v,s)\in G}f_e-\sum_{(s,v)\in G} f_e \ge -m\\
\quad \sum_{(v,t)\in G}f_e-\sum_{(t,v)\in G} f_e \ge m\\
\quad \sum_{(v,u)\in G}f_e-\sum_{(u,v)\in G} f_e \ge 0\\
\quad 0 \le f_e \le c_e\\
\quad m>0
$$

<img src="C:\Users\Administrator\Desktop\TP\)7J42UKZ@[8(ZX`PGVH)8KB.png" alt="图片未加载" >
