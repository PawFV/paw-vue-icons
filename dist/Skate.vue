<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon skate-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21.1,16.5C20.36,16.17 19.5,16.5 19.19,17.26C19.06,17.58 18.8,17.87 18.5,18H3V21H17.97C19.68,21 21.22,20 21.88,18.41C22.2,17.67 21.86,16.81 21.1,16.5M19,15C19,15 19,16 17,16C15,16 4,16 4,16V3H11L11.21,4.5H9.24V6H11.43L11.64,7.5H9.24V9H11.86L12,10H14C14,10 19,10 19,15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SkateIcon",
  props: {
    title: {
      type: String,
      default: "Skate icon"
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
