<template>
    <header class="navbar bg-base-100">
        <div class="flex-none">
            <a class="btn btn-ghost text-xl normal-case text-white">Company Name</a>
        </div>
        <div class="flex-none">
            <ul class="menu menu-horizontal p-0">
                <li>
                    <router-link class="text-white" to="/">Home</router-link>
                </li>
                <li>
                    <router-link class="text-white" to="/not-found">NotFound</router-link>
                </li>
                <li>
                    <router-link class="text-white" :to="`/hi/${counter.count}`" replace>DynamicRoute:{{ counter.count }}</router-link>
                </li>
                <li>
                    <router-link class="text-white" to="/about">About</router-link>
                </li>
                <li>
                    <LanguageSwitcher />
                </li>
            </ul>
        </div>
        <div class="flex-1">
        <slot></slot>
        </div>
    </header>
</template>

<script setup lang="ts">
import { useCounterStore } from '@/stores/counter';

const counter = useCounterStore()
</script>
