<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon shield-sync-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 21C8.25 20 5 15.54 5 11.22V6.3L12 3.18L19 6.3V12.07A6.45 6.45 0 0 1 20.91 12.67A11.63 11.63 0 0 0 21 11V5L12 1L3 5V11C3 16.55 6.84 21.74 12 23C12.35 22.91 12.7 22.8 13 22.68A6.3 6.3 0 0 1 12 21M18 14.5V13L15.75 15.25L18 17.5V16A2.5 2.5 0 0 1 20.24 19.62L21.33 20.71A4 4 0 0 0 18 14.5M18 21A2.5 2.5 0 0 1 15.76 17.38L14.67 16.29A4 4 0 0 0 18 22.5V24L20.25 21.75L18 19.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ShieldSyncOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Shield Sync Outline icon"
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
