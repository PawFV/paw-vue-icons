<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon surround-sound20-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M17,7H19A2,2 0 0,1 21,9V15A2,2 0 0,1 19,17H17A2,2 0 0,1 15,15V9A2,2 0 0,1 17,7M17,9V15H19V9H17M9,17H3V15L7,9H3V7H7A2,2 0 0,1 9,9C9,9.42 8.87,9.81 8.65,10.13L5.41,15H9V17M12,17A1,1 0 0,1 11,16A1,1 0 0,1 12,15A1,1 0 0,1 13,16A1,1 0 0,1 12,17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SurroundSound20Icon",
  props: {
    title: {
      type: String,
      default: "Surround Sound20 icon"
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
