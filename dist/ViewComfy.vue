<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon view-comfy-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3,9H7V5H3V9M3,14H7V10H3V14M8,14H12V10H8V14M13,14H17V10H13V14M8,9H12V5H8V9M13,5V9H17V5H13M18,14H22V10H18V14M3,19H7V15H3V19M8,19H12V15H8V19M13,19H17V15H13V19M18,19H22V15H18V19M18,5V9H22V5H18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ViewComfyIcon",
  props: {
    title: {
      type: String,
      default: "View Comfy icon"
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
