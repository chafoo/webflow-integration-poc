<template>
    <div>
        <LayoutHeader />
        <Nuxt />
        <LayoutFooter />
    </div>
</template>

<script lang="ts">
import Vue from 'vue'
import LayoutHeader from "@/components/layout/Header.vue"
import LayoutFooter from "@/components/layout/Footer.vue"

export default Vue.extend({
    components: {
        LayoutFooter,
        LayoutHeader,
    }
})
</script>