<template>
    <li
      style="padding-top: 10px"
      class="message"
      @click="handleClick">
        {{message}}
    </li>
</template>

<script>
export default {
  name: 'Message',
  props: {
    message: {
      type: String,
      required: true,
      validator: value => value.length > 1
    },
    author: {
      type: String,
      default: 'Cristina'
    }
  },
  methods: {
    handleClick () {
      this.$emit('message-clicked', this.message)
    }
  }
}
</script>
