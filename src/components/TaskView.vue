<template>
  <v-card>
    <v-list>
      <v-list-item-group>
        <v-list-item
            v-for="(item, idx) in tasks"
            :key="idx"
            @click="() => itemClick(item)"
        >
            <v-list-item-content >
                <v-list-item-title >{{item.title}}</v-list-item-title>
            </v-list-item-content>
            <v-icon
                v-if="!item.select"
                color="grey"
            >
            mdi-star-outline
            </v-icon>
            <v-icon
                v-else
                color="black"
            >
            mdi-star
            </v-icon>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>

<script>
export default{

    props:{
        tasks: []

    },
    methods:{
        itemClick(item){
            item.select=!item.select
        }
    }

}
</script>