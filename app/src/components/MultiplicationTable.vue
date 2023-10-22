<template>
<div>
    <h1>Multiplication Table</h1>
    <div>
    <label for="number">Enter a number: </label>
    <input type="number" id="number" v-model="selectedNumber">
    </div>
    <hr style="margin: 20px;"/>
    <table class="center-table">
    <thead>
        <tr>
        <th>Multiplication</th>
        <th>Result</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="multiplier in multipliers" :key="multiplier">
        <td>{{ selectedNumber }} * {{ multiplier }}</td>
        <td>{{ selectedNumber * multiplier }}</td>
        </tr>
    </tbody>
    </table>
</div>
</template>

<script>
export default {
data() {
    return {
    selectedNumber: 1,
    };
},
computed: {
    multipliers() {
    return [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];
    },
},
};
</script>

<style>
.center-container {
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
height: 100vh;
text-align: center;
}

.center-table {
margin: 0 auto;
border-collapse: collapse; /* Merge table borders */
border: 1px solid #000; /* Add border to the table */
}

.center-table th,
.center-table td {
border: 1px solid #000; /* Add border to table cells */
padding: 8px; /* Adjust padding for better visual spacing */
}

.center-table th {
background-color: #f0f0f0; /* Add a background color for header cells */
}
</style>
