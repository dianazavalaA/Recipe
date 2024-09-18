<template>
    <div class="nutrition-component">
        <h3 class="nutrition-title">{{ title }}</h3>
        <p class="nutrition-description">
            The table below shows nutritional values per serving without the additional fillings.
        </p>
        <table class="nutrition-table">
            <tbody>
                <tr>
                    <td class="nutrition-label">Calories</td>
                    <td class="nutrition-value">{{ nutrition.calories }}kcal</td>
                </tr>
                <tr>
                    <td class="nutrition-label">Carbs</td>
                    <td class="nutrition-value">{{ nutrition.carbs }}g</td>
                </tr>
                <tr>
                    <td class="nutrition-label">Protein</td>
                    <td class="nutrition-value">{{ nutrition.protein }}g</td>
                </tr>
                <tr>
                    <td class="nutrition-label">Fat</td>
                    <td class="nutrition-value">{{ nutrition.fat }}g</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: 'NutritionComponent',
    props: {
        title: {
            type: String,
            default: 'Nutrition'
        }
    },
    data() {
        return {
            nutrition: {
                calories: 277,
                carbs: 0,
                protein: 20,
                fat: 22
            }
        };
    }
}
</script>

<style scoped>
.nutrition-component {
    margin-bottom: 20px;
    padding: 20px;
}

.nutrition-title {
    font-size: 1.8rem;
    font-weight: bold;
    color: #5b2c1d;
    margin-bottom: 10px;
    text-align: left;
}

.nutrition-description {
    font-size: 1rem;
    color: #555;
    margin-bottom: 15px;
    text-align: center;
}

.nutrition-table {
    width: 100%;
    border-collapse: collapse;
    letter-spacing: 0.2px;
}

.nutrition-label {
    text-align: center;
    font-size: 1rem;
    color: #000000;
    padding: 5px 0;
}

.nutrition-value {
    text-align: center;
    font-size: 1rem;
    color: #5b2c1d;
    font-weight: bold;
    padding: 5px 0;
}

.nutrition-table tr td {
    text-align: center;
}

.nutrition-table tr:not(:last-child) td {
    border-bottom: 1px solid #ddd;
}

/* Media query para pantallas de 360px a 800px */
@media only screen and (width >=360px) and (width <=800px) {

    .nutrition-component {
        /* Reducir el padding para pantallas más pequeñas */
        padding: 10px;

    }
}
</style>