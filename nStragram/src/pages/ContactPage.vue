<template>
    <div id="contact-page">
        <h1>Contact Page !!</h1>
        <a :href="backlink">
            <button>back</button>
        </a>
    </div>
</template>

<script>
export default {
    name: "ContactPage",
    data: () => {
      return {
        backlink: '/'
      }
    }
};
</script>

<style>
</style>
