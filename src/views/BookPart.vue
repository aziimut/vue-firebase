<template>
    <v-container grid-list-md v-if="part">
        <v-layout row wrap>
            <v-flex xs12 sm10 offset-sm1>
                <book-part-content :part="part"></book-part-content>
            </v-flex>
            <v-flex xs12 sm10 offset-sm1>
                <!--<book-part-words :words="part.words"></book-part-words>-->
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
    import BookPartContent from '../components/BookPartContent'
    export default {
        name: "BookPart",
        components: {
           BookPartContent
        },
        props: {
            'bookId': {
                type: String,
                required: true
            },
            'partId': {
                type: String,
                required: true
            }
        },
        computed: {
            part() {
                let val = this.$store.getters.getParts.find(b => b.bookId == this.bookId && b.bookPartId == this.partId)
            }
        }
    }
</script>

<style scoped>

</style>