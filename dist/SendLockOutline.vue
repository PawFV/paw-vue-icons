<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon send-lock-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M23 18V17.5C23 16.12 21.88 15 20.5 15S18 16.12 18 17.5V18C17.45 18 17 18.45 17 19V23C17 23.55 17.45 24 18 24H23C23.55 24 24 23.55 24 23V19C24 18.45 23.55 18 23 18M22 18H19V17.5C19 16.67 19.67 16 20.5 16S22 16.67 22 17.5V18M4 6.03L11.5 9.25L4 8.25L4 6.03M11.5 14.75L4 17.97V15.75L11.5 14.75M2 3L2 10L17 12L2 14L2 21L23 12L2 3Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SendLockOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Send Lock Outline icon"
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
