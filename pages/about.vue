<template>
    <Hero heading="About" subHeading="Profile assessment, personality type and education" :button='true'
        buttonText="Follow the white rabbit" buttonSVG="buttons/white-rabbit" buttonLink="/languages" class=""></Hero>
    <div class="flex flex-col text-white  w-full space-y-8 xl:p-32">
        <div
            class="flex flex-col  rounded-md p-4 bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg p-8">
            <h1 class="text-white text-3xl mb-6">Profile assessment</h1>
            <p>The individual is able to solve complex operational tasks. In addition, people with this score
                generally have a potential for effective problem solving with unfamiliar tasks and in more complex
                situations. A mix of routine work with clear instructions and medium to high complexity problem solving
                tasks generally is a good recipe for good performance and motivation over time. It is probably smart for
                you
                to establish methods and cooperation around the most strategic and complex aspects of your job.</p>
        </div>
        <div
            class="flex flex-col  rounded-md p-4 bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg p-8">
            <h1 class="text-white text-3xl mb-6 flex items-center">
                Personality Type - Meyers Brigs Assessment : INTJ Architect
            </h1>
            <div class="space-y-4">
                <p>INTJ stands for Introverted, Intuitive, Thinking, and Judging.
                </p>
                <p>It’s lonely at the top, and being one of
                    the rarest and most strategically capable personality types,
                    INTJs
                    know this all too well. INTJs form just two percent of the population. </p>
                <p>
                    People with the INTJ personality
                    type (Architects) are intellectually curious individuals with a deep-seated thirst for
                    knowledge.
                    INTJs
                    tend to value creative ingenuity, straightforward rationality, and self-improvement. They
                    consistently
                    work toward enhancing intellectual abilities and are often driven by an intense desire to
                    master any
                    and
                    every topic that piques their interest.
                </p>
                <NuxtLink to="https://www.16personalities.com/intj-personality">
                    <button class="text-white ml-2 px-4 py-1 mt-4 rounded-md border-solid border-white border-2 ">
                        Learn more</button>
                </NuxtLink>
            </div>
        </div>

        <div
            class="flow-root rounded-md bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg w-[90%] xl:w-[50%] md:w-[80%]  self-center p-8">
            <ul role="list" class="-mb-8">
                <li v-for="(event, eventIdx) in timeline" :key="event.id">
                    <div class="relative pb-8">
                        <span v-if="eventIdx !== timeline.length - 1"
                            class="absolute left-4 top-4 -ml-px h-full w-0.5 bg-white" aria-hidden="true" />
                        <div class="relative flex space-x-3">
                            <div>
                                <span
                                    :class="[event.iconBackground, 'flex h-8 w-8 items-center justify-center rounded-full ring-2 ring-[]']">
                                    <component :is="event.icon" class="h-5 w-5 text-white" aria-hidden="true" />
                                </span>
                            </div>
                            <div class="flex min-w-0 flex-1 justify-between space-x-4 pt-1.5">
                                <div>
                                    <p class="text-sm text-white-500">
                                        {{ event.content }}
                                    </p>
                                    <a :href="event.href" class="font-medium text-white-900">{{ event.target }}</a>
                                </div>
                                <div class="whitespace-nowrap text-right text-sm text-white-500">
                                    <time :datetime="event.datetime">{{ event.date }}</time>
                                </div>
                            </div>

                        </div>
                        <div v-if="event.child">
                            <div class="relative flex space-x-3 ml-8 mt-4" v-for="(item, index) in event.child"
                                :key=item.id>
                                <div>
                                    <span
                                        :class="[item.iconBackground, 'flex h-8 w-8 items-center justify-center rounded-full ring-2 ring-[]']">
                                        <component :is="item.icon" class="h-5 w-5 text-white" aria-hidden="true" />
                                    </span>
                                </div>
                                <div class="flex min-w-0 flex-1 justify-between space-x-4 pt-1.5">
                                    <div>
                                        <p class="text-sm text-white-500">
                                            {{ item.content }}
                                        </p>
                                        <a :href="item.href" class="font-medium text-white-900">{{ item.target }}</a>
                                    </div>
                                    <div class="whitespace-nowrap text-right text-sm text-white-500">
                                        <time :datetime="item.datetime">{{ item.date }}</time>
                                    </div>
                                </div>

                            </div>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
    </div>

</template>

<script lang="ts" setup>
definePageMeta({
    layout: 'default'
})

import { CheckIcon, HandThumbUpIcon, UserIcon, AcademicCapIcon, BriefcaseIcon, ArrowUturnLeftIcon, NewspaperIcon } from '@heroicons/vue/20/solid'

const timeline = [
    {
        id: 1,
        content: 'Graduated Matric',
        target: 'Backenfell High School',
        href: '#',
        date: 'December 2008',
        datetime: '2008-12-31',
        icon: UserIcon,
        iconBackground: 'bg-gray-400',
    },
    {
        id: 2,
        content: 'Studied in B.Eng Civil Engineering',
        target: 'Stellenbosch University',
        href: '#',
        date: 'Jan 2009 - July 2012',
        datetime: '2020-09-22',
        icon: AcademicCapIcon,
        iconBackground: 'bg-blue-500',
    },
    {
        id: 3,
        content: 'Worked as a Candidate Civil Engineer - Consulting Civil Quality Control in Fiber Optics Installation',
        target: 'KWCE Consulting Engineers',
        href: '#',
        date: 'Jan 2013 - May 2017',
        datetime: '2020-09-28',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
    },
    {
        id: 4,
        content: 'Career Change to Fiber Optics Engineering',
        target: 'From Civil Engineering to Fiber Optics Engineering',
        href: '#',
        date: 'May 2017',
        datetime: '2020-10-04',
        icon: ArrowUturnLeftIcon,
        iconBackground: 'bg-red-500',
    },
    {
        id: 5,
        content: 'Worked as a Core Network Project Manager - FTTH Core Network (Aerial and Ground Hybrid Fiber Optics Model for Fiber and civils)',
        target: 'Fiberhoods on behalf of Vumatel',
        href: '#',
        date: 'Jun 2017 - Mar 2018 ',
        datetime: '2020-09-30',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
        child: [{
            id: 1,
            content: 'Aerial Fiber Installation Certificate',
            target: 'Fiberhoods',
            href: '#',
            date: 'Jun 2017 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        ]
    },
    {
        id: 6,
        content: ' Worked as the Western Cape Provincial Wayleave Manager - FTTS Fiber Optic Engineering Department',
        target: 'ZTE Corporation',
        href: '#',
        date: 'Mar 2018 - Feb 2020',
        datetime: '2020-10-04',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
        child: [{
            id: 1,
            content: 'Project Management Certificate',
            target: 'Stellenbosch Business School',
            href: '#',
            date: 'Nov 2018 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Microsoft Excel Master Certificate',
            target: 'International Academy of Computer Training',
            href: '#',
            date: 'Nov 2018 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Project Management South Africa (PMSA) Certificate',
            target: 'Project Management South Africa (PMSA) - Professional Designation',
            href: '#',
            date: 'Apr 2019 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        }]
    },
    {
        id: 7,
        content: 'Career Change to Software Development',
        target: 'From Fiber Optics Engineering to Software Development',
        href: '#',
        date: 'Feb 2020',
        datetime: '2020-10-04',
        icon: ArrowUturnLeftIcon,
        iconBackground: 'bg-red-500',
    },
    {
        id: 8,
        content: 'Worked as a Junior React, Nextjs and PHP full-stack Developer',
        target: 'Lumico',
        href: '#',
        date: 'Mar 2020 - Nov 2022',
        datetime: '2020-10-04',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
        child: [{
            id: 1,
            content: 'Responsive Web Design Certification',
            target: 'freeCodeCamp',
            href: '#',
            date: 'Aug 2020 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Javascript Algorithms and Data Structures Certification',
            target: 'freeCodeCamp',
            href: '#',
            date: 'Jan 2021 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Front-end Development Libraries Certification',
            target: 'freeCodeCamp',
            href: '#',
            date: 'Jan 2021 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Professional Scrum Master (PSM I) Certification',
            target: 'Scrum.org',
            href: '#',
            date: 'Mar 2021 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Being Competent in Linux',
            target: 'TryHackMe',
            href: '#',
            date: 'Apr 2021 ',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        }]
    },
    {
        id: 9,
        content: 'Studied in B.sc Information Technology',
        target: 'Nortwest University',
        href: '#',
        date: 'Jan 2022 - Dec 2024',
        datetime: '2020-09-22',
        icon: AcademicCapIcon,
        iconBackground: 'bg-blue-500',
    },
    {
        id: 10,
        content: ' Worked as a Intermediate Vue javascript Frontend Developer',
        target: 'Exigent Group a company of Morae Global Corporation',
        href: '#',
        date: 'Nov 2022 - Feb 2023',
        datetime: '2020-10-04',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
    },
    {
        id: 11,
        content: ' Worked as a Team lead and Senior Vue and Nuxt Javascript Frontend Developer  (Promotion)',
        target: 'Exigent Group a company of Morae Global Corporation',
        href: '#',
        date: 'Feb 2023 - Feb 2024',
        datetime: '2020-10-04',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
        child: [{
            id: 1,
            content: 'Certified Vue.js Developer',
            target: 'Vue',
            href: '#',
            date: 'Apr 2023 - Present',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Certified Senior Vue.js Developer',
            target: 'Vue',
            href: '#',
            date: 'Apr 2023 - Present',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        },
        {
            id: 1,
            content: 'Certified Nuxt Developer',
            target: 'Nuxt',
            href: '#',
            date: 'March 2024 - Present',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        }, {
            id: 1,
            content: 'Certified Senior Nuxt Developer',
            target: 'Nuxt',
            href: '#',
            date: 'March 2024 - Present',
            datetime: '2020-09-30',
            icon: NewspaperIcon,
            iconBackground: 'bg-yellow-500',
        }]
    },
    {
        id: 12,
        content: 'Working as a Software Engineering Manager  (Promotion)',
        target: 'Exigent Group a company of Morae Global Corporation',
        href: '#',
        date: 'March 2024 - Present',
        datetime: '2020-10-04',
        icon: BriefcaseIcon,
        iconBackground: 'bg-green-500',
    },
]
</script>

<style>

</style>
