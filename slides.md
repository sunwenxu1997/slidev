---
theme: default
class: content-end text-left
highlighter: prism
lineNumbers: true
routerMode: hash
drawings:
  persist: false
transition: slide-left
mdc: true
download: true
exportFilename: exported.pdf
title: GithubCopilot
---

# GithubCopilot

开发效率提升工具

<style>
.slidev-layout.slidev-page-1 {
  background-image:url("/pubilc/page1.jpg") !important;
  color: #5a5a5a !important;
}
p{
    text-transform:uppercase;
}
</style>

<!--
* 大家好，今天来的各位应该都是开发的同事，然后今天的主题是copilot，相信有的同事用过，有的没用过。这里就先简单讲一下copilot的由来
-->

---

# 
##

GitHub的首席执行官 [Thomas](https://github.blog/author/ashtom/) 在 **2022年6月21日** ，首次将 **Github Copilot** 面向个人开发者全面开放的公告。

<img src="/pubilc/1704691680302.jpg" class="m-auto mt-5 h-95">

<!--
这是托马斯在2022年6月21日发布的一则公告。大概意思就是顺应ai时代的到来，方方面面都受益于了大家，但是代码方面还以就是手动编写，不够完全智能，所以推出了copilot提供给开发人员，提高各位的开发效率。
-->

---

# 什么是 Github Copilot
##
<img src="/pubilc/1704698345259.jpg" class="h-80 m-auto my-10">

<v-click>

简单来说就是能帮助程序员提高代码方面的开发效率，完全展示了作为副驾驶员 ( **copilot** ) 的导航，协助的能力。

</v-click>

<!--
copilot有3大特点。
1.提供相匹配的代码编写建议；
2.大多开发者工具的兼容；
3.涉及领域广，尤其是在你不擅长的领域，也能帮你提供代码建议。
-->

---
transition: slide-up
---

# 如何使用 Copilot

##

目前 `Github Copilot`是收费的😔，对于个人开发用户也是个不小的开销。当然`Github Copilot`也提供了30天的免费试用体验😊，前提是你需要绑定 **信用卡** 或者 **PayPal**。

<img src="/pubilc/1704700226543.jpg" class="w-1/2 m-auto mt-10">

---

# 
##
🎉开通成功后，基于`VS Code工具`来讲的话。

1.直接登录已开通绑定的github账号；

2.在扩展市场下载对应的`Github Copilot` 插件；

3.等待右下角机器人🤖小图标正常显示时就能使用了。

<img src="/pubilc/1704702605209.jpg" class="h-80 m-auto">

---
transition: slide-up
layout: two-cols
---

# Copilot 自动化代码生成

简单实现一个案例：点击按钮随机更换背景颜色
<img src="/pubilc/button.gif" class="m-auto mt-5 h-100">

::right::

<div class="code">
```html {all|1,11,22,28,36,43,44|all}
<!-- 生成一个垂直水平居中的按钮 -->
<template>
  <div class="other">
    <div class="btn" @click="changeColor">
      <div class="btn-inner">
        <div class="btn-inner-inner">按钮</div>
      </div>
    </div>
  </div>
</template>
<!-- 给按钮添加一个点击事件，每次点击按钮，背景颜色就会随机改变 -->
<script>
export default {
  data() {
    return {
      color: '#fff'
    }
  },
  methods: {
    changeColor() {
      this.color = '#' + Math.floor(Math.random() * 0xffffff).toString(16)
      // 背景颜色改变
      this.$el.style.backgroundColor = this.color
    }
  }
}
</script>
<!-- 样式部分 -->
<style lang="scss" scoped>
.other {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  .btn {
    width: 200px;
    height: 50px;
    background: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px #ccc;
    cursor: pointer;
    user-select: none;
    .btn-inner {
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      .btn-inner-inner {
        font-size: 20px;
      }
    }
  }
}
</style>
```
</div>

<style>
  .code{
    height:31rem;
    overflow: auto;
  }
</style>

<!--
这里给大家展示一个小案例。
先看下代码量，差不多57行代码，也不是特别复杂的功能。让我们看下下面代码中哪些是通过copilot生成的。没错高亮的7行部分是我写的，其余50行全部是copilot建议生成的。占比很是惊人。怪不得copilot能说提升55%的效率。
-->

---

# 注释生成
##
通过编写注释，根据注释内容自动生成代码。
* 多用于简单js方法生成
* 简单的css布局样式等

<img src="/pubilc/code1.gif" class="m-auto mt-5 h-70">

---

# 自动填充生成
##
Copilot可以结合当前项目上下文，编写时会提前帮你 **预测** 出你想要的代码。
* 编写上半段代码，帮你生成下半段代码，节省 **55%** 的时间；
* 尤其是在你可能不擅长的领域，这种 **预测** 方式，可以优先帮你生成代码，然后你再去学习代码。(经常会给人一种意想不到的效果😮)
<img src="/pubilc/code2.gif" class="m-auto mt-5 h-60">


---
src: ./pages/end-page.md
---
