<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cellphone-settings-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M16,16H8V4H16M16,0H8A2,2 0 0,0 6,2V18A2,2 0 0,0 8,20H16A2,2 0 0,0 18,18V2A2,2 0 0,0 16,0M15,24H17V22H15M11,24H13V22H11M7,24H9V22H7V24Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CellphoneSettingsIcon",
  props: {
    title: {
      type: String,
      default: "Cellphone Settings icon"
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
