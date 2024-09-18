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
    background: #fff7fc;
    padding: 20px;
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
@media only screen and (width >=360px) and (width <=800px) {

    .time-info-component {
        /* Reducir el padding para pantallas más pequeñas */
        padding: 10px;
        background: #fff7fc;
        border-radius: 5px;
        margin-bottom: 15px;
        margin-left: 10px;
        margin-right: 10px;
    }
}
</style>