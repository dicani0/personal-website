<script setup>
import ExperienceItem from "./ExperienceItem.vue";
</script>

<template>
  <section class="py-12 pt-16">
    <div class="container mx-auto px-4">
      <h2 class="text-4xl font-bold text-center text-gray-800 mb-8">Professional Experience</h2>
      <div class="space-y-8">
        <ExperienceItem
            position="Backend Developer"
            company="Sailing Byte"
            date="January 2024 - Present(Mandate Contract)"
            :points="[
                'Creation of an application for aggregation and presentation of data of companies, their investors and acquirers and the flow of funds between them',
                'Integration of stripe payment system and subscription management',
                'Creation of an api accepting data coming from webscraping',
                'Sql query optimization'
                ]"
            :technologies="['Laravel', 'PHP', 'MySQL', 'Tailwind CSS', 'Bootstrap', 'Git', 'Asana', 'Laravel Orchid']"
        />
        <ExperienceItem
            position="Backend Developer"
            company="Escola S.A."
            date="February 2022 - December 2023"
            :points="[
                'Development and implementation of backend solutions for LMS application',
                'Creation of new and editing of existing functionalities for ecommerce system',
                'Work with front-end team to integrate APIs ensuring seamless communication and functionality between application layers',
                'Creating application similar to google meets but more complex, allowing the creation of meetings, tasks, and votes, along with a live agenda during the meeting'
                ]"
            :technologies="['Laravel', 'PHP', 'MySQL', 'PostgreSQL', 'Git', 'Jira', 'Atlassian', 'Websockets', 'Laravel Echo', 'Docker', 'Kubernetes']"
        />

        <ExperienceItem
            position="Backend Developer"
            company="COM40"
            date="October 2020 - February 2022"
            :points="[
                'Design, develop and maintain in-house applications to automate and streamline the work of other departments',
                ]"
            :technologies="['Laravel', 'PHP', 'MySQL', 'Git', 'Docker', 'JavaScript', 'Angular']"
        />

        <ExperienceItem
            position="Technical assistance consultant"
            company="Multimedia Polska"
            date="October 2012 - August 2017"
            :points="[
                'Providing technical assistance to customers',
                'Troubleshooting',
                ]"
        />

      </div>
    </div>
  </section>
</template>

<style scoped>

</style>