<template>
    <div>
        <h1>tilte: {{ tilte }}</h1>
        <h2 v-bind="$attrs">author: {{ author }}</h2>
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
    },
    inheritAttrs: false
}
</script>

<style scoped></style>



<!-- non props attributs are some default attributs that is provide by vue itself and can be applied directly to parent div if present -->
<!-- Else we have to use @attrs to custom set non props attributes to specific element -->
<!-- to disable non props attributes default behavious we have to use inharitAttrs: false -->