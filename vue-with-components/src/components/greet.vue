<template>
  <div>
    <h1>Hello {{ name }}, I know you like {{ fruit }}</h1>
  </div>
</template>

<script>
export default {
  name: "LetGreet",
  props: ['name', 'fruit']
}
</script>

<style scoped></style>