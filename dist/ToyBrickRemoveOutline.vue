<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon toy-brick-remove-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 6V5C19 3.9 18.1 3 17 3H15C13.9 3 13 3.9 13 5V6H11V5C11 3.9 10.1 3 9 3H7C5.9 3 5 3.9 5 5V6H3V20H14V18H5V8H19V13H21V6M17.88 15.46L20 17.59L22.12 15.47L23.54 16.88L21.41 19L23.54 21.12L22.12 22.54L20 20.41L17.88 22.54L16.46 21.12L18.59 19L16.47 16.88">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ToyBrickRemoveOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Toy Brick Remove Outline icon"
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
