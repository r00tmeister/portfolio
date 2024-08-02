<template>
  <div class="rounded-md p-4 bg-black bg-transparent bg-opacity-20 backdrop:filter backdrop-blur-md shadow-lg">
    <div class="mx-auto max-w-2xl px-4 py-24 sm:px-6 sm:py-32 lg:max-w-7xl lg:px-8">
      <div class="mx-auto max-w-3xl text-center">
        <h2 class="text-white text-xl md:text-3xl font-bold font-mono text-center mb-6 flex flex-col">Recent Projects
        </h2>
        <p class="text-white px-8 text-md md:text-2xl  font-mono text-center ">You are only as good as your
          last project.</p>
      </div>

      <div class="mt-16 space-y-16">
        <div v-for="(feature, featureIdx) in features" :key="feature.name"
          class="flex flex-col-reverse lg:grid lg:grid-cols-12 lg:items-center lg:gap-x-8">
          <div
            :class="[featureIdx % 2 === 0 ? 'lg:col-start-1' : 'lg:col-start-8 xl:col-start-9', 'mt-6 lg:col-span-5 lg:row-start-1 lg:mt-0 xl:col-span-4']">
            <h3 class="text-lg font-medium text-white">{{ feature.name }}</h3>
            <p class="mt-2 text-sm text-gray-500">{{ feature.description }}</p>
            <NuxtLink :to="feature.siteUrl">
              <button class=" text-white px-4 py-1 mt-4 rounded-md border-solid border-white border-2"><span
                  class="text-sm md:text-lg">View Site</span>
              </button>
            </NuxtLink>
            <NuxtLink :to="feature.docsUrl" v-if="feature.docsUrl.length > 0">
              <button
                class=" text-white ml-2 px-4 py-1 mt-4 rounded-md border-solid border-white border-2"><span
                  class="text-sm md:text-lg ">View Documentation</span>
              </button>
            </NuxtLink>
            <div class="mt-6 flex space-x-2">
              <div class="text-white justify-center flex flex-col items-center" v-for="(item, index) in feature.stack"
                :key="item.id">
                <img :src="item.imageSrc" :alt="item.imageAlt" width="50" height="50" />
                <span>{{ item.name }}</span>
              </div>
            </div>
          </div>
          <div :class="[featureIdx % 2 === 0 ? 'lg:col-start-6 xl:col-start-5' : 'lg:col-start-1'
            , 'flex-auto lg:col-span-7 lg:row-start-1 xl:col-span-8']">
            <div class="aspect-h-2 aspect-w-5 overflow-hidden rounded-lg bg-gray-100">
              <img :src="feature.imageSrc" :alt="feature.imageAlt" class="object-cover object-center" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ragChatbotImage from '@/assets/images/choice/rag-chatbot.png';
import cmsImage from '@/assets/images/choice/cms.png';
import piiImage from '@/assets/images/choice/pii.png';
import webAppImage from '@/assets/images/choice/webapp.png';

const features = reactive([
  {
    name: 'Retrieval Augmented Generation AI Chatbot',
    description:
      'The RAG chatbot is a state of the art chatbot that uses the RAG model to generate responses to user queries. The chatbot is trained on a large dataset of user queries and files uploaded by the users, files are OCRd, chunked, embedded as vectors, stored in a vector database and is then able to generate responses that are relevant to the user query using cosine similarities to find relevant data.',
    imageSrc: ragChatbotImage,
    siteUrl: 'https://white-hill-02be3721e.5.azurestaticapps.net/',
    docsUrl: 'https://purple-pebble-0f8ea6e03.5.azurestaticapps.net/',
    imageAlt: 'RAG chatbot',
    stack: [
      {
        id: 1,
        name: 'FastAPI',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/fastapi/fastapi-original.svg',
        imageAlt: 'FastAPI',
      },
      {
        id: 2,
        name: 'NuxtJS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nuxtjs/nuxtjs-original.svg',
        imageAlt: 'NuxtJS',
      },
      {
        id: 3,
        name: 'PostgreSQL',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg',
        imageAlt: 'PostgreSQL',
      },
      {
        id: 4,
        name: 'Azure',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg',
        imageAlt: 'Azure',
      },
      {
        id: 5,
        name: 'TailwindCSS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original-wordmark.svg',
        imageAlt: 'TailwindCSS',
      }
    ]
  },
  {
    name: 'Personal Identifiable Information (PII) Detection and Redaction Tool',
    description:
      'The PII detection and redaction tool is a state of the art tool that uses machine learning to detect and redact personal identifiable information from documents. The tool is able to detect a wide range of PII including names, addresses, phone numbers, and social security numbers. Users have the ability to export redacted documents in a variety of formats including PDF, Word, and Excel.',
    imageSrc: piiImage,
    siteUrl: 'https://lemon-field-05638fa03.4.azurestaticapps.net/',
    docsUrl: 'https://proud-mud-001e54f03.5.azurestaticapps.net/',
    imageAlt: 'PII detection and redaction tool',
    stack: [
      {
        id: 1,
        name: 'FastAPI',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/fastapi/fastapi-original.svg',
        imageAlt: 'FastAPI',
      },
      {
        id: 2,
        name: 'NuxtJS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nuxtjs/nuxtjs-original.svg',
        imageAlt: 'NuxtJS',
      },
      {
        id: 3,
        name: 'PostgreSQL',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original.svg',
        imageAlt: 'PostgreSQL',
      },
      {
        id: 4,
        name: 'Azure',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg',
        imageAlt: 'Azure',
      },
      {
        id: 5,
        name: 'TailwindCSS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original-wordmark.svg',
        imageAlt: 'TailwindCSS',
      }
    ]
  },
  {
    name: 'Content Management System (CMS) for a large lawyer firm, integrated with Imanage a document management system',
    description:
      'The CMS system is a state of the art system that allows the law firm to manage their content, users, and permissions. The CMS system is integrated with Imanage a document management system that allows the law firm to manage their documents, files, and folders. The CMS system is able to generate reports, track user activity, and manage user permissions.',
    imageSrc: cmsImage,
    siteUrl: 'https://online.polsinelli.com/',
    docsUrl: '',
    imageAlt: 'CMS system integrated with Imanage',
    stack: [
      {
        id: 1,
        name: 'Laravel',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg',
        imageAlt: 'FastAPI',
      },
      {
        id: 2,
        name: 'VueJS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/vuejs/vuejs-original.svg',
        imageAlt: 'VueJS',
      },
      {
        id: 3,
        name: 'MySQL',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mysql/mysql-original.svg',
        imageAlt: 'MySQL',
      },
      {
        id: 4,
        name: 'Azure',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azure/azure-original.svg',
        imageAlt: 'Azure',
      },
      {
        id: 5,
        name: 'TailwindCSS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original-wordmark.svg',
        imageAlt: 'TailwindCSS',
      }
    ]
  },
  {
    name: 'Webapp for a content creation company',
    description:
      'Webapp for a content creation company that allows internal admin users to create, edit, and delete content for a public blog. The webapp is able guide potential clients to what they need by means of a questionaire and then provide them with a quote and setup a meeting with the relevant departments. The site also showcases the companies portfolio and allows users to contact the company.',
    imageSrc: webAppImage,
    siteUrl: 'https://lumico.co.za/',
    docsUrl: '',
    imageAlt: 'Webapp for a content creation company',
    stack: [
      {
        id: 1,
        name: 'DynamoDB',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/dynamodb/dynamodb-original.svg',
        imageAlt: 'DynamoDB',
      },
      {
        id: 2,
        name: 'GraphQL',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/graphql/graphql-plain.svg',
        imageAlt: 'GraphQL',
      },
      {
        id: 3,
        name: 'React',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg',
        imageAlt: 'React',
      },
      {
        id: 4,
        name: 'AWS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/amazonwebservices/amazonwebservices-original-wordmark.svg',
        imageAlt: 'Azure',
      },
      {
        id: 5,
        name: 'TailwindCSS',
        imageSrc: 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/tailwindcss/tailwindcss-original-wordmark.svg',
        imageAlt: 'TailwindCSS',
      }
    ]
  },
])
</script>