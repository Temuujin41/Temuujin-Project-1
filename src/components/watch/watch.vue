<template>
    <link rel="stylesheet" href="style.css">
    <div>
    <button style="margin:15px;" class="button" @click="toggleShowbooks">
        Toggle Videos "CLICK!"
  </button>
 
  </div>
    <div v-if="ShowVideos">
        <h1 style="text-align:center;">VueJs Tuturial</h1>
    <div class="columns is-mobile vidoe place-content-center">
        <div class="column"><iframe width="560" height="315" src="https://www.youtube.com/embed/YrxBCBibVo0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>
    </div>
    </div>
    
</template>
<script>
    export default {
        data() {
            return{
                ShowVideos: true,
                title: ' Error',
                tetx: 'lorem10'
            }
        },
          methods: {
            toggleShowbooks() {
                this.ShowVideos = !this.ShowVideos
            }
          }
    }
</script>