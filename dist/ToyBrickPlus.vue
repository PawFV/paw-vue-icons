<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon toy-brick-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 6V5A2 2 0 0 0 17 3H15A2 2 0 0 0 13 5V6H11V5A2 2 0 0 0 9 3H7A2 2 0 0 0 5 5V6H3V20H13.09A5.47 5.47 0 0 1 13 19A6 6 0 0 1 21 13.34V6M20 15V18H23V20H20V23H18V20H15V18H18V15Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ToyBrickPlusIcon",
  props: {
    title: {
      type: String,
      default: "Toy Brick Plus icon"
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
