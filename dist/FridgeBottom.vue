<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fridge-bottom-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M7,2A2,2 0 0,0 5,4V19A2,2 0 0,0 7,21V22H9V21H15V22H17V21A2,2 0 0,0 19,19V4A2,2 0 0,0 17,2H7M8,6H10V8H8V6M7,11H17V19H7V11M8,12V15H10V12H8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FridgeBottomIcon",
  props: {
    title: {
      type: String,
      default: "Fridge Bottom icon"
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
