<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon car-door-lock-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21 3H11L3 11V12H4.5C7.5 12 10 14.91 10 18.5V21H22V4A1 1 0 0 0 21 3M19 16H16V14H19M20 11H5.83L11.83 5H20M7 17V16.5A2.5 2.5 0 0 0 2 16.5V17A1 1 0 0 0 1 18V22A1 1 0 0 0 2 23H7A1 1 0 0 0 8 22V18A1 1 0 0 0 7 17M6.2 17H2.8V16.5A1.7 1.7 0 0 1 6.2 16.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CarDoorLockIcon",
  props: {
    title: {
      type: String,
      default: "Car Door Lock icon"
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
