<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon video-input-scart-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.6 2.2L17.3 2.4L13.8 4.4L13.3 3.5L2 10V17H3V19C3 20.1 3.9 21 5 21H15C16.1 21 17 20.1 17 19V17H18V10H17L16.8 9.6L20.3 7.6L22.1 4.8L20.6 2.2M15 17V19H5V17H15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "VideoInputScartIcon",
  props: {
    title: {
      type: String,
      default: "Video Input Scart icon"
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
