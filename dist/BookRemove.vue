<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon book-remove-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18,22H6A2,2 0 0,1 4,20V4C4,2.89 4.9,2 6,2H7V9L9.5,7.5L12,9V2H18A2,2 0 0,1 20,4V20A2,2 0 0,1 18,22M16.41,19.83L17.83,18.41L16.41,17L17.83,15.59L16.41,14.17L15,15.59L13.59,14.17L12.17,15.59L13.59,17L12.17,18.41L13.59,19.83L15,18.41L16.41,19.83Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BookRemoveIcon",
  props: {
    title: {
      type: String,
      default: "Book Remove icon"
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
