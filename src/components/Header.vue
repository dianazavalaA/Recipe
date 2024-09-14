<template>
    <div class="header-component">
        <img :src="imageSrc" alt="Omelette" class="recipe-image" />
        <h1 class="recipe-title">{{ title }}</h1>
        <p class="recipe-description">{{ description }}</p>
    </div>
</template>

<script>
export default {
    name: 'HeaderComponent',
    props: {
        imageSrc: {
            type: String,
            default: '/img/omelette.jpg'
        },
        title: {
            type: String,
            default: 'Simple Omelette Recipe'
        },
        description: {
            type: String,
            default: 'An easy and quick dish, perfect for any meal. This classic omelette combines beaten eggs cooked to perfection, optionally filled with your choice of cheese, vegetables, or meats.'
        }
    }
}
</script>

<style scoped>
.header-component {
    text-align: center;
    margin-bottom: 20px;
    padding: 0 15px;
    /* Añadir padding para los márgenes laterales en pantallas pequeñas */
}

.recipe-image {
    max-width: 100%;
    height: auto;
    border-radius: 10px;
    margin-bottom: 15px;
}

/* Estilos generales */
.recipe-title {
    font-size: 2rem;
    margin: 0;
    font-weight: bold;
    text-align: left;
}

.recipe-description {
    font-size: 1.2rem;
    color: #555;
    text-align: left;
}

/* Media query para pantallas de 360px a 800px */
@media only screen and (width >=360px) and (width <=800px) {

    /* Reducir tamaño de fuente en pantallas pequeñas */
    .recipe-title {
        font-size: 1.5rem;

    }

    .recipe-description {
        /* Reducir tamaño de la descripción */
        font-size: 1rem;

    }

    .header-component {
        /* Reducir el padding para pantallas más pequeñas */
        padding: 0 10px;

    }
}
</style>
