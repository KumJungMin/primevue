<template>
    <!-- TODO: test this -->
    <div>
        <div :style="{ backgroundColor: 'red', width: '200vw', height: '20px' }"></div>
        <Dialog v-model:visible="visible" modal header="My modal" :style="{ width: '50vw' }">
            <Dropdown v-model="selected" :options="items" placeholder="Select an item" />
        </Dialog>
        <Button label="Open Modal" @click="visible = true" />
    </div>
</template>

<script>
import Dropdown from 'primevue/dropdown';
import Dialog from 'primevue/dialog';
import Button from 'primevue/button';

export default {
    setup() {
        definePageMeta({
            layout: ''
        });
    },
    data() {
        return {
            visible: false,
            selected: null,
            items: [
                { label: 'Item 1', value: 'Item 1' },
                { label: 'Item 2', value: 'Item 2' },
                { label: 'Item 3', value: 'Item 3' }
            ]
        };
    },
    components: {
        Dropdown,
        Dialog,
        Button
    }
};
</script>
