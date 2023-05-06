<script setup>
const whatsHappenings = ref([
    {
        title: "SpaceX",
        count: "18.8K Tweets"
    },
    {
        title: "#CodingIsFun",
        count: "8.8K Tweets"
    },{
        title: "#artforall",
        count: "1.8K Tweets"
    }
])

const whoToFollows = ref([
    {
        name: "Ahhehe",
        handle: "@dede",
        image: "https://picsum.photos/200/200"
    },
    {
        name: "Ahhehe",
        handle: "@dede",
        image: "https://picsum.photos/200/200"
    },{
        name: "Ahhehe",
        handle: "@dede",
        image: "https://picsum.photos/200/200"
    }
])
</script>


<template>
    <div class="flex flex-col">
        <!-- Card: What's happening -->
        <SidebarRightPreviewCard title="What's happening">
            <SidebarRightPreviewCardItem v-for="(item, i) in whatsHappenings" :key="i">
                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{item.title}}</h2>
                    <p class="text-xs text-gray-400">{{item.count}}</p>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>

        <!-- Card: Who to follow -->
        <SidebarRightPreviewCard title="Who to follow">
            <SidebarRightPreviewCardItem v-for="(item, i) in whoToFollows" :key="i">
                <div class="flex flex-row justify-between items-center p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="item.image" :alt="item.name">
                        <div class="flex flex-col ml-2">
                            <h1 class="text-sm font-bold text-gray-900 dark:text-white">{{item.name}}</h1>
                            <p class="text-xs text-gray-400">{{item.handle}}</p>
                        </div>
                    </div>
                    <div class="flex items-center h-full">
                        <button class="px-4 py-2 font-bold text-xs text-white dark:text-black bg-black dark:bg-white rounded-full">Follow</button>
                    </div>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>

        <!-- Card: Trends for you -->
    </div>
</template>