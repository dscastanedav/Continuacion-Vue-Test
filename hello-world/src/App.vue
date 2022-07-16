<template>
  <!-- 
  <h2 v-if="num === 0">The number is zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>  
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>Not a number</h2>
  <h2 :style="vShowStyle" v-show="showElement">V-show</h2>
  <template v-if="display">
    <h2>Comida</h2>
    <h2>Cachichurris</h2>
    <h2>Perris</h2>
  </template>
  -->
  <h2 v-for="(name, index) in names" :key="name">{{index + 1}} {{name}}</h2>
  
  <h2 v-for="name in fullnames" :key="name.first">{{name.first}} {{name.last}}</h2>
  
  <div v-for="actor in actores" :key="actor.name">
    <h2>{{actor.name}}</h2> 
        <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
  
  </div>
  
  <h2 v-for="nombre in nombres" :key="nombre">{{nombre}}</h2>

  <h2 v-for="(Element, key, index) in myInfo" :key="Element">{{index}} {{key}} {{Element}}</h2>

  <template v-for="vendetta in nombres" :key="vendetta">
  <hr />
  <h2>{{vendetta}}</h2>
  <hr />
  
  </template>

  <template v-for="nombre in nombres" :key="nombre">
    <h2 v-if="nombre === 'pollo'">{{nombre}} yoyoyo</h2>
  </template>



</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      nombres: ['pedro', 'pablo', 'pollo'],
        actores:[
            {name: 'Aurelio Cheveroni',
            movies: ['el desquisiado carlan', 'Ya mataron a Krilin']},
            {name: 'Ken Brockman',
            movies: ['Tal vez me recuerden en peliculas como...', 'Y acabate tu sandia muchacho estupido']}
        ],

       names: ['cachichurris', 'churris', 'chichurris'],
        fullnames: [
          {first: 'Davy', last: 'Jem'},
          {first: 'Teodoro', last: 'Montorico'},
          {first: 'Capirulis', last: 'Pirulis'},
          
        ],
        //uno tambien puede itarar sobre propiedades {} y no solo en listas []

        myInfo: {
          name: 'Cachichurris',
          age: 21,
          favouriteColor: 'Yellow'

        }


      /*num: 5,
      display: true,
      showElement: false,
      vShowStyle: {
        padding: '200px',
        backgroundColor: 'magenta'
      } */
     
    } 
    
  }  

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
