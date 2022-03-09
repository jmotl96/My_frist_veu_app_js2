<template>
    <v-card class="mb-2 col-sm-12 col-md-6 col-lg-4 col-xl-3">
      <h1>{{itemName}}</h1>
      <div>manufacturer: {{manufacturer}}</div>
      <div>Type: {{type}}</div>
      <div>cuddlyRank: {{cuddlyRank}}</div>
      <div>Cost: {{cost}}</div>
      <v-row class="mt-3">
        <v-btn class="mr-2" color="primary">
          Edit
        </v-btn>
        <v-btn color="error">
          delete
        </v-btn>
      </v-row>

    </v-card>
</template>

<script>
export default {
  name: "collectionItem",
  manufacturer: "collectionItem",
  type:"collectionItem",
  cuddlyRank:"collectionItem",
  cost:"collectionItem",
  props:{
    itemName:String,
    manufacturer: String,
    type: String,
    cuddlyRank: String,
    cost: String,
  }
}
</script>

<style scoped>

</style>