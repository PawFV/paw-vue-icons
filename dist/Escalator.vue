<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon escalator-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20,8H18.95L6.95,20H4A2,2 0 0,1 2,18A2,2 0 0,1 4,16H5.29L7,14.29V10A1,1 0 0,1 8,9H9A1,1 0 0,1 10,10V11.29L17.29,4H20A2,2 0 0,1 22,6A2,2 0 0,1 20,8M8.5,5A1.5,1.5 0 0,1 10,6.5A1.5,1.5 0 0,1 8.5,8A1.5,1.5 0 0,1 7,6.5A1.5,1.5 0 0,1 8.5,5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EscalatorIcon",
  props: {
    title: {
      type: String,
      default: "Escalator icon"
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
