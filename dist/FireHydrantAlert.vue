<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fire-hydrant-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 7H20V13H22V7M22 15H20V17H22V15M3 15V14H2V12H3V11H5V15H3M17 12V11H15V15H17V14H18V12H17M16 6H13.86C13.5 4.6 12.4 3.5 11 3.14V2H9V3.14C7.6 3.5 6.5 4.6 6.14 6H4V8H16V6M16 22H4C4 20.9 4.89 20 6 20V9H14V20C15.11 20 16 20.9 16 22M8 13C8 14.11 8.9 15 10 15S12 14.11 12 13 11.11 11 10 11 8 11.9 8 13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FireHydrantAlertIcon",
  props: {
    title: {
      type: String,
      default: "Fire Hydrant Alert icon"
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
