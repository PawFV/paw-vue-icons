<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon flask-empty-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.8 22.7L19.6 21.5C19.1 21.8 18.6 22 18 22H6C4.3 22 3 20.7 3 19C3 18.4 3.2 17.8 3.5 17.4L7.9 9.8L1.1 3L2.4 1.7L22.1 21.4L20.8 22.7M15 7.8V6C15.6 6 16 5.6 16 5V4C16 2.9 15.1 2 14 2H10C8.9 2 8 2.9 8 4V4.8L20.4 17.2L15 7.8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FlaskEmptyOffIcon",
  props: {
    title: {
      type: String,
      default: "Flask Empty Off icon"
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
