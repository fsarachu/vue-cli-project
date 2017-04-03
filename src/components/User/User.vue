<template>
    <section class="hero">
        <div class="hero-body">
            <div class="container">
                <div class="box">
                    <h1 class="title has-text-centered">User</h1>

                    <button @click="reverseName" class="button is-primary">Reverse Name</button>

                    <div class="columns">
                        <div class="column">
                            <app-user-details :name="name"></app-user-details>
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
        data: function () {
            return {
                name: 'Franco'
            };
        },
        methods: {
            reverseName() {
                this.name = this.name.split('').reverse().join('');
            }
        },
        components: {
            appUserDetails: UserDetails,
            appUserEdit: UserEdit
        }
    }
</script>