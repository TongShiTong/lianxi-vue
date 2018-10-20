<template>
  <div>
    <h1>首页</h1>
    <my-btn type="primary">我的按钮</my-btn>
    <name-slot :text="msg">
      <template>标题</template>
      <!--作用域插槽，渲染你加工过的数据，不用的话传什么就显什么-->
      <!--<template slot="right" slot-scope="scope">-->
        <!--<h1>-->
          <!--{{scope.msg}}-->
        <!--</h1>-->
      <!--</template>-->
    </name-slot>
  </div>
</template>

<script>
  import myBtn from '@/components/my-btn'
  import nameSlot from '@/components/nameSlot'
    export default {
      components: {
        myBtn,
        nameSlot
      },
      data() {
        return {
          msg: '父组件的按钮'
        }
      }
    }
</script>

<style scoped>

</style>
