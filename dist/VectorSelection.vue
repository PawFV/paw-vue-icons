<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon vector-selection-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3,1H5V3H3V5H1V3A2,2 0 0,1 3,1M14,1A2,2 0 0,1 16,3V5H14V3H12V1H14M20,7A2,2 0 0,1 22,9V11H20V9H18V7H20M22,20A2,2 0 0,1 20,22H18V20H20V18H22V20M20,13H22V16H20V13M13,9V7H16V10H14V9H13M13,22V20H16V22H13M9,22A2,2 0 0,1 7,20V18H9V20H11V22H9M7,16V13H9V14H10V16H7M7,3V1H10V3H7M3,16A2,2 0 0,1 1,14V12H3V14H5V16H3M1,7H3V10H1V7M9,7H11V9H9V11H7V9A2,2 0 0,1 9,7M16,14A2,2 0 0,1 14,16H12V14H14V12H16V14Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "VectorSelectionIcon",
  props: {
    title: {
      type: String,
      default: "Vector Selection icon"
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
