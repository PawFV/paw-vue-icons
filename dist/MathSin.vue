<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon math-sin-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4,7A2,2 0 0,0 2,9V11A2,2 0 0,0 4,13H6V15H2V17H6A2,2 0 0,0 8,15V13A2,2 0 0,0 6,11H4V9H8V7H4M14,7V9H13V15H14V17H10V15H11V9H10V7H14M16,7V17H18V12L20,17H22V7H20V12L18,7H16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MathSinIcon",
  props: {
    title: {
      type: String,
      default: "Math Sin icon"
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
