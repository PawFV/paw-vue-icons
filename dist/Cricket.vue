<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cricket-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14.34,17.77L15.75,16.36L20,20.58L18.56,22L14.34,17.77M18.5,2A3.5,3.5 0 0,1 22,5.5A3.5,3.5 0 0,1 18.5,9A3.5,3.5 0 0,1 15,5.5A3.5,3.5 0 0,1 18.5,2M2.24,7.11L5.07,4.28C5.46,3.89 6.09,3.89 6.5,4.28L14.97,12.77C15.36,13.16 15.36,13.79 14.97,14.18L12.14,17C11.75,17.4 11.12,17.4 10.72,17L2.24,8.53C1.85,8.13 1.85,7.5 2.24,7.11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CricketIcon",
  props: {
    title: {
      type: String,
      default: "Cricket icon"
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
