<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cloud-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19,20H6C2.71,20 0,17.29 0,14C0,10.9 2.34,8.36 5.35,8.03C6.6,5.64 9.11,4 12,4C15.64,4 18.67,6.59 19.35,10.03C21.95,10.22 24,12.36 24,15C24,17.74 21.74,20 19,20M11,15V17H13V15H11M11,13H13V8H11V13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CloudAlertIcon",
  props: {
    title: {
      type: String,
      default: "Cloud Alert icon"
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
