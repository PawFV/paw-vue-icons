<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon beaker-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3,3H21V5A2,2 0 0,0 19,7V19A2,2 0 0,1 17,21H7A2,2 0 0,1 5,19V7A2,2 0 0,0 3,5V3M7,5V7H12V8H7V9H10V10H7V11H10V12H7V13H12V14H7V15H10V16H7V19H17V5H7Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BeakerOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Beaker Outline icon"
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
