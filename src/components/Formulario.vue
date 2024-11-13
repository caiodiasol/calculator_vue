<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    getNumber1: Function,
    getNumber2: Function,
    getOperador: Function,
    resultado: [Number, String]
});
</script>

<template>
    <form class="calculator p-4">
        <div class="row mb-3">
            <div class="col mb-3">
                <input placeholder="Enter a number" type="number" class="form-control mb-3 text-center"
                    @keyup="props.getNumber1" />
            </div>
            <div class="col">
                <input placeholder="Enter a number" type="number" class="form-control mb-3 text-center"
                @keyup="props.getNumber2" />
            </div>
            <h5 class="text-center ">Operators</h5>
        </div>
        <div class="col-md-s mb-4 text-center">
            <select class="form-control text-center operator-select" @change="props.getOperador">
                <option value="add" class="add text-center">+</option>
                <option value="subtract" class="subtract text-center">-</option>
                <option value="multiply" class="multiply text-center">*</option>
                <option value="divide" class="divide text-center">/</option>
            </select>
        </div>
        <div>
            <div class="row">
                <div class="col">
                    <h5 class="text-center result-container">Result</h5>
                </div>
                <div class="row">
                    <div class="col">
                        <h3 class="black-text fs-0 text-center fw-bold ps-s mb-2 resultado" > {{ props.resultado }} </h3>
                    </div>
                </div>
            </div>
        </div>
    </form>
</template>

<style scoped>
.calculator{
    max-width: 400px;
    margin: auto;
    border-radius: 10px;
    background: #f0f0f0;
    box-shadow: 1px 6px 12px rgba(0, 0, 0, 0.1);
}

.form-control{
    border: 2px solid #323438;
    border-radius: 8px;
    transition: border-color 0.3s;
}

.form-control:focus {
    border-color: #007bff;
    box-shadow: 1px 2px 8px rgba(0, 123, 255, 0.2);
}

.operator-select{
    border: 2px solid #323438;
    border-radius: 8px;
    transition: border-color 0.3s;
}

.operator-select:focus {
    border-color: #007bff;
    box-shadow: 0px 0px 8px rgba(0, 123, 255, 0.2);
}

.result-container{
    background: #f0f0f0;
    padding: 10px;
    border-radius: 10px;
    margin-top: 20px;
}

.resultado{
    font-size: 2rem;
    color: #28a745;
    font-weight: bold;
}


.bg-vue-dark {
    background: #030322;
}

input[type=number]::-webkit-inner-spin-button {
    -webkit-appearance: none;
    margin: 0;
}

@media screen and (max-width: 768px) {
    .form-control {
        text-align: center;
    }

    select {
        padding-left: 48%;
        padding-right: 48%;
    }
}
</style>
