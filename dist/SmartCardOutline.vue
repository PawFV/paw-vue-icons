<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon smart-card-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 3H2A2.07 2.07 0 0 0 0 5V19A2.07 2.07 0 0 0 2 21H22A2.07 2.07 0 0 0 24 19V5A2.07 2.07 0 0 0 22 3M22 19H2V5H22M14 17V15.75C14 14.09 10.66 13.25 9 13.25S4 14.09 4 15.75V17H14M9 7A2.5 2.5 0 1 0 11.5 9.5A2.5 2.5 0 0 0 9 7M15 10V13H19V10H15">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SmartCardOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Smart Card Outline icon"
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
