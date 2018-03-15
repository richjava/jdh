<template>
    <div class="designer-page">
        <Banner></Banner>

        <div class="holder">
            <div class="designer-info">
                <h2></h2>
            </div>
        </div>
        <!-- / holder -->
    </div>
</template>

<script>
import Banner from './Banner'
export default {
    name: 'designer',
    components: {
        Banner
    },
    props: ['username']
}
</script>
<!-- styling for the component -->
<style>

</style>
