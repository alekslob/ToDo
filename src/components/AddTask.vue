<template>
    <div>
        <input type="text" v-model="text" v-if="add" /><v-btn
      class="mx-2"
      fab
      dark
      color="indigo"
    >
      <v-icon dark>
        mdi-plus
      </v-icon>
    </v-btn>
    </div>
</template>
<script>
export default{
    data:()=>({
        add: false,
        text: '',
        tap:' tete'
    }),
    methods:{
        onClick(){
            if (this.add){
                this.tap = this.text
            }
            this.add = !this.add;
            
        }
    }
    
}
</script>
<style></style>