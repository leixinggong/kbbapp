
<script>
export default {
  inheritAttrs: false,
  data () {
    return {
      value: 12
    }
  },
  render (h) {
    const root = h('div', this.$slots.default)
    const self = this
    setTimeout(() => {
      const ch = self.$children
      console.log(ch)
    }, 2000)
    return root
  }
}
</script>

<style lang="scss" scoped>

</style>
