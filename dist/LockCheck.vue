<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon lock-check-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18 8C19.1 8 20 8.89 20 10V20C20 21.1 19.1 22 18 22H6C4.89 22 4 21.1 4 20V10C4 8.89 4.89 8 6 8H7V6C7 3.24 9.24 .998 12 .998C14.76 .998 17 3.24 17 6V8H18M12 3C10.34 3 9 4.34 9 6V8H15V6C15 4.34 13.66 3 12 3M11 19L17.25 12.76L15.84 11.35L11 16.18L8.41 13.6L7 15L11 19Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LockCheckIcon",
  props: {
    title: {
      type: String,
      default: "Lock Check icon"
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
