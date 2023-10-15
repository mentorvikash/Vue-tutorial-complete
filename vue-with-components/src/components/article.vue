<template>
    <div>
        <h1>tilte: {{ tilte }}</h1>
        <h2>author: {{ author }}</h2>
        <h3>likes: {{ likes }}</h3>
        <h3>Published: {{ isPublished ? "Yes" : "No" }}</h3>
    </div>
</template>

<script>
export default {
    name: 'ArticleData',
    props: {
        tilte: {
            type: String,
            required: true,
            default: "this is our default title"
        },
        author: String,
        likes: Number,
        isPublished: Boolean,
    }
}
</script>

<style scoped></style>