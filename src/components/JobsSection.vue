<script setup>
// Temporary sample data. We'll swap this for an API call later.
const jobs = [
    {
        id: 1,
        type: 'Full-Time',
        title: 'Front-End Engineer (Vue)',
        description:
            'Build accessible, performant user interfaces in Vue 3, collaborate with designers, and ship features weekly.',
        salary: '$110,000 – $140,000',
    },
    {
        id: 2,
        type: 'Full-Time',
        title: 'UI Engineer',
        description:
            'Own UI components, write clean Tailwind-powered layouts, and improve DX across the team.',
        salary: '$95,000 – $120,000',
    },
    {
        id: 3,
        type: 'Full-Time',
        title: 'Senior Vue Developer',
        description:
            'Lead front-end architecture, mentor teammates, and drive UX improvements across our web apps.',
        salary: '$135,000 – $165,000',
    },
]
</script>

<template>
    <!-- same bg as Hero: blue-50 -->
    <section class="bg-blue-50 py-16">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <!-- Section heading -->
            <h2 class="text-center text-3xl font-bold text-blue-600">Browse Jobs</h2>

            <!-- Cards -->
            <div class="mt-10 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
                <article v-for="job in jobs" :key="job.id" class="bg-white rounded-xl shadow p-6 flex flex-col">
                    <!-- Top-left badge -->
                    <span class="text-sm font-medium text-gray-500 uppercase tracking-wide">
                        {{ job.type }}
                    </span>

                    <!-- Job title -->
                    <h3 class="mt-2 text-xl font-semibold text-gray-900">
                        {{ job.title }}
                    </h3>

                    <!-- Description -->
                    <p class="mt-3 text-gray-700">
                        {{ job.description }}
                    </p>

                    <!-- Footer: salary + apply -->
                    <div class="mt-6 flex items-center justify-between">
                        <span class="text-blue-600 font-light">
                            {{ job.salary }}
                        </span>

                        <button type="button"
                            class="rounded-lg bg-blue-600 px-4 py-2 text-white font-semibold hover:bg-blue-700 transition">
                            Apply
                        </button>
                    </div>
                </article>
            </div>
        </div>
    </section>
</template>
