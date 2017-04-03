<template>
    <section class="hero">
        <div class="hero-body">
            <div class="container">
                <div class="box">
                    <h1 class="title has-text-centered">User</h1>
                    <div class="columns">
                        <div class="column">
                            <app-user-details name="Jack"></app-user-details>
                        </div>
                        <div class="column">
                            <div class="box"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import UserDetails from './UserDetails.vue';

    export default {
        components: {
            appUserDetails: UserDetails
        }
    }
</script>