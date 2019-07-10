<template>
    <div>
        <ol class='breadcrumb'>
            <li><nuxt-link to="dashboard"><i class='fa fa-dashboard'></i>
            Home</nuxt-link></li>
    
        <li v-if="page"><nuxt-link :to="route"> {{section}}</nuxt-link></li>
        <li v-if="page" class='active'>{{page}}</li>
        
    
        <li v-else class='active'>{{section}}</li>
        </ol>
    </div>
</template>

<script>
export default {
    props: ['section', 'page', 'title', 'route'],
}
</script>