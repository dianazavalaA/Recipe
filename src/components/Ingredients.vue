<template>
    <div class="ingredient-component">
        <h2 class="ingredient-title">{{ title }}</h2>

        <ul class="ingredient-list">
            <li v-for="(ingredient, index) in ingredients" :key="index" class="ingredient-item">
                {{ ingredient }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'IngredientsComponent',
    props: {
        title: {
            type: String,
            default: 'Ingredients'
        }
    },
    data() {
        return {
            ingredients: [
                '2-3 large eggs',
                'Salt, to taste',
                'Pepper, to taste',
                '1 tablespoon of butter or oil',
                'Optional fillings: cheese, diced vegetables, cooked meats, herbs'
            ]
        };
    }
}
</script>

<style scoped>
.ingredient-item {
    display: flex;
    align-items: center;
    gap: 20px;
}

.ingredient-item::before {
    content: "• ";
}

.ingredient-title {
    font-size: 1.5rem;
    margin-bottom: 10px;
    font-weight: bold;
    color: #723e55;
    text-align: left;
}

.ingredient-list {
    list-style-type: disc;
    margin-right: 25px;
    letter-spacing: 0.2px;

}

.ingredient-component {
    padding: 10px;
    border-radius: 8px;
    margin-bottom: 20px;
}


/* Media query para pantallas de 360px a 800px */
@media (min-width: 360px) and (max-width: 800px) {

    .ingredient-component {
        /* Reducir el padding en pantallas pequeñas */
        padding: 2px;

    }

    .ingredient-title {
        /* Reducir tamaño de la fuente para pantallas pequeñas */
        font-size: 1.5rem;

    }

    .ingredient-item {
        /* Reducir el espacio entre los elementos */
        gap: 15px;
        /* Reducir el tamaño de letra de los items */
        font-size: 1rem;

    }

    .ingredient-list {
        /* Añadir espacio entre los items */
        gap: 10px;

    }

}
</style>
