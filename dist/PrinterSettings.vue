<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon printer-settings-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18,2V6H6V2H18M19,11A1,1 0 0,0 20,10A1,1 0 0,0 19,9A1,1 0 0,0 18,10A1,1 0 0,0 19,11M16,18V13H8V18H16M19,7A3,3 0 0,1 22,10V16H18V20H6V16H2V10A3,3 0 0,1 5,7H19M15,24V22H17V24H15M11,24V22H13V24H11M7,24V22H9V24H7Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PrinterSettingsIcon",
  props: {
    title: {
      type: String,
      default: "Printer Settings icon"
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
