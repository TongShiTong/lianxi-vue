<template>
  <button class="my-btn" :class="bindClass">
    <slot></slot>
  </button>
</template>

<script>
    export default {
      name: "my-btn",
      props: {
        text: String,
        type: {
          type: String,
          default: ''
        }
      },
      computed: {
        bindClass() {
          switch (this.type) {
            case 'primary':
              return 'my-btn-primary'
            default:
              return ''
          }
        }
      }
    }
</script>

<style scoped>
  .my-btn {
    -webkit-appearance: none;
    line-height: 1;
    color: #343434;
    font-size: 14px;
    border: 1px solid #e8e8e8;
    border-radius: 4px;
    padding: 12px 20px;
    background: #fff;
    outline: none;
    transition: .1s;
  }
  .my-btn:active {
    background: #409eff;
    color: #fff;
  }

  .my-btn-primary {
    background: #409eff;
    border-color: #409eff;
    color: #fff;
  }

  .my-btn-primary:active {
    background-color: #50eeff;
  }
</style>
