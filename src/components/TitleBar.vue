<template>
    <v-container fluid>
      <v-app-bar elevation="6" >
        <v-spacer>ToDo</v-spacer>
        <v-btn class="mx-4"
               color="gray" @click="onClick">
            <v-icon dark>
                mdi-plus
            </v-icon>
        </v-btn>
      </v-app-bar>
      </v-container>
</template>

<script>
 export default{
    data:() => ({
        
    }),
    methods: {
        onClick(){
            this.$emit('add_new')
        }
    }
 }
</script>
<style>
</style>