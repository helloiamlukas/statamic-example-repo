<template>
    <div>
        <v-select
            :value="value"
            :filterable="false"
            label="name"
            :options="[
                { name: 'Option 1', value: 'option-1' },
                { name: 'Option 2', value: 'option-2' },
                { name: 'Option 3', value: 'option-3' },
                { name: 'Option 4', value: 'option-4' },
                { name: 'Option 5', value: 'option-5'},
                   { name: 'Option 6', value: 'option-6'},
                   { name: 'Option 7', value: 'option-7'},
                   { name: 'Option 8', value: 'option-8'},
                   { name: 'Option 9', value: 'option-9'},
                   { name: 'Option 10', value: 'option-10'},
                   { name: 'Option 11', value: 'option-11'},
                   { name: 'Option 12', value: 'option-12'},
            ]"
            :placeholder="config.placeholder"
            :disabled="isReadOnly"
            :is-read-only="isReadOnly"
            @search:focus="$emit('focus')"
            @search:blur="$emit('blur')"
        >
            <template #option="option">
                <div class="flex items-center">
                    {{ option.name }}
                </div>
            </template>
        </v-select>
    </div>
</template>

<script>
import vSelect from 'vue-select'

export default {
    mixins: [Fieldtype],
    components: {
        vSelect,
    },
}
</script>
