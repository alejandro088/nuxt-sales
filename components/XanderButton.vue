<template>
    <nuxt-link :to="url" class='btn btn-app' >
        <i class='text-red' :class="icon"></i>
        <slot></slot>
    </nuxt-link>  
</template>

<script>
export default {
    props: ['url', 'icon'],
}
</script>