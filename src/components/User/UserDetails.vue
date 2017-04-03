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
        </div>
    </div>
</template>

<script>
    export default {
        props: {
            name: {
                type: String,
                default: 'Anonymous'
            }
        }
    }
</script>