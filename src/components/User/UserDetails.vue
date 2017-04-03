<template>
    <div class="card">
        <div class="card-content">

            <h3 class="title is-4">User Details</h3>

            <hr>

            <div class="content">
                <ul>
                    <li>
                        Name: {{ name }}
                        <button @click="nameToUppercase" class="button is-primary is-small">toUpper</button>
                        <button @click="callback" class="button is-primary is-small">toLower</button>
                    </li>
                    <li>Age: {{ age }}</li>
                </ul>
            </div>

        </div>
    </div>
</template>

<script>
    import {bus} from '../../main';

    export default {
        props: {
            name: {
                type: String,
                default: 'Anonymous'
            },
            initialAge: {
                type: Number,
                default: 18
            },
            callback: {
                type: Function,
                required: true
            }
        },
        data: function () {
            return {
                age: this.initialAge
            }
        },
        methods: {
            nameToUppercase() {
                this.$emit('changeName', this.name.toUpperCase());
            }
        },
        created() {
            bus.$on('ageIncremented', newAge => {
                this.age = newAge;
            });
        }
    }
</script>