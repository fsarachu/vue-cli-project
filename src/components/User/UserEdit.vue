<template>
    <div class="card">
        <div class="card-content">
            <h3 class="title is-4">User Edit</h3>
            <hr>
            <div class="content">
                <p>
                    Current Age: {{ age }} -
                    <button class="button is-primary is-small">Increment</button>
                    <button class="button is-primary is-small">Decrement</button>
                </p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            age: {
                type: Number,
                default: 18
            }
        }
    }
</script>