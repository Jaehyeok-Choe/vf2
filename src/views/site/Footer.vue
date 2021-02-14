<template>
<div>
    <v-footer padless color="primary" dark>
        <v-col
        class="text-center"
        cols="12"
        >
        {{ new Date().getFullYear() + ' ' + footer}} — <strong>Vuetify</strong>
        </v-col>
    </v-footer>
</div>
</template>

<script>
export default {
  props: ['footer']
}
</script>

<style>

</style>
