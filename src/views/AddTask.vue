<template>
    <div>
        <input type="text" v-model="text" v-if="add" /><button @click="onClick">добавить</button>
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