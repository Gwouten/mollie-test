<template>
<div>
    <h3>User ID: {{$route.params.id}}</h3>
    <router-link tag="button" :to="{ name: 'userEdit', params: { id: $route.params.id }, query: {locale: 'en', q: 100} }">Edit user data</router-link>
</div>
</template>
