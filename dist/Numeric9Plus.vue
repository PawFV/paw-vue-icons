<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon numeric9-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 11H17V9H15V11H13V13H15V15H17V13H19V11M10 7H8C6.9 7 6 7.9 6 9V11C6 12.11 6.9 13 8 13H10V15H6V17H10C11.11 17 12 16.11 12 15V9C12 7.89 11.1 7 10 7M10 11H8V9H10V11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "Numeric9PlusIcon",
  props: {
    title: {
      type: String,
      default: "Numeric9 Plus icon"
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
