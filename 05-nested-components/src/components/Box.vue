<template>
    <div class='box' v-bind:style='{backgroundColor: bgColor}'>
        {{content}}
    </div>
</template>

<script>
export default {
    props:['bgColor', 'content']
}
</script>

<style scoped>
.box {
    border: 1px solid black;
    width:150px;
    height:150px;
}
</style>