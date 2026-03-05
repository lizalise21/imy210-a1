<script setup>
const { data: weather, refresh } = await useFetch(
'https://wttr.in/Johannesburg?format=j1'

)


const refreshWeather = () => {
  refresh()
}
</script>

<template>
    <div class="container">
    <h1> Lizalise Mbonisweni </h1>
    <img src="/profile.jpeg" alt="My Photo" class="profile-image"/>

    <h2>Hi there, welcome to my portfolio!</h2>

    <p>My name is Lizalise Mbonisweni. I am a second year Bsc(IT) Information and Knowledge Systems student. 
    I enjoy web development and building modern applications. I have learnt C++, C# and ASP.NET MVC. 
    This portfolio showcases some of my academic projects.
    </p>
</div>
 <div class="weather-section">
  <h4>Current Weather in Johannesburg</h4>

  <div v-if="weather">
  <p>
    Temperature: {{ weather.current_condition[0].temp_C }}°C
  </p>

  <p>
    Condition: {{ weather.current_condition[0].weatherDesc[0].value }}
  </p>
  </div>

 <p v-else> Loading weather </p>
  <button @click="refreshWeather">Refresh Weather</button>
</div>

</template>

<style scoped>
.container {
    text-align: center;
    padding: 40px;
}

.profile-image {
    width: 200px;
    border-radius: 50%;
    margin: 20px 0;
}

.weather-section{

  margin-top:10px;
  padding:10px;
  border:1px solid #ddd;
  border-radius:8px;
}

button{
  margin-top:5px;
  padding:5px 10px;
  cursor:pointer;
}

</style>