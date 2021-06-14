<template>
<!-- Box1 -->
    <div class="grid md:grid=cols-2 gap-4">
        <div class="shadow-md bg-blue-200 p-10 text-center rounded">
            <h3 class="text-3xl font-bold m-4 text-blue-900">
                Cases
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">New:</span>
                {{ numberWithCommas(stats.NewConfirmed) }}
        
            </div>
             <div class="text-2xl mb-4">
                     <span class="font-bold">Total:</span>
                {{ numberWithCommas(stats.TotalConfirmed) }}
             </div>
        </div>
        <!-- Box2 -->
           <div class="shadow-md bg-red-100 p-10 text-center rounded">
            <h3 class="text-3xl font-bold m-4 text-blue-900">
                Deaths
            </h3>
            <div class="text-2xl mb-4">
                <span class="font-bold">New:</span>
                {{ numberWithCommas(stats.NewDeaths)}}
        
            </div>
             <div class="text-2xl mb-4">
                     <span class="font-bold">Total:</span>
                {{ numberWithCommas(stats.TotalDeaths) }}
             </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'DataBox',
        props: ['stats'],
        methods: {
             numberWithCommas(x) {
             return x.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
}
        }

    }
</script>

