<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon content-save-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 12H20V7H22M22 14H20V16H22M14 4H4A2 2 0 0 0 2 6V18A2 2 0 0 0 4 20H16A2 2 0 0 0 18 18V8M4 6H12V9H4M10 18A2.5 2.5 0 1 1 12.5 15.5A2.5 2.5 0 0 1 10 18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ContentSaveAlertIcon",
  props: {
    title: {
      type: String,
      default: "Content Save Alert icon"
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
