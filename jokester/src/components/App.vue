<template>
    <div id="app">
        <h3>Wanna Jokes? C'mmon</h3>
        <button class="btn btn-primary" @click="initJokes" >Ten jokes random</button>
        <div class="">
            {{ $store.state }}
        </div>
    </div>
</template>

<script>
import { mapActions } from 'vuex'

export default {
    methods: mapActions([
        'initJokes'
    ])    
}

</script>
