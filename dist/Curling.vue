<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon curling-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10,3V5C12.5,5 13.9,5.05 14.72,5.41C15.26,5.65 15.73,6.21 16.25,7H5V9H19.62L18.89,7.55C17.86,5.5 16.96,4.22 15.53,3.59C14.1,2.95 12.5,3 10,3M6,11C3.78,11 2,12.78 2,15V18C2,20.22 3.78,22 6,22H18C20.22,22 22,20.22 22,18V15C22,12.78 20.22,11 18,11H6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CurlingIcon",
  props: {
    title: {
      type: String,
      default: "Curling icon"
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
