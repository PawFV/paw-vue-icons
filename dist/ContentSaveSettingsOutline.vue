<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon content-save-settings-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M7 22H9V24H7V22M11 22H13V24H11V22M15 22H17V24H15V22M17 2H5C3.89 2 3 2.9 3 4V18C3 19.1 3.89 20 5 20H19C20.1 20 21 19.1 21 18V6L17 2M19 18H5V4H16.17L19 6.83V18M12 11C10.34 11 9 12.34 9 14S10.34 17 12 17 15 15.66 15 14 13.66 11 12 11M6 5H15V9H6V5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ContentSaveSettingsOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Content Save Settings Outline icon"
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
