<template>
    <div id="app">
        <h3>Starbase Router</h3>
        <h4>
            <router-link to="/data/people">Meet the characters</router-link> |
            <router-link to="/data/planets">Explore the planets</router-link> 
        </h4>
        <router-view></router-view>  
    </div>
</template>
