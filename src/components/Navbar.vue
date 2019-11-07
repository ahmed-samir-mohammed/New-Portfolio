<template>
    <b-navbar variant="faded" type="light">
        <router-link :to="{name: 'Home'}">
            <b-navbar-brand tag="h1" class="mb-0">
                <span>A</span>hmed - <span>S</span>amir
            </b-navbar-brand>
        </router-link>
    </b-navbar>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss">
    .navbar-brand {
        display: flex;
        align-items: center;
        text-decoration: none;
        span {
            font-size: 2rem
        }
    }
</style>