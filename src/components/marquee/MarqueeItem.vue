<template>
  <div :class="classes">
    <slot></slot>
  </div>
</template>

<script>
export default {
  componentName: 'XMarqueeItem',
  computed: {
    classes () {
      return ['vx-marquee-item', 'swiper-slide']
    }
  }
}
</script>
