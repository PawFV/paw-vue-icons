<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon sausage-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3.5,3H9.5L7.96,5.32C9.16,5.87 10,7.09 10,8.5A5.5,5.5 0 0,0 15.5,14C16.91,14 18.13,14.84 18.68,16.04L21,14.5V20.5L18.68,18.96C18.13,20.16 16.91,21 15.5,21A12.5,12.5 0 0,1 3,8.5C3,7.09 3.84,5.87 5.04,5.32L3.5,3Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SausageIcon",
  props: {
    title: {
      type: String,
      default: "Sausage icon"
    },
    decorative: {
      type: Boolean,
      default: false
    },
    fillColor: {
      type: String,
      default: "currentColor"
    },
    size: {
      type: Number,
      default: 24
    }
  }
}
</script>
