<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon printer-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6,3V4.18L8.82,7H18V3H6M2.28,3L1,4.27L4.75,8C3.19,8.15 2,9.44 2,11V17H6V21H17.73L19.73,23L21,21.72L2.28,3M9.82,8L18.82,17H22V11A3,3 0 0,0 19,8H9.82M19,10A1,1 0 0,1 20,11A1,1 0 0,1 19,12A1,1 0 0,1 18,11A1,1 0 0,1 19,10M8,14H10.73L15.73,19H8V14Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PrinterOffIcon",
  props: {
    title: {
      type: String,
      default: "Printer Off icon"
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
