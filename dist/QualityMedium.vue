<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon quality-medium-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M21,6V18A2,2 0 0,1 19,20H5A2,2 0 0,1 3,18V6A2,2 0 0,1 5,4H19A2,2 0 0,1 21,6M12,10C12,9.5 11.5,9 11,9H6.5C6,9 5.5,9.5 5.5,10V15H7V10.5H8V14H9.5V10.5H10.5V15H12V10M14.5,9A1,1 0 0,0 13.5,10V14A1,1 0 0,0 14.5,15H15.5V16.5H16.75V15H17.5A1,1 0 0,0 18.5,14V10A1,1 0 0,0 17.5,9H14.5M15,10.5H17V13.5H15V10.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "QualityMediumIcon",
  props: {
    title: {
      type: String,
      default: "Quality Medium icon"
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
