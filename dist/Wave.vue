<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon wave-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20,12C18.61,12 17.22,11.53 16,10.67C13.56,12.38 10.44,12.38 8,10.67C6.78,11.53 5.39,12 4,12H2V14H4C5.37,14 6.74,13.65 8,13C10.5,14.3 13.5,14.3 16,13C17.26,13.65 18.62,14 20,14H22V12">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "WaveIcon",
  props: {
    title: {
      type: String,
      default: "Wave icon"
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
