<template>
    <div id="app">
        <app-user></app-user>
    </div>
</template>

<script>
    import User from './components/User/User.vue';

    export default {
        components: {
            appUser: User
        }
    };
</script>
