<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon ultra-high-definition-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M9,7H11V11H13V7H15V17H13V13H11V17H9V7M17,7H20A3,3 0 0,1 23,10V14A3,3 0 0,1 20,17H17V7M20,15A1,1 0 0,0 21,14V10A1,1 0 0,0 20,9H19V15H20M7,14A3,3 0 0,1 4,17A3,3 0 0,1 1,14V7H3V14A1,1 0 0,0 4,15A1,1 0 0,0 5,14V7H7V14Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "UltraHighDefinitionIcon",
  props: {
    title: {
      type: String,
      default: "Ultra High Definition icon"
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
