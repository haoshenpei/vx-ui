<template>
  <div :class="classes" @click="handleClick">
    <slot></slot>
  </div>
</template>

<script>
export default {
  componentName: 'SidebarItem',
  props: {
    name: {
      type: [Number, String, Object],
      required: true
    }
  },
  methods: {
    handleClick () {
      this.$emit('change', this.name)
    }
  },
  computed: {
    classes () {
      let array = ['vx-sidebar-item']
      if (this.$parent.active === this.name) {
        array.push('vx-sidebar-item-active')
        array.push(this.$parent.activeClass)
      }
      return array
    }
  }
}
</script>
