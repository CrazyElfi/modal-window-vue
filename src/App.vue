<template>
  <div class="wrapper">
    <div class="wrapper-content">
      <section>
        <div class="container">
          <button
            class="btn btnPrimary"
            @click="modalFirst =  !modalFirst">Show first modal</button>
          <!--First model-->
          <models
            title="First model"
            v-if="modalFirst"
            @close="modalFirst =  !modalFirst"></models>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import models from '@/components/Modal.vue'

export default {
  components: {
    models
  },
  data() {
    return {
      modalFirst: false
    }
  }
}
</script>

<style>

</style>
