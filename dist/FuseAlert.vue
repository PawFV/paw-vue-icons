<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fuse-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6 7V17H13V7H6M9.16 16V12.87H7.41L9.91 8V11.14H11.59L9.16 16M14 2V6H5V2C5 1.45 5.45 1 6 1H13C13.55 1 14 1.45 14 2M14 18V22C14 22.55 13.55 23 13 23H6C5.45 23 5 22.55 5 22V18H14M19 13H17V7H19V13M19 17H17V15H19V17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FuseAlertIcon",
  props: {
    title: {
      type: String,
      default: "Fuse Alert icon"
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
