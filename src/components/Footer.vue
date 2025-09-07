<template>
    <footer class="bg-blue-600 text-white py-8 mt-16">
        <div class="max-w-7xl mx-auto px-6 lg:px-8">
            <div class="flex flex-col md:flex-row items-center justify-between gap-6">

                <div class="text-2xl font-bold">Indeed</div>


                <div class="flex flex-wrap justify-center gap-6 text-sm">
                    <a href="#" class="hover:text-blue-200">About</a>
                    <a href="#" class="hover:text-blue-200">Jobs</a>
                    <a href="#" class="hover:text-blue-200">Employers</a>
                    <a href="#" class="hover:text-blue-200">Contact</a>
                </div>


                <div class="text-sm text-blue-200">
                    © {{ new Date().getFullYear() }} Indeed. All rights reserved.
                </div>
            </div>
        </div>
    </footer>
</template>
