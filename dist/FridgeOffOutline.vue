<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fridge-off-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22.11 21.46L2.39 1.73L1.11 3L5 6.89V19C5 20.11 5.9 21 7 21V22H9V21H15V22H17V21C17.58 21 18.1 20.75 18.46 20.35L20.84 22.73L22.11 21.46M17 19H7V11H9.11L17 18.89V19M7.2 4L5.7 2.5C6.05 2.19 6.5 2 7 2H17C18.11 2 19 2.9 19 4V15.8L17 13.8V11H14.2L12.2 9H17V4H7.2M8 12H10V15H8V12Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FridgeOffOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Fridge Off Outline icon"
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
