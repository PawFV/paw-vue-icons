<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon elevator-passenger-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 3H5C3.9 3 3 3.9 3 5V19C3 20.1 3.9 21 5 21H19C20.1 21 21 20.1 21 19V5C21 3.9 20.1 3 19 3M8 5C8.8 5 9.5 5.7 9.5 6.5S8.8 8 8 8 6.5 7.3 6.5 6.5 7.2 5 8 5M11 14H9.5V19H6.5V14H5V11C5 9.9 5.9 9 7 9H9C10.1 9 11 9.9 11 11V14M15.9 19L13 14.2H18.8L15.9 19M13 10L16 5L19 10H13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ElevatorPassengerIcon",
  props: {
    title: {
      type: String,
      default: "Elevator Passenger icon"
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
