<template>
    <div className="container">
        <div className='box'>
            <h1 className="multiplication-header">Multiplication Table 🚀</h1>
            <div className="input-container">
            <label for="number" className="input-label">Enter a number: </label>
            <input type="number" id="number" v-model="selectedNumber">
            </div>
            <div>
                <table className="table">
                <thead className="table-header">
                    <tr>
                        <th className="table-header">Multiplication</th>
                        <th className="table-header">Result</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="multiplier in multipliers" :key="multiplier">
                    <td className="table-cell center">{{ selectedNumber }} * {{ multiplier }}</td>
                    <td className="table-cell center">{{ selectedNumber * multiplier }}</td>
                    </tr>
                </tbody>
                </table>
            </div>
        </div>
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
@import 'tailwindcss/base';
@import 'tailwindcss/components';
@import 'tailwindcss/utilities';

.box {
    background-color: #f5f5f5;
    padding: 30px;
}

.container {
    display: flex;
    height: 100%;
    width: 100%;
    justify-content: center;
    align-items: center;
    border-radius: 0.25rem;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
    padding: 1rem;
    background: linear-gradient(45deg, #FF0000, #FFA500, #FFFF00, #008000, #0000FF, #4B0082, #8B00FF);
    background-size: 200% 200%;
    animation: rainbowBackground 10s linear infinite;
}

@keyframes rainbowBackground {
    0% {
        background-position: 0 100%;
    }
    100% {
        background-position: 100% 0;
    }
}

.multiplication-header {
    font-size: 2rem;
    font-weight: bold;
    margin-bottom: 1rem;
}

.input-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
}

.input-label {
    font-size: 1rem;
    margin-right: 1rem;
}

.input-field {
    border: 2px solid #ccc;
    border-radius: 0.25rem;
    padding: 0.5rem;
    font-size: 1rem;
}

.table {
    height: 100%;
    width: 100%;
    border-collapse: collapse;
    padding: 50px;
}

.table-header {
    padding: 0.5rem 1rem;
    background-color: #eee;
}

.table-cell {
    padding: 0.5rem 1rem;
    border-bottom: 1px solid #ccc;
    font-size: 1rem;
}

.table-cell:nth-child(even) {
    background-color: #f5f5f5;
}

.table-row:hover {
    background-color: #e0e0e0;
    cursor: pointer;
}

.table-row:hover .table-cell {
    transition: background-color 0.3s ease-in-out;
}
</style>
