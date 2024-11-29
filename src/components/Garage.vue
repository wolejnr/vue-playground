<script setup>
import { ref } from 'vue'

const title = ref("Adewole's Garage")

const props = defineProps({
    data: Array
})

</script>

<template>
    <div>
        <h1>{{ title }}</h1>

        <div class="content">
            <div v-for="car in props.data" :id="car.vin">
                <p>{{ car.year }} {{ car.manufacturer }} {{ car.model }}</p>
                <p v-if="car.safetied">Has been safetied</p>
                <p v-else>Has not been safetied</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.content {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 20px;
}
</style>