<template>
    <RouterLink :to="to">
        <slot/>
    </RouterLink>
</template>

<script setup lang="ts">


type InternalRoute = {
  page: 'home',
} | {
  page: 'about'
}

defineProps<{ to: InternalRoute }>();
</script>