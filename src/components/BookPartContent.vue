<template>
    <v-card>
        <div>
            <div class="display-1">{{part.bookTitle}}</div>
        </div>
    </v-card>
</template>

<script>
    export default {
        name: "BookPartContent",
        props: {
            "part": {
                type: Object,
                required: true
            }
        }
    }
</script>

<style scoped>

</style>