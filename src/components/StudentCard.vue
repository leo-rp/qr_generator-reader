<template>
  <figure class="qrcode">
    <vue-qrcode
      :value="studentLink"
      tag="svg"
      :options="{
        errorCorrectionLevel: 'H',
        width: 300,
      }"
    ></vue-qrcode>
    <img
      class="qrcode__image"
      :src="studentPhoto"
      :alt="studentName"
    />
  </figure>
  name: {{studentName}}
  photo: {{studentPhoto}}
  link: {{studentLink}}
</template>
<script>
import { defineComponent } from 'vue'
import VueQrcode from '@chenfengyuan/vue-qrcode'

export default defineComponent({
  name: 'StudentCard',
  props: {
    studentName: {
      type: String,
      required: true,
      default: 'Student name'
    },
    studentPhoto: {
      type: String,
      required: false
    },
    studentLink: {
      type: String,
      default: ''
    }
  },
  components: {
    VueQrcode
  }
})
</script>

<style scoped>
.qrcode {
  display: inline-block;
  font-size: 0;
  margin-bottom: 0;
  position: relative;
}

.qrcode__image {
  background-color: #fff;
  border: 0.25rem solid #fff;
  border-radius: 0.25rem;
  box-shadow: 0 0.125rem 0.25rem rgba(0, 0, 0, 0.25);
  height: 25%;
  left: 50%;
  overflow: hidden;
  position: absolute;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 25%;
}
</style>
