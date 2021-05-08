<template>
  <div>
    <p>文字处理</p>
    <div>禁止复制</div>
    <div class="forbid-copy" @contextmenu="forbidContentMenu">
      禁止复制禁止复制禁止复制禁止复制禁止复制禁止复制禁止复制禁止复制
<!-- todo 行内url处理  ~assets/logo.png   @/assets/logo.png  不能生效； vue.config.js 好像没有被用到    -->
      <img src="src/assets/logo.png" alt="" style="width: 50px" class="img-forbid-copy">
    </div>
  </div>
</template>

<script>
export default {
name: "home",
  methods:{
    forbidContentMenu(e){
      e.preventDefault()
    }
  }
}
</script>

<style scoped>
.forbid-copy{
  /*禁止选中内容*/
  user-select:none;
  /*无法选中*/
  /**/
}
.img-forbid-copy{
  pointer-events:none;
}
</style>
