<template>
  <div class="container">
    <h1>Contact Me</h1>


    <div class="contact-details">
      <h2>My Details</h2>
      <p><strong>Email:</strong> u23587874@tuks.co.za</p>
      <p><strong>Phone:</strong> 071 803 2901</p>
      <p>
        <strong>GitHub:</strong>
        <a href="https://github.com/lizalise21" target="_blank">
          github.com/lizalise21
        </a>
      </p>
    </div> 

    <form name="contact" method="POST" data-netlify="true">
      <input type="hidden" name="form-name" value="contact"/>

      <label>Name:</label>
      <input type="text" name="name" required/>

      <label>Email:</label>
      <input type="email" name="email" required />

      <label>Message:</label>
      <textarea name="message" required></textarea>

      <button type="submit">Send</button>
    </form>
  </div>
</template>

<style scoped>
.container {
  padding: 40px;
  max-width: 800px;
  margin: auto;
}

h1 {
  text-align: center;
  margin-bottom: 30px;
}

.contact-details,
.contact-form {
  margin-bottom: 40px;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
}

form {
  display: flex;
  flex-direction: column;
}

label {
  margin-top: 10px;
  font-weight: bold;
}

input,
textarea {
  margin-top: 5px;
  padding: 8px;
  border-radius: 4px;
  border: 1px solid #ccc;
}

button {
  margin-top: 15px;
  padding: 10px;
  background-color: black;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background-color: #333;
}

.success-message {
  margin-top: 15px;
  color: green;
  font-weight: bold;
}
</style>