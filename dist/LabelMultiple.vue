<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon label-multiple-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4 19H13L11 21H4C3.5 21 2.97 20.79 2.59 20.41C2.21 20.03 2 19.5 2 19V9H4V19M17.63 5.84C17.27 5.33 16.67 5 16 5H8C6.9 5 6 5.9 6 7V15C6 16.1 6.9 17 8 17H16C16.67 17 17.27 16.66 17.63 16.15L22 11L17.63 5.84Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LabelMultipleIcon",
  props: {
    title: {
      type: String,
      default: "Label Multiple icon"
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
