<template>

</template>

<script type="text/babel">
import 'weui/dist/style/weui.min.css'

export default {
  name: 'wv-dialog',

  props: {
    type: {
      type: String,
      default: 'ios'
    },
    actions: {
      type: Array,
      default: () => []
    },
    showCancel: {
      type: Boolean,
      default: true
    },
    cancelText: {
      type: String,
      default: 'Cancel'
    }
  },

  data () {
    return {
      visible: true
    }
  },

  methods: {
    itemClick (item) {
      if (item.method && typeof item.method === 'function') {
        item.method()
      }
      this.visible = false
    }
  }
}
</script>