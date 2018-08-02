<template>
    <div id="app">
        <h3>Wanna Jokes? C'mmon</h3>
        <button class="btn btn-primary" @click="initJokes" >Ten jokes random</button>
        <button class="btn btn-success" @click="addJoke" >Ten jokes random</button>
       <br>
        <span v-for="type in types">
            <input 
                type="checkbox" 
                :value="type"
                v-model="checkedTypes"
                checked
            >
            <label for="">{{type}}</label>&nbsp;
        </span>
       <br>
       <div class="row">
           <Joke
                v-for="(joke, index) in $store.state.jokes"
                v-show="checkedTypes.includes(joke.type)"
                :joke="joke"
                :index="index"
                :  key="index"
           />
       </div>
    </div>
</template>
 
<script>
import { mapActions } from 'vuex'
import Joke from './Joke.vue'

export default {
    data() {
        return {
            types: ['general', 'knock-knock', 'programming'],
            checkedTypes: ['general', 'knock-knock', 'programming']
        }
    },
    methods: mapActions([
        'initJokes',
        'addJoke',
    ]),
    components: {
        Joke  
    }    
}

</script>
