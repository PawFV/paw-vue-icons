<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon rowing-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8.5,14.5L4,19L5.5,20.5L9,17H11L8.5,14.5M15,1A2,2 0 0,0 13,3A2,2 0 0,0 15,5A2,2 0 0,0 17,3A2,2 0 0,0 15,1M21,21L18,24L15,21V19.5L7.91,12.41C7.6,12.46 7.3,12.5 7,12.5V10.32C8.66,10.35 10.61,9.45 11.67,8.28L13.07,6.73C13.26,6.5 13.5,6.35 13.76,6.23C14.05,6.09 14.38,6 14.72,6H14.75C16,6 17,7 17,8.26V14C17,14.85 16.65,15.62 16.08,16.17L12.5,12.59V10.32C11.87,10.84 11.07,11.34 10.21,11.71L16.5,18H18L21,21Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RowingIcon",
  props: {
    title: {
      type: String,
      default: "Rowing icon"
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
