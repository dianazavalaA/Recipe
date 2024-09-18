<template>
    <div class="instructions-component">
        <h2 class="instructions-title">{{ title }}</h2>
        <ol class="instruction-list">
            <li v-for="(instruction, index) in instructions" :key="index" class="instruction-item">
                <strong>{{ instruction.title }}:</strong> {{ instruction.text }}
            </li>
        </ol>
    </div>
</template>

<script>
export default {
    name: 'InstructionsComponent',
    props: {
        title: {
            type: String,
            default: 'Instructions'
        }
    },
    data() {
        return {
            instructions: [
                {
                    title: 'Beat the eggs',
                    text: 'In a bowl, beat the eggs with a pinch of salt and pepper until they are well mixed. You can add a tablespoon of water or milk for a fluffier texture.'
                },
                {
                    title: 'Heat the pan',
                    text: 'Place a non-stick frying pan over medium heat and add butter or oil.'
                },
                {
                    title: 'Cook the omelette',
                    text: 'Once the butter is melted and bubbling, pour in the eggs. Tilt the pan to ensure the eggs evenly coat the surface.'
                },
                {
                    title: 'Add fillings (optional)',
                    text: 'When the eggs begin to set at the edges but are still slightly runny in the middle, sprinkle your chosen fillings over one half of the omelette.'
                },
                {
                    title: 'Fold and serve',
                    text: 'As the omelette continues to cook, carefully lift one edge and fold it over the fillings. Let it cook for another minute, then slide it onto a plate.'
                },
                {
                    title: 'Enjoy',
                    text: 'Serve hot, with additional salt and pepper if needed.'
                }
            ]
        };
    }
}
</script>

<style scoped>
.instructions-component {
    padding: 20px;
    border-radius: 8px;
    margin-bottom: 20px;

}

.instructions-title {
    font-size: 1.8rem;
    margin-bottom: 15px;
    font-weight: bold;
    color: #723e55;
    text-align: left;
    padding-bottom: 10px;
}

.instruction-list {
    /* Inicializa el contador */
    counter-reset: list-counter;
    /* Esta propiedad oculta los números predeterminados */
    list-style: none;
    /* Ajusta según sea necesario para la alineación */
    padding-left: 20px;
    /* Ajusta según sea necesario para la alineación */
    margin-left: 0;
    letter-spacing: 0.2px;
}

.instruction-item {
    counter-increment: list-counter;
    /* Incrementa el contador en cada ítem */
    margin-bottom: 12px;
    /* Espacio entre ítems */
    line-height: 1.6;
    /* Ajusta para una mejor legibilidad */
    color: #333;
    /* Color del texto */
    position: relative;
    /* Posicionamiento relativo para los pseudoelementos */
    padding-left: 30px;
    /* Espacio para los números personalizados */
}

.instruction-item::before {
    content: counter(list-counter) ". ";
    /* Formato del número con punto */
    color: #723e55;
    /* Color personalizado para el número */
    font-weight: bold;
    /* Negrita para los números */
    position: absolute;
    /* Posicionamiento absoluto */
    left: 0;
    /* Alineación izquierda dentro del elemento de lista */
    top: 0;
    /* Alineación superior */
}


/* Media query para pantallas de 360px a 800px */
@media only screen and (width >=360px) and (width <=800px) {

    .instructions-component {
        /* Reducir el padding para pantallas más pequeñas */
        padding: 10px;

    }
}
</style>
