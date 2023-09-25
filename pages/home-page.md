---
# 主题选择
theme: default
# 首页背景图片
# 提供的精美壁纸 https://source.unsplash.com/collection/94734566/1920x1080
background: /pubilc/page1.jpg
class: content-end text-left
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: slide-left
mdc: true
---



# PPT文档 演示标题

Document presentation report

<div class="pb-10">
  <span @click="$slidev.nav.next" class="py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">请按空格键查看下一页 <carbon:arrow-right class="inline"/>
  </span>
</div>

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
