<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bell-circle-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M17,16H7V15L8,14V11.39C8,10.3 8.27,9.34 8.79,8.53C9.3,7.72 10.04,7.21 11,7V6.5A1,1 0 0,1 12,5.5A1,1 0 0,1 13,6.5V7C13.96,7.21 14.7,7.72 15.21,8.53C15.73,9.34 16,10.3 16,11.39V14L17,15V16M13.5,17A1.5,1.5 0 0,1 12,18.5A1.5,1.5 0 0,1 10.5,17H13.5M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M12,4A8,8 0 0,0 4,12A8,8 0 0,0 12,20A8,8 0 0,0 20,12A8,8 0 0,0 12,4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BellCircleOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Bell Circle Outline icon"
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
