<template>
    <div>
        <form>
            <v-text-field
              v-model="text"
              :rules="nameRules"
              :counter="60"
              label="Задача"
              append-outer-icon="mdi-plus"
              @click:append-outer="onClick"
              required
            > </v-text-field>

        </form>
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
            this.$emit('back', this.text)
        }
    }
    
}
</script>
<style>
.text {
    color: red;
}
</style>