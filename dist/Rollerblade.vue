<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon rollerblade-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19,15C19,15 19,16 17,16C15,16 4,16 4,16V3H11L11.21,4.5H9.24V6H11.43L11.64,7.5H9.24V9H11.86L12,10H14C14,10 19,10 19,15M5.5,17A2.5,2.5 0 0,0 3,19.5A2.5,2.5 0 0,0 5.5,22A2.5,2.5 0 0,0 8,19.5A2.5,2.5 0 0,0 5.5,17M17.5,17A2.5,2.5 0 0,0 15,19.5A2.5,2.5 0 0,0 17.5,22A2.5,2.5 0 0,0 20,19.5A2.5,2.5 0 0,0 17.5,17M11.5,17A2.5,2.5 0 0,0 9,19.5A2.5,2.5 0 0,0 11.5,22A2.5,2.5 0 0,0 14,19.5A2.5,2.5 0 0,0 11.5,17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RollerbladeIcon",
  props: {
    title: {
      type: String,
      default: "Rollerblade icon"
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
