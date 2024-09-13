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

/* Media query para pantallas de 360px a 800px */
@media (min-width: 360px) and (max-width: 800px) {

    .time-info-component {
        /* Reducir el padding en pantallas pequeñas */
        padding: 2px;

    }

    .time-title {
        /* Reducir tamaño de la fuente para pantallas pequeñas */
        font-size: 1.5rem;

    }

    .time-item {
        /* Reducir el espacio entre los elementos */
        gap: 5px;
        /* Reducir el tamaño de letra de los items */
        font-size: 0.8rem;

    }

    .time-list {
        /* Añadir espacio entre los items */
        gap: 10px;

    }

}
</style>