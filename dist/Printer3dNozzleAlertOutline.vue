<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon printer3d-nozzle-alert-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M7 2H17V7H19V13H16.5L13 17H11L7.5 13H5V7H7V2M10 22H2V20H10C10.55 20 11 19.55 11 19V18H13V19C13 20.66 11.66 22 10 22M7 9V11H8.5L12 15L15.5 11H17V9H15V4H9V9H7M21 12V7H23V12H21M21 16V14H23V16H21Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "Printer3dNozzleAlertOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Printer3d Nozzle Alert Outline icon"
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
