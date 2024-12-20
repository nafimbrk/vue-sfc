<template>
    <h1>ini halaman user</h1>

    <h2>list user</h2>

    <ul>
        <li v-for="user in users">
            <RouterLink :to="'/user/' + user.params">
                {{ user.name }}
            </RouterLink>
        </li>
    </ul>
</template>

<script>
import { RouterLink } from 'vue-router';

export default {
    data() {
        return {
            users: [
                { params: 'meg', name: 'Meg' },
                { params: 'ben', name: 'Ben' },
                { params: 'greg', name: 'Greg' }
            ]
        };
    },
    components: { RouterLink }
}
</script>