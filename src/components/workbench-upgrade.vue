<script setup>
import { ref, computed } from 'vue';

// Component data
const data = ref({
    meadows: {
        choppingBlock: {
            wood: 10,
            flint: 10
        },
        tanningRack: {
            wood: 10,
            flint: 15,
            leatherScraps: 20,
            deerHide: 5
        }
    },

    darkForest: {
        adze: {
            fineWood: 10,
            bronze: 3
        }
    },

    mountains: {
        toolShelf: {
            fineWood: 10,
            iron: 4,
            obsidian: 4
        }
    }

});

// Computed properties
const computedProperties = computed(() => {
    // Your computed properties logic goes here
});

// Methods
const methods = {
    // Your component methods go here
};
</script>

<template>
    <div class="workbench-upgrade">
        <a>workbench-upgrade</a>
    </div>
</template>

<style scoped>
.workbench-upgrade {
    /* Your component styles go here */
}
</style>