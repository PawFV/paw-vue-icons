<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon key-arrow-right-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10.7 6C10.1 4.2 8.4 3 6.5 3C4 3 2 5 2 7.5S4 12 6.5 12C8.5 12 10.1 10.8 10.7 9H15V12H18V9H22V6H10.7M6.5 9C5.7 9 5 8.3 5 7.5S5.7 6 6.5 6 8 6.7 8 7.5 7.3 9 6.5 9M13 21V19H8V17H13V15L16 18L13 21">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "KeyArrowRightIcon",
  props: {
    title: {
      type: String,
      default: "Key Arrow Right icon"
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
