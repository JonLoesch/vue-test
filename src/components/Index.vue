<script setup lang="ts">
import Test from './Test.vue';
</script>

<template>
    <div> Some test components: </div>
    <!-- These work fine: -->
    <Test foo="World" /> <!-- Works fine -->
    <Test :foo="'World'" /> <!-- Works fine -->

    <!-- These give a runtime warning but nothing at compile time: -->
    <Test :foo="42" />
    <Test />
    <Test :foo="{ some: 'other_data_structure' }" />

    <!-- Even a built-in component doesn't work -->
    <Transition :name="42" />
</template>