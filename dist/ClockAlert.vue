<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon clock-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,2C16.46,2 20.26,4.95 21.54,9H18V20C16.33,21.25 14.25,22 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M16.2,16.2L17,14.9L12.5,12.2V7H11V13L16.2,16.2M20,11H22V18H20V11M20,20H22V22H20V20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ClockAlertIcon",
  props: {
    title: {
      type: String,
      default: "Clock Alert icon"
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
