<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon bowl-mix-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15.6 12H2V15C2 18.9 5.1 22 9 22H15C18.9 22 22 18.9 22 15V12H15.6M20 15C20 17.8 17.8 20 15 20H9C6.2 20 4 17.8 4 15V14H20V15M16.2 11L20.3 4.4L22 5.5L18.6 11H16.2Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BowlMixOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Bowl Mix Outline icon"
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
