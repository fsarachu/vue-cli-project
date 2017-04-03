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
                            <app-user-edit></app-user-edit>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import UserDetails from './UserDetails.vue';
    import UserEdit from './UserEdit.vue';

    export default {
        components: {
            appUserDetails: UserDetails,
            appUserEdit: UserEdit
        }
    }
</script>