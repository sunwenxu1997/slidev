---
layout: center
class: text-center
---

#

<div class="code">
```html {all|1,11,22,28,36,43,44|1-6|9|all}
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
    height:50vh;
    overflow: auto;
  }
</style>
<!-- 
让我们看下下面代码中哪些是通过copilot生成的
 -->