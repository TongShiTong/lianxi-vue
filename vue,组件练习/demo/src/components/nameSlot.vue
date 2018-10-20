<template>
    <div class="box clearfix">
      <div class="left-text">
        <slot></slot>
      </div>
      <div class="right-text">
        <slot name="right" :msg="changeText">{{text}}</slot>
      </div>
    </div>
</template>

<script>
    export default {
        name: "nameSlot",
      props: {
          text: String
      },
      computed: {
          changeText() {
            return this.text + '子组件的数据'
          }
      }
    }
</script>

<style scoped>
  .box {
    line-height: 40px;
    width: 400px;
    border: 1px solid #888;
    border-radius: 4px;
  }

  .left-text {
    padding-left: 10px;
    float: left;
    color: #333;
    font-size: 14px;
  }

  .right-text {
    padding-right: 10px;
    float: right;
    color: #555;
    font-size: 12px;
  }
</style>
