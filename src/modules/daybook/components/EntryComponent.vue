<template>
  <div class="mb-3 pointer p-2 entry-container" @click="goToEntry(id)">

    <div class="entry-title d-flex">
        <span class="text-success fs-5 fw-bold">15</span>
        <span class="mx-1 fs-5">Julio</span>
        <span class="mx-2 fw-light">2021, jueves</span>
    </div>

    <div class="entry-description">
      Pariatur laboris et non nulla. Nostrud commodo tempor labore incididunt dolor est ipsum nulla. Fugiat laboris ad ut ut velit. Cupidatat veniam incididunt consequat ut culpa voluptate aute sunt commodo Lorem esse ipsum. Esse exercitation enim eu adipisicing amet fugiat do sint. Cupidatat occaecat laboris dolor adipisicing do id laboris nulla non ipsum qui. Exercitation amet adipisicing esse adipisicing consectetur anim mollit consequat culpa id quis reprehenderit minim.
    </div>
  </div>
</template>

<script>
export default {

  props: {
    id: {
      Type: Number,
      required: true
    }
  },

  methods: {
      goToEntry(id) {
          this.$router.push({ name: "entry", params: { id } })
      }
  }
}
</script>

<style lang="scss" scoped>
.entry-container {
  border-bottom: 1px solid #2c3e50;
  transition: 0.2s all ease-in;

  &:hover {
    background-color: lighten($color: grey, $amount: 45);
    transition: 0.2s all ease-in;
  }
  
  .entry-description {
    font-size: 12px;
  }
}

</style>