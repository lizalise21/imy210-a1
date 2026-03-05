<script setup>

const { data: dogImage, refresh, pending, error } = await useFetch(
  'https://dog.ceo/api/breeds/image/random', 
)


const refreshDog = () => {
  refresh()
} 

</script>

<template>
    <div>
        <h1>My Projects</h1>
        <div class="project">
            <h2>Database Management System</h2>
            <p>Developed a MariaDB-based system for managing accessories inventory.</p>
        </div>

        <div class="project">
            <h2>HTML & CSS Website</h2>
            <p>Designed and styled a responsive website on booking flights.</p>
        </div>

        <div class="project">
            <h2>An ASP.NET MVC Website</h2>
            <p>Created a Website about dog shelter using ASP.NET MVC.</p>

            <!--Dog Facts section-->
            <div class="project">
                <h3>Random Dog  API</h3>

              
            <p v-if="pending">Loading dog image...</p>

            <div v-else-if="dogImage">
                <img :src="dogImage.message" alt="Random Dog" class="dog-img"/>
            </div>

            <p v-else-if="error">
                 Failed to load dog fact.
            </p>
                <button @click="refreshDog">Get Another Dog</button>

            </div>
        </div>

    </div>
</template>

<style scoped>

h1 {
    text-align: center;
}
.container {
  padding: 40px;
}

.project {
  margin-bottom: 30px;
  text-align: center;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
}

.dog-img {
    width: 250px;
    border-radius: 5px;
    margin-top: 10px;
}
button {
  margin-top: 10px;
  padding: 8px 12px;
  cursor: pointer;
}

</style>