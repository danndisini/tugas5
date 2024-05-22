<template>
  <q-card>
    <q-card-section>
      <div class="text-h6">Card Title</div>
      <div class="text-subtitle2">Card subtitle</div>
    </q-card-section>

    <q-card-section>
      This is some text within a card. You can place any content here.
    </q-card-section>

    <q-card-actions align="right">
      <q-btn flat label="Action 1" />
      <q-btn flat label="Action 2" />
    </q-card-actions>
  </q-card>
</template>

<script>
export default {
  name: 'Card'
}
</script>

<style scoped>
.q-card {
  max-width: 350px;
  margin: 20px auto;
}
</style>
