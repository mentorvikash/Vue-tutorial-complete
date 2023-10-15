<template>
    <div>
        <button @click="activeTab = 'TabA'">Tab A</button>
        <button @click="activeTab = 'TabB'">Tab B</button>
        <button @click="activeTab = 'TabC'">Tab C</button>
    </div>
    <div>

        <!-- will help to preserve the state -->
        <keep-alive>
            <component :is="activeTab" />
        </keep-alive>
        <!-- 
        <TabA v-if="activeTab === 'TabA'" />
        <TabB v-if="activeTab === 'TabB'" />
        <TabC v-if="activeTab === 'TabC'" /> 
    -->
    </div>
</template>

<script>
import TabA from './TabA.vue';
import TabB from './TabB.vue';
import TabC from './TabC.vue';

export default {
    name: 'DynamicTab',
    data() {
        return {
            activeTab: 'TabA'
        }
    },
    components: {
        TabA,
        TabB,
        TabC,
    }
}
</script>

<style scoped></style>

<!-- keepAlive tag is used when we not want to rerender our component again and again and preserve its state -->