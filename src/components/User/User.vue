<template>
    <section class="hero">
        <div class="hero-body">
            <div class="container">
                <div class="box">
                    <h1 class="title has-text-centered">This is {{ name }}'s Profile</h1>

                    <button @click="reverseName" class="button is-primary is-fullwidth">Reverse Name</button>

                    <hr>

                    <div class="columns">
                        <div class="column">
                            <app-user-details @changeName="name = $event" :name="name"></app-user-details>
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