<template>
    <div>{{ text }}</div>
</template>

<script>
export default{
    props:{
        title: {
            type: String,
            default: 'WHERE IS MY TITLE'
        }
    }
}
</script>