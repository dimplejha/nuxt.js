<template>
<div>
    <h1>hii i m here</h1>
    <div v-for="video in videos" :key="video.id">{{video.name}}</div>
    <nuxt-child/>
</div>

</template>

<script>

export default {
    data() {
        return {
            videos:[{
              id:"34567",
              name:"DIMPLE"
            },
            {
              id:"34568",
              name:"Aaliya"
            },
            {
              id:"34569",
              name:"Shital"
            },
            
            ]
        }
    }
    }

</script>

<style>


</style>
