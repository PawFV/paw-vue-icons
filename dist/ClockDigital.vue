<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon clock-digital-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2,6A2,2 0 0,0 0,8V16A2,2 0 0,0 2,18H22A2,2 0 0,0 24,16V8A2,2 0 0,0 22,6M2,8H22V16H2M3,9V10.5H6.25L3,15H4.75L8,10.5V9M9.25,9V10.5H10.75V9M12,9V10.5H13.5V15H15V9M17,9A1,1 0 0,0 16,10V14A1,1 0 0,0 17,15H20A1,1 0 0,0 21,14V10A1,1 0 0,0 20,9M17.5,10.5H19.5V13.5H17.5M9.25,13.5V15H10.75V13.5">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ClockDigitalIcon",
  props: {
    title: {
      type: String,
      default: "Clock Digital icon"
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
