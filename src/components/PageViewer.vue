<template>
     <div class='container'>
        <h1>{{ page.pageTitle }}</h1>
        <p>{{ page.paragraph }}</p>
     </div>
</template>

<script>
export default {
    props: [ 'page' ]
}

</script>