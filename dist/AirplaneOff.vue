<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon airplane-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M3.15,5.27L8.13,10.26L2.15,14V16L10.15,13.5V19L8.15,20.5V22L11.65,21L15.15,22V20.5L13.15,19V15.27L18.87,21L20.15,19.73L4.42,4M13.15,9V3.5A1.5,1.5 0 0,0 11.65,2A1.5,1.5 0 0,0 10.15,3.5V7.18L17.97,15L21.15,16V14L13.15,9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "AirplaneOffIcon",
  props: {
    title: {
      type: String,
      default: "Airplane Off icon"
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
