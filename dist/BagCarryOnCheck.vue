<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bag-carry-on-check-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15.28,16.69L18.14,13.88L18.84,14.58L15.28,18.14L13.17,16L13.88,15.28L15.28,16.69M8,21A2,2 0 0,1 6,19V9A2,2 0 0,1 8,7V21M9,7H14V4A2,2 0 0,1 12,2H16V10A6,6 0 0,1 22,16A6,6 0 0,1 16,22C14.77,22 13.63,21.63 12.68,21H9V7M16,12A4,4 0 0,0 12,16A4,4 0 0,0 16,20A4,4 0 0,0 20,16A4,4 0 0,0 16,12Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BagCarryOnCheckIcon",
  props: {
    title: {
      type: String,
      default: "Bag Carry On Check icon"
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
