<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon leek-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10 2V5.55L12 7.55L14 5.55V2H10M6.34 4L3.87 6.5L15 17.62V12.67L6.34 4M17.66 4L13.06 8.61L15.54 11.09L20.13 6.5L17.66 4M9 13.74V20A2 2 0 0 0 11 22H13A2 2 0 0 0 15 20V19.74L13 17.74V20H11V15.74L9 13.74Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LeekIcon",
  props: {
    title: {
      type: String,
      default: "Leek icon"
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
