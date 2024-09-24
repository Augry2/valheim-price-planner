<script setup>
import { ref, computed } from 'vue';

// Component data
const data = ref({
    // Adding locations array under data
    locations: [
        {
            name: "Meadows",
            items: {
                choppingBlock: {
                    name: "Chopping Block",
                    wood: 10,
                    flint: 10
                },
                tanningRack: {
                    name: "Tanning Rack",
                    wood: 10,
                    flint: 15,
                    leatherScraps: 20,
                    deerHide: 5
                }
            },
            showItems: false,
        },
        {
            name: "Dark Forest",
            items: {
                adze: {
                    name: "Adze",
                    fineWood: 10,
                    bronze: 3
                }
            },
            showItems: false,
        },
        {
            name: "Mountains",
            items: {
                toolShelf: {
                    name: "Tool Shelf",
                    fineWood: 10,
                    iron: 4,
                    obsidian: 4
                }
            },
            showItems: false,
        }
    ]
});


// Methods
const toggleItems = (location) => {
    location.showItems = !location.showItems; // Toggle showItems on click
    console.log(location.showItems);
};

</script>

<template>
    <div class="workbench-upgrade">
        <h2>Workbench Upgrades</h2>

        <ul>
            <li v-for="location in data.locations" :key="location.name">
                <h3>{{ location.name }} <button @click="toggleItems(location)">+</button></h3>
                <ul v-if="location.showItems">
                    <li v-for="item in location.items" :key="item.name">
                        {{ item.name }}
                    </li>

                </ul>
            </li>
        </ul>

    </div>
</template>

<style scoped>
.workbench-upgrade {
    /* Your component styles go here */
}
</style>