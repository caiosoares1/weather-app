<script setup>
import CityCard from '../components/CityCard.vue'
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <nav>
    <h1>Weather App</h1>
  </nav>
  <div id="welcome">
    <h2> Procure por uma cidade para ver a previsão do tempo!</h2>

  </div>
  <div class="search">
    <div class="search-city">

      <input type="text" placeholder="Digite aqui...">
      <button> Adicionar Cidade</button>
    </div>

    <div class="filter">
      <h3>Filtros</h3>
      <input type="text" id="country" name="country">
      <select name="heat-level" id="heat-level">
        <option value="frio">Mais Frio</option>
        <option value="quente">Mais Quente</option>
      </select>
      <select name="temperature" id="temperature-measurement">
        <option value="celsius">Celsius</option>
        <option value="fahrenheit">Fahrenheit</option>
      </select>

    </div>
  </div>

  <div id="cards">
    <!-- cards derivados de componente -->
    <CityCard cityName="São Paulo" temperature="25" />
  </div>
</template>

<style scoped>


h1 {
  font-family: 'Poppins', sans-serif;
  font-weight: 500;
  font-size: 2.6rem;

}

h2 {
  font-size: 1.6rem;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
  color: aliceblue;
}

h3 {
  font-size: 1.2rem;
  margin: 0 10px;
}

.search {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  justify-content: space-between;
  margin-top: 50px;
  padding: 0 50px;
}

.search-city {
  padding: 0 50px;
  background-color: #24343D;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
}

button {
  background-color: #1B262C;
  color: #fff;
  border: none;
  padding: 1rem;
  border-radius: 10px;
  margin-left: 10px;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
}

select {
  background-color: #1B262C;
  border-radius: 10px;
  color: #fff;
  width: auto;
  padding: 1rem;
  margin: 0 10px;
  appearance: none;
  border: none;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
}

.filter {
  padding: 0 50px;
  background-color: #24343D;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  border-radius: 10px;
}

.filter input {
  background-color: #1B262C;
  border-radius: 10px;
}

nav {
  display: flex;
  background: linear-gradient(#24343D, #1B262C);
  color: #fff;
  padding: 20px;
  text-align: center;
  justify-content: center;
  align-items: center;
}

#welcome {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 50px;
}

input {
  background-color: #24343D;
  width: auto;
  padding: 1rem;
  margin: 0.5rem;
  border: none;
  border-radius: 5px;
  font-family: 'Poppins', sans-serif;
  font-weight: 400;
}

#cards {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  margin-top: 50px;
}
</style>
