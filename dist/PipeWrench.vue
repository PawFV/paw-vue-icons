<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon pipe-wrench-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M16.17 5.63L14.06 7.78L11.91 5.63L16.17 1.41L19.69 4.92C20.86 6.09 20.86 8 19.69 9.19L16.17 5.63M4.83 12.7L7 14.81L10.5 11.3L8.39 9.19L4.83 12.7M15.47 7.78L19 11.3L17.58 12.7L16.88 12L6.23 22.59L3.42 19.78L11.91 11.3L7.69 7.03L9.8 4.92L14.06 9.19L15.47 7.78Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PipeWrenchIcon",
  props: {
    title: {
      type: String,
      default: "Pipe Wrench icon"
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
