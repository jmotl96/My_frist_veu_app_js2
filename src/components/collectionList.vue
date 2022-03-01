<template>
<div>
  <collection-item
        v-for="item in items"
        v-bind:key="item.id"
        v-bind:itemName="item.itemName"
  ></collection-item></div>
</template>

<script>
import CollectionItem from "@/components/collectionItem";
export default {
  name: "collectionList",
  components: {CollectionItem},
  data: function(){
    return{
      items: [
        {id:1, itemName: "hooters", manufacturer: "something", type: "owl", cuddlyRank: 5, cost: 24},
        {id:2, itemName: "vaporeon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: 9, cost: 80},
        {id:3, itemName: "flareon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: 9, cost: 80},
        {id:4, itemName: "glaceon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: 9, cost: 80},
        {id:5, itemName: "Wifu", manufacturer: "dakimakuri", type: "Dakimakura", cuddlyRank: 10, cost: 200},
      ]
    }

  },
}
</script>

<style scoped>

</style>