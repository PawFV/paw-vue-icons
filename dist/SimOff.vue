<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon sim-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19,5A2,2 0 0,0 17,3H10L7.66,5.34L19,16.68V5M3.65,3.88L2.38,5.15L5,7.77V19A2,2 0 0,0 7,21H17C17.36,21 17.68,20.9 17.97,20.74L19.85,22.62L21.12,21.35L3.65,3.88Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SimOffIcon",
  props: {
    title: {
      type: String,
      default: "Sim Off icon"
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
