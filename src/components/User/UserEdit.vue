<template>
    <div class="card">
        <div class="card-content">
            <h3 class="title is-4">User Edit</h3>
            <hr>
            <div class="content">
                <p>
                    Current Age: {{ age }} -

                    <button @click="incrementAge" class="button is-primary is-small">Increment</button>
                    <button class="button is-primary is-small">Decrement</button>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    import {bus} from '../../main'

    export default {
        props: {
            age: {
                type: Number,
                default: 18
            }
        },
        methods: {
            incrementAge() {
                this.age += 1;
                bus.$emit('ageIncremented', this.age);
            }
        }
    }
</script>