<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon instrument-triangle-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M11.5 2H10.5V6.2C10.4 6.3 10.3 6.3 10.2 6.5L2.1 20.7C1.8 21.3 2.2 22 2.9 22H16V20H4.8L11 9.2L16.7 19.2L18.4 18.2L11.8 6.4L11.5 6.1V2M21 6H20V18L19.5 22H21.5L21 18V6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "InstrumentTriangleIcon",
  props: {
    title: {
      type: String,
      default: "Instrument Triangle icon"
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
