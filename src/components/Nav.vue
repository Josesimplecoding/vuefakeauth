<template>
    <div class="text-indigo-200 bg-indigo-900">
        <div class="container flex items-center justify-between mx-auto">
            <h1 class="text-3xl font-thin tracking-tighter">
                Vue<span class="font-normal">FakeAuth</span></h1>
            <nav>
                <ul class="flex space-x-4">
                    <router-link to="/">
                        <li class="px-4 py-8 hover:cursor-pointer hover:bg-indigo-500 hover:text-indigo-800"> Home </li>
                    </router-link>
                    <router-link to="/about">
                        <li class="px-4 py-8 hover:cursor-pointer hover:bg-indigo-500 hover:text-indigo-800">About</li>
                    </router-link>
                    <router-link to="/login">
                        <li class="px-4 py-8 hover:cursor-pointer hover:bg-indigo-500 hover:text-indigo-800">Login</li>
                    </router-link>
                        <router-link to="/secret">
                        <li class="px-4 py-8 hover:cursor-pointer hover:bg-indigo-500 hover:text-indigo-800">Secret</li>
                    </router-link>
                </ul>
            </nav>
        </div>
    </div>
</template>