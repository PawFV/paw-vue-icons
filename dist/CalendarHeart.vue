<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon calendar-heart-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19,20V9H5V20H19M16,2H18V4H19A2,2 0 0,1 21,6V20A2,2 0 0,1 19,22H5A2,2 0 0,1 3,20V6A2,2 0 0,1 5,4H6V2H8V4H16V2M12,18.17L11.42,17.64C9.36,15.77 8,14.54 8,13.03C8,11.8 8.97,10.83 10.2,10.83C10.9,10.83 11.56,11.15 12,11.66C12.44,11.15 13.1,10.83 13.8,10.83C15.03,10.83 16,11.8 16,13.03C16,14.54 14.64,15.77 12.58,17.64L12,18.17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CalendarHeartIcon",
  props: {
    title: {
      type: String,
      default: "Calendar Heart icon"
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
