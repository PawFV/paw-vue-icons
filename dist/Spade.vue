<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon spade-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15.71,1.22L12.88,4.05C12.1,4.83 12.1,6.09 12.88,6.87L14.3,8.29L10.06,12.53L7.58,10.06L1.22,16.42L7.58,22.78L13.94,16.42L11.47,13.94L15.71,9.7L17.13,11.12C17.91,11.9 19.17,11.9 19.95,11.12L22.78,8.29L15.71,1.22M15.71,4.05L19.95,8.29L18.54,9.7L14.3,5.46L15.71,4.05Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SpadeIcon",
  props: {
    title: {
      type: String,
      default: "Spade icon"
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
