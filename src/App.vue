<script setup>
const colors = ['red', 'brown', 'yellow', 'green', 'blue', 'purple', 'pink', 'orange', 'black', 'white', 'cyan', 'magenta', 'lime', 'indigo', 'teal', 'maroon', 'navy', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver', 'aqua', 'fuchsia', 'lime', 'purple', 'teal', 'navy', 'maroon', 'olive', 'silver']

const randomColor = () => {
  return colors[Math.floor(Math.random() * colors.length)]
}
</script>

<template>
  <section>
    <article 
    v-for="i in 18" 
    :style="{backgroundColor: randomColor()}" 
    :class="{double: Math.random() > 0.5}"
    >
  </article>
  </section>
</template>

<style scoped>
article {
  width: 100%;
  height: 170px;
  background-color: red;
  border: 1px solid gainsboro;
  transition: transform 0.3s;
}

article:hover {
  transform: scale(1.1);
}

section {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 10px;
}

.double {
  grid-column: span 2;
}
</style>