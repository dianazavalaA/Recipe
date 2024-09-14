<template>
    <div class="time-info-component">
        <h3 class="time-title">{{ title }}</h3>
        <ul class="time-list">
            <li class="time-item">
                <strong>Total:</strong> {{ totalTime }}
            </li>

            <li class="time-item">
                <strong>Preparation:</strong> {{ preparationTime }}
            </li>

            <li class="time-item">
                <strong>Cooking:</strong> {{ cookingTime }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'PreparationComponent',
    props: {
        title: {
            type: String,
            default: 'Preparation time'
        }
    },
    data() {
        return {
            totalTime: 'Approximately 10 minutes',
            preparationTime: '5 minutes',
            cookingTime: '5 minutes'
        };
    }
}
</script>

<style scoped>
.time-info-component {

    padding: 10px;
    border-radius: 8px;
    margin-bottom: 20px;
}

.time-item {
    display: flex;
    align-items: center;
    /* Espacio entre el término y el valor */
    gap: 5px;
    letter-spacing: 0.2px;

}

.time-item strong {
    font-weight: bold;
}

.time-item::before {
    content: "• ";
    /* Viñeta personalizada */
}

.time-title {
    font-size: 1.5rem;
    margin-bottom: 10px;
    font-weight: bold;
    color: #723e55;
    text-align: left;
}

.time-list {
    list-style-type: none;
    /* Deshabilita las viñetas predeterminadas */
    display: flex;
    flex-direction: column;
    letter-spacing: 0.2px;
}
</style>