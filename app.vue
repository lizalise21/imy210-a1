<template>
  <div>
    <nav>
      <NuxtLink to="/">Home</NuxtLink> ||
      <NuxtLink to="/projects">Projects</NuxtLink> ||
      <NuxtLink to="/contact">Contact</NuxtLink>
    </nav>

    <NuxtPage />
  </div>
</template>

<style>
nav {
  background-color: black;
  padding: 15px;
  text-align: center;
}

nav a {
  color: white;
  text-decoration: none;
  margin: 0 15px;
  font-weight: bold;
}

nav a:hover {
  text-decoration: underline;
}
</style>