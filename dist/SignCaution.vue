<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon sign-caution-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2,3H22V13H18V21H16V13H8V21H6V13H2V3M18.97,11L20,9.97V7.15L16.15,11H18.97M13.32,11L19.32,5H16.5L10.5,11H13.32M7.66,11L13.66,5H10.83L4.83,11H7.66M5.18,5L4,6.18V9L8,5H5.18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SignCautionIcon",
  props: {
    title: {
      type: String,
      default: "Sign Caution icon"
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
