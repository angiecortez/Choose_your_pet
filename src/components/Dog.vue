<template>
  <v-card class="dog-card" style="margin: 2px">
    <v-img :src="dog" height="150px"></v-img>
    <v-card-actions>
      <v-spacer></v-spacer>
        <v-btn icon @click="remove">
          <v-icon>delete</v-icon>
        </v-btn>
    </v-card-actions>
  </v-card>

</template>
<script>
export default {
  props: {
      dog: {
        type: String
      },
    },
  methods: {
    remove(){
      this.$emit('remove', this.dog)
    }
  }
}
</script>

