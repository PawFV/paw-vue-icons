<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon scatter-plot-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M7,11A3,3 0 0,1 10,14A3,3 0 0,1 7,17A3,3 0 0,1 4,14A3,3 0 0,1 7,11M11,3A3,3 0 0,1 14,6A3,3 0 0,1 11,9A3,3 0 0,1 8,6A3,3 0 0,1 11,3M16.6,14.6C18.25,14.6 19.6,15.94 19.6,17.6A3,3 0 0,1 16.6,20.6C14.94,20.6 13.6,19.25 13.6,17.6A3,3 0 0,1 16.6,14.6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ScatterPlotIcon",
  props: {
    title: {
      type: String,
      default: "Scatter Plot icon"
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
