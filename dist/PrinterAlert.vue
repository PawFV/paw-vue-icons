<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon printer-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M14,4V8H6V4H14M15,13A1,1 0 0,0 16,12A1,1 0 0,0 15,11A1,1 0 0,0 14,12A1,1 0 0,0 15,13M13,19V15H7V19H13M15,9A3,3 0 0,1 18,12V17H15V21H5V17H2V12A3,3 0 0,1 5,9H15M22,7V12H20V7H22M22,14V16H20V14H22Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PrinterAlertIcon",
  props: {
    title: {
      type: String,
      default: "Printer Alert icon"
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
