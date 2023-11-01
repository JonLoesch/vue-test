<script setup lang="ts">
import {type PropType} from 'vue'

defineProps({
    foo: {
        required: true,
        type: String,
    }
})

// I have also tried the following 2 and I seem to get the same behavior:

// defineProps({
//     foo: String as PropType<string>
// });

// defineProps<{foo: string}>();

</script>

<template>
    <div> Hello {{ foo }} </div>
    <!-- The above 'foo' is properly typed and has autocomplete and everything. -->
</template>