<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon cup-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M1,4.27L2.28,3L21,21.72L19.73,23L18.27,21.54C17.93,21.83 17.5,22 17,22H7C5.97,22 5.13,21.23 5,20.23L3.53,6.8L1,4.27M18.32,8L18.77,4H5.82L3.82,2H21L19.29,17.47L9.82,8H18.32Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CupOffIcon",
  props: {
    title: {
      type: String,
      default: "Cup Off icon"
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
