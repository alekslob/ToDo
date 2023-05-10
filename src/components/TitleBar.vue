<template>
    <v-app-bar elevation="6" app >
        <v-spacer>ToDo</v-spacer>
        <v-btn class="mx-4"
                color="gray" @click="isAddActive = true">
            <v-icon dark>
                mdi-plus
            </v-icon>
        </v-btn>
        <template v-if="isAddActive" #extension>
            <v-container fluid>
                <AddTask style="widht: 100%" @cancel="isAddActive = false" @addTask="(e) => $emit('addTask', e)" />
            </v-container>
        </template>
    </v-app-bar>
</template>

<script>

import AddTask from './AddTask.vue'

export default{
data:() => ({
    isAddActive: false
}),
methods: {

},
components: {
    AddTask
}
}
</script>
<style>
</style>