<template>
    <v-card>
      {{itemName}}
    </v-card>
</template>

<script>
export default {
  name: "collectionItem",
  props:{
    itemName:String,
  }
}
</script>

<style scoped>

</style>