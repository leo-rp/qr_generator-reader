<template>
  <q-page class="flex flex-center">
    <StudentCard
      studentName="Henry Rodriguez"
      studentLink="https://www.linkedin.com/in/henry-l-rodriguez/"
      studentPhoto="https://wssinternational.net/a/wp-content/uploads/elementor/thumbs/Leonardo-Rodriguez-Developer-o6pxfrp7a0q580pahabktj5fw9ibo5vlktc6q6yla8.png"
    />
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import StudentCard from 'components/StudentCard.vue'

export default defineComponent({
  name: 'IndexPage',
  components: {
    StudentCard
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
