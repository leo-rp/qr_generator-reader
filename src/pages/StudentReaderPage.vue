<template>
  <StreamBarcodeReader @decode="onDecode" @loaded="onLoaded"></StreamBarcodeReader>
  <p>status: <a href="{{cameraStatus}}">{{cameraStatus}}</a></p>
</template>

<script>
import { defineComponent } from 'vue'
import { StreamBarcodeReader } from 'vue-barcode-reader'

export default defineComponent({
  name: 'IndexPage',
  components: {
    StreamBarcodeReader
  },
  data () {
    return {
      cameraStatus: 'false'
    }
  },
  methods: {
    onDecode (result) {
      this.cameraStatus = result
    },
    onLoaded (result) {
      alert('cameraloaded')
    }
  }
})
</script>
