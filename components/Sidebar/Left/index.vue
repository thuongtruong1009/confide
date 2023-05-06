<script setup>
    const {defaultTransition } = import('@/composable/useTailwindConfig.ts')
    import { HomeIcon} from '@heroicons/vue/24/solid'
    import { HashtagIcon, BellIcon, InboxIcon, BookmarkIcon, DocumentTextIcon, UserIcon, DotsCircleHorizontalIcon } from '@heroicons/vue/24/outline'

</script>

<template>
<div class="flex flex-col h-screen">
    <div class="p-2 my-2 rounded-full hover:bg-blue-100 w-min dark:hover:bg-white-20" :class="defaultTransition">
        <nuxt-link to="/">
            <div class="w-8 h-8"><LogoTwitter /></div>
        </nuxt-link>
    </div>

    <div class="mt-2 space-y-3"></div>

    <SidebarLeftTab active>
        <template v-slot:icon>
            <HomeIcon />
        </template>
        <template v-slot:name>
            Home
        </template>
    </SidebarLeftTab>

     <SidebarLeftTab active>
        <template v-slot:icon>
            <HashtagIcon />
        </template>
        <template v-slot:name>
            Explore
        </template>
    </SidebarLeftTab>

    <SidebarLeftTab active>
        <template v-slot:icon>
            <BellIcon />
        </template>
        <template v-slot:name>
            Notifications
        </template>
    </SidebarLeftTab>

     <SidebarLeftTab active>
        <template v-slot:icon>
            <InboxIcon />
        </template>
        <template v-slot:name>
            Messages
        </template>
    </SidebarLeftTab>

    <SidebarLeftTab active>
        <template v-slot:icon>
            <BookmarkIcon />
        </template>
        <template v-slot:name>
            Bookmarks
        </template>
    </SidebarLeftTab>

     <SidebarLeftTab active>
        <template v-slot:icon>
            <UserIcon />
        </template>
        <template v-slot:name>
            Profile
        </template>
    </SidebarLeftTab>

    <SidebarLeftTab active>
        <template v-slot:icon>
            <DotsCircleHorizontalIcon />
        </template>
        <template v-slot:name>
            More
        </template>
    </SidebarLeftTab>
</div>
</template>