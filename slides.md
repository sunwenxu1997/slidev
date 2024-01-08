---
# 主题选择
theme: default
# 首页背景图片
# 提供的精美壁纸 https://source.unsplash.com/collection/94734566/1920x1080
# background: /pubilc/page1.jpg
class: content-end text-left
highlighter: prism 
lineNumbers: true
routerMode: hash
drawings:
  persist: false
transition: slide-left
mdc: true
---

# GithubCopilot

开发效率提升工具

<!-- <div class="pb-10">
  <span @click="$slidev.nav.next" class="py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10"> <carbon:arrow-right class="inline"/>
  </span>
</div> -->

<!--
每张幻灯片的最后一个注释块将被视为幻灯片注释。它将在演示者模式下与幻灯片一起显示和编辑。 [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

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
* 最后部分的注释可以在演讲模式下只针对你个人展示出来
* 没错，是这样的
-->
---

# 
##

GitHub的首席执行官 [Thomas](https://github.blog/author/ashtom/) 在 **2022年6月21日** ，首次将 **Github Copilot** 面向个人开发者全面开放的公告。

<img src="/pubilc/1704691680302.jpg" class="m-auto mt-5 h-95">
<!--
您可以在markdown中使用“style”标签来覆盖当前页面的样式。
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<!--
每一页的最后的注释或评论部分都可以在演讲模式下只针对你个人展示出来
-->
---


# 什么是 Github Copilot
##
<img src="/pubilc/1704698345259.jpg" class="h-80 m-auto my-10">

<v-click>

简单来说就是能帮助程序员提高代码方面的开发效率，完全展示了作为副驾驶员 ( **copilot** ) 的导航，协助的能力。

</v-click>
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
让我们看下下面代码中哪些是通过copilot生成的
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