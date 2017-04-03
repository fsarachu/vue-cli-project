<template>
    <div class="card">
        <div class="card-content">
            <h3 class="title is-4">User Edit</h3>
            <hr>
            <div class="content">
                <p>
                    Current Age: {{ age }} -
                    <button @click="incrementAge" class="button is-primary is-small">Increment</button>
                    <button @click="decrementAge" class="button is-primary is-small">Decrement</button>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    import {bus} from '../../main'

    export default {
        props: {
            initialAge: {
                type: Number,
                default: 18
            }
        },
        data: function () {
            return {
                age: this.initialAge
            }
        },
        methods: {
            incrementAge() {
                this.age += 1;
                bus.$emit('ageIncremented', this.age);
            },
            decrementAge() {
                this.age -= 1;
                bus.$emit('ageIncremented', this.age);
            }
        }
    }
</script>