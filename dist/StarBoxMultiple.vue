<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon star-box-multiple-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4 6V20H18V22H3C2.4 22 2 21.6 2 21V6H4M8 2H20C21.11 2 22 2.9 22 4V16C22 17.11 21.11 18 20 18H8C6.9 18 6 17.11 6 16V4C6 2.9 6.9 2 8 2M16.3 13.3L15.9 10.7L17.8 8.8L15.2 8.4L14 6L12.8 8.4L10.2 8.8L12.1 10.6L11.6 13.2L14 12L16.3 13.3Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "StarBoxMultipleIcon",
  props: {
    title: {
      type: String,
      default: "Star Box Multiple icon"
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
