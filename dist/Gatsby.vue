<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon gatsby-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M12,4C8.27,4 5.14,6.55 4.25,10L14,19.75C17.45,18.86 20,15.73 20,12H14.75V13.5H18.2C17.71,15.54 16.24,17.19 14.31,17.94L6.06,9.69C7,7.31 9.3,5.63 12,5.63C14.13,5.63 16,6.67 17.18,8.28L18.41,7.22C16.95,5.26 14.63,4 12,4M4,12A8,8 0 0,0 12,20C12.04,20 12.09,20 4,12Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "GatsbyIcon",
  props: {
    title: {
      type: String,
      default: "Gatsby icon"
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
