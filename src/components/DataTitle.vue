<template>
    <div class="text-center">
        <h2 class="font-bold text-3xl">{{text}}</h2>
        <div class="mt-6 mb-8 text2-xl">
            {{timestamp}}
        </div>
    
    </div>
</template>

<script>
import moment from 'moment'
    export default {
        name: 'DataTitle',
        props: ['text', 'dataDate'],
        computed: {
            timestamp: function() {
                return moment(this.dataDate).format('MMMM Do YYYY, h:mm:ss a')
            }
        }
 
    }
</script>



