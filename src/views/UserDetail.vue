<template>
    ini halaman user detail {{ $route.params.name }}
    <br>
    <RouterLink :to="'/user/' + $route.params.name + '/posts'">{{ $route.params.name }}'s posts'</RouterLink>
    <br>
    <RouterLink :to="'/user/' + $route.params.name + '/profile'">{{ $route.params.name }}'s profile'</RouterLink>
</template>