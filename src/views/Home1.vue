<!--<template>
  <div class="home">
    <glx></glx>
    <img class='svg' src="../assets/svg/wechat.svg" alt="">
    <glButton></glButton>
  </div>
</template>-->

<script>
import glButton from '../componets/gl-button'

export default {
  name: 'Home',
  // components: {
  //   glButton
  // },
  render (h) {
    const root = h(glButton, {
      nativeOn: {
        click: () => {
          console.log('xxxxxx')
        }
      },
      children: [
        {
          tag: 'label',
          properties: {
            attrs: { id: 'myLabel' },
            domProps: { innerHTML: '输入框： ' }
          }
        },
        {
          tag: 'input',
          properties: {
            attrs: { id: 'myInput', value: 'hello~~' }
          },
          on: { change: this.handleChange }
        }
      ],
      attrs: {
        id: 2
      },
      on: {
        cb: () => {
          console.log('object')
        }
      },
      scopedSlots: {
        default: h('h1', 'xxx')
      }
    }, [h('h2', { slot: 'cc' }, 'gg'), h('h2', { slot: 'cc2' }, 'gg'), (<div>xxxxxx</div>)])
    return root
  }
}
</script>

<style scoped>
  .svg {
    fill: red;
    width: 50px;
  }

  .container {
    background-color: red;
  }
</style>
