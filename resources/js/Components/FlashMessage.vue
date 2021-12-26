<template>
    <div v-if="message">
        <ul class="flex items-center justify-center bg-gray-600 text-white">
            <li>{{ message }}</li>
        </ul>
    </div>
</template>

<script>
import {usePage} from "@inertiajs/inertia-vue3";
import {computed} from "vue";

export default {
    name: "FlashMessage",

    setup() {
         const message = computed(() => usePage().props.value.flash.message)

        return {
            message,
        }
    }
}
</script>

<style scoped>

</style>
