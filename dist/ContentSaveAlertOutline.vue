<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon content-save-alert-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 7V12H20V7H22M20 16H22V14H20V16M18 8V18C18 19.11 17.11 20 16 20H4C2.9 20 2 19.11 2 18V6C2 4.89 2.9 4 4 4H14L18 8M16 8.83L13.17 6H4V18H16V8.83M12 7H5V10H12V7M9.75 12.25C8.5 12.25 7.5 13.26 7.5 14.5S8.5 16.76 9.75 16.76 12 15.75 12 14.5 11 12.25 9.75 12.25Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ContentSaveAlertOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Content Save Alert Outline icon"
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
