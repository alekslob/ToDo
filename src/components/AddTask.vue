<template>
    <div>
        <v-form @submit.prevent="onClick">
            <v-text-field
              autofocus
              ref="input"
              hide-details
              dense
              v-model="text"
              :rules="nameRules"
              :counter="60"
              label="Задача"
              
              @blur="$emit('cancel')"
              required
            > </v-text-field>

        </v-form>
    </div>
</template>
<script>
export default{
    data:()=>({
        add: false,
        text: '',
        tap:' tete',
        nameRules: [
        v => v.length <= 60 || 'Слишком много букав',
    ]
    }),
    methods:{
        onClick(){
            if (this.text.length <= 60) {
                
                this.$emit('addTask', this.text)
                this.$refs.input.blur()
            }
        }
    }
    
}
</script>
<style>
.text {
    color: red;
}
</style>