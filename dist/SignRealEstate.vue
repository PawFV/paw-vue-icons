<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon sign-real-estate-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18 8H8C6.9 8 6 8.9 6 10V16C6 17.11 6.9 18 8 18H18C19.11 18 20 17.11 20 16V10C20 8.9 19.11 8 18 8M14 16H8V14H14V16M18 12H8V10H18V12M22 6H4V22H2V2H4V4H22V6Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SignRealEstateIcon",
  props: {
    title: {
      type: String,
      default: "Sign Real Estate icon"
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
