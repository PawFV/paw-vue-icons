<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon coffee-maker-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21 1V4H7V21H21V23H2V3C2 1.89 2.89 1 4 1H21M22 13V15C22 16.11 21.11 17 20 17H18C18 20 15 20 14 20S10 20 10 17V11H20C21.11 11 22 11.9 22 13M20 13H18V15H20V13M17 9L19 5H9L11 9H17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CoffeeMakerIcon",
  props: {
    title: {
      type: String,
      default: "Coffee Maker icon"
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
