<template>
    <DocSectionText v-bind="$attrs">
        <p>
            MultiSelect is used with the <i>v-model</i> property for two-way value binding along with the <i>options</i> collection. Label and value of an option are defined with the <i>optionLabel</i> and <i>optionValue</i> properties respectively.
            Note that, when options are simple primitive values such as a string array, no <i>optionLabel</i> and <i>optionValue</i> would be necessary.
        </p>
    </DocSectionText>
    <div class="card flex justify-center">
        <MultiSelect v-model="selectedCities" :options="cities" optionLabel="name" filter placeholder="Select Cities" :maxSelectedLabels="3" class="w-full md:w-80" />
    </div>
    <DocSectionCode :code="code" />
</template>

<script setup lang="ts">
import MultiSelect from '@/volt/MultiSelect.vue';
import { ref } from 'vue';

const selectedCities = ref(null);
const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);

const code = ref(`
<template>
    <div class="card flex justify-center">
        <MultiSelect v-model="selectedCities" :options="cities" optionLabel="name" filter placeholder="Select Cities" :maxSelectedLabels="3" class="w-full md:w-80" />
    </div>
</template>

<script setup lang="ts">
import MultiSelect from '@/volt/MultiSelect.vue';
import { ref } from 'vue';

const selectedCities = ref(null);
const cities = ref([
    { name: 'New York', code: 'NY' },
    { name: 'Rome', code: 'RM' },
    { name: 'London', code: 'LDN' },
    { name: 'Istanbul', code: 'IST' },
    { name: 'Paris', code: 'PRS' }
]);
<\/script>
`);
</script>
