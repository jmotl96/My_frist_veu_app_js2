<template>
<div>
  <v-row class="col-12 ml-0 pl-0">
  <collection-item
        v-for="item in items"
        v-bind:key="item.id"
        v-bind:itemName="item.itemName"
        v-bind:manufacturer="item.manufacturer"
        v-bind:type="item.type"
        v-bind:cuddlyRank="item.cuddlyRank"
        v-bind:cost="item.cost"
  ></collection-item></v-row>
<!--  <v-card-text style="height: 100px; position: relative">-->
<!--    <v-fab-transition>-->
<!--      <v-btn-->
<!--          onclick="addItem()"-->
<!--          color="primary"-->
<!--          dark-->
<!--          absolute-->
<!--          top-->
<!--          right-->
<!--          fab-->
<!--      >-->
<!--        <v-icon>mdi-plus</v-icon>-->
<!--      </v-btn>-->
<!--    </v-fab-transition>-->
<!--  </v-card-text>-->
  <item-box
      v-bind:collection-list = "items"
  >

  </item-box>
</div>
</template>

<script>
import CollectionItem from "@/components/collectionItem";
import ItemBox from "@/components/ItemBox";

export default {
  name: "collectionList",
  components: {ItemBox, CollectionItem},
  data: function(){
    return{
      items: [
        {id:1, itemName: "hooters", manufacturer: "something", type: "owl", cuddlyRank: "5", cost: "24"},
        {id:2, itemName: "vaporeon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: "9", cost: "80"},
        {id:3, itemName: "flareon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: "9", cost: "80"},
        {id:4, itemName: "glaceon", manufacturer: "Build a bare", type: "Pokemon", cuddlyRank: "9", cost: "80"},
        {id:5, itemName: "Wifu", manufacturer: "dakimakuri", type: "Dakimakura", cuddlyRank: "10", cost: "200"},
      ]
    }


  },

}
</script>

<style scoped>

</style>