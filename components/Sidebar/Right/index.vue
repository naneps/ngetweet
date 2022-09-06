<template>
    <div class="flex flex-col">
        
        <!-- Preview Card what happening -->
        <SidebarRightPreviewCard title="What Happening"> 
            <SidebarRightPreviewCardItem v-for="whatHappening in whatHappeningItems" :key="whatHappening">
                <div>
                    <h1 class="font-bold text-gray-800 text-md dark:text-white">{{ whatHappening.title }}</h1>
                    <p class="text-xs text-gray-400">{{ whatHappening.count }}</p>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>
        <!-- Preview Card  wo to follow-->
        <SidebarRightPreviewCard title="Who to follow">
            <SidebarRightPreviewCardItem v-for="whoToFollow in whoToFollowItems" :key="whoToFollow" >
                <div class="flex flex-row  item-center justify-between p-2 ">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">
                        <div class="flex flex-col ml-3">
                            <h1 class="text-sm font-bold dark:text-white text-gray-900">
                                {{ whoToFollow.name }}
                            </h1>
                            <p class="text-xs text-gray-400">
                                {{ whoToFollow.handle }}
                            </p>
                        </div>
                        
                    </div>
                    <div class="flex h-full">
                        <button class="px-4 py-2 text-xs font-bold text-white bg-black dark:text-black dark:bg-white rounded-full">
                            Follow
                        </button>
                    </div>
                </div>
            </SidebarRightPreviewCardItem>
        </SidebarRightPreviewCard>
    </div>
</template>
<script setup>
    const whatHappeningItems = ref([
        {
            title: 'What Happening',
            count: '20k Tweets',
        },
        {
            title: 'BBm Naik',
            count: '200k Tweets',
        },
        {
            title: 'What Happening',
            count: '20k Tweets',
        },
        {
            title: 'BBm Naik',
            count: '200k Tweets',
        },
    ])
    const whoToFollowItems = ref([
        {
            name: 'Ahmad',
            handle:'@ahmad',
            image: 'https://picsum.photos/200/200',
        },
        {
            name: 'Ahmad',
            handle:'@ahmad',
            image: 'https://picsum.photos/200/200',
        },
        {
            name: 'Ahmad',
            handle:'@ahmad',
            image: 'https://picsum.photos/200/200',
        },

    ])
</script>