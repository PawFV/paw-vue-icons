<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon human-wheelchair-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8.5 4A2 2 0 0 1 6.5 6A2 2 0 0 1 4.5 4A2 2 0 0 1 6.5 2A2 2 0 0 1 8.5 4M5 7C3.89 7 3 7.89 3 9V15H5V22H8.61A7 7 0 0 1 6.5 17A7 7 0 0 1 10 10.95V9C10 7.89 9.11 7 8 7M13 8V16H18.5L21.2 19.6L22.8 18.4L19.5 14H15V8M12 12.23A5 5 0 0 0 8.5 17A5 5 0 0 0 13.5 22A5 5 0 0 0 18.5 17H16.5A3 3 0 0 1 13.5 20A3 3 0 0 1 10.5 17A3 3 0 0 1 12 14.41Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "HumanWheelchairIcon",
  props: {
    title: {
      type: String,
      default: "Human Wheelchair icon"
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
