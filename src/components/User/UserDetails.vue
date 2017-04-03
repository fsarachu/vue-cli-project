<template>
    <div class="card">
        <div class="card-content">

            <h3 class="title is-4">User Details</h3>

            <hr>

            <div class="content">
                <ul>
                    <li>Name: {{ name }}</li>
                </ul>
            </div>

            <hr>

            <button @click="nameToUppercase" class="button is-light is-fullwidth">Name to Uppercase</button>
            <button @click="callback" class="button is-light is-fullwidth">Name to Lowercase</button>

        </div>
    </div>
</template>

<script>
    export default {
        props: {
            name: {
                type: String,
                default: 'Anonymous'
            },
            callback: {
                type: Function,
                required: true
            }
        },
        methods: {
            nameToUppercase() {
                this.$emit('changeName', this.name.toUpperCase());
            }
        }
    }
</script>