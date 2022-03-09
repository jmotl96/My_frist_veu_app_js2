<template>
  <v-row justify="center">
    <v-dialog
        v-model="dialog"
        persistent
        max-width="600px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
            color="primary"
            dark
            v-bind="attrs"
            v-on="on"
        >
          Open Dialog
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">User Profile</span>
        </v-card-title>
        <v-card-text>
          <v-container>
            <v-row>
              <v-col
                  cols="12"
              >
                <v-text-field
                    label="name*"
                    v-model="itemName"
                    required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                    label="manufacturer*"
                    v-model="manufacturer"
                    required
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field
                    label="type*"
                    v-model="type"
                    type="text"
                    required
                ></v-text-field>
              </v-col>
              <v-col
                  cols="12"

                  sm="6"
              >
                <v-text-field
                    label="cuddlyRank*"
                    v-model="cuddlyRank"
                    type="text"
                    required
                >
                </v-text-field>
              </v-col>
              <v-col
                  cols="12"
                  sm="6"
              >
                <v-text-field
                    label="cost*"
                    v-model="cost"
                    type="text"
                    required
                >
                </v-text-field>
              </v-col>
            </v-row>
          </v-container>
          <small>*indicates required field</small>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
              color="blue darken-1"
              text
              @click="dialog = false"
          >
            Close
          </v-btn>
          <v-btn
              color="blue darken-1"
              text
              @click="addItem"
          >
            Save
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
import collectionList from "@/components/collectionList";

export default {
  name: "ItemBox",
  data: () => ({
    dialog: false,
    itemName: "",
    manufacturer: "",
    type: "",
    cuddlyRank: "",
    cost: "",
    id: "",
  }),
  props: {
    collectionList: Array,
  },
  methods: {
    addItem: function (){
      console.log(this.itemName, this.manufacturer, this.type, this.cuddlyRank, this.cost);
      console.log(collectionList.data().items)
      for(var i = 0; i< collectionList.data().items.length; i++){
        console.log(i);
        this.id = i + 2;
      }
      // let itemsArray = collectionList.data().items;
      let newItem = {id:this.id, itemName:this.itemName, manufacturer:this.manufacturer, type:this.type,cuddlyRank: this.cuddlyRank, cost: this.cost}
      // collectionList.data().items.push(newItem);
      this.collectionList.push(newItem)


      console.log(collectionList.data().items);
      this.dialog = false;
    }
  }
}
</script>

<style scoped>

</style>