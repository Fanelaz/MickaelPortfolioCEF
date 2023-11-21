<template>
  <div class="container">
    <h2>Contactez-nous</h2>
    <form ref="form" @submit.prevent="sendEmail" >
      <label>Prénom :</label>
      <input type="text" name="user_name" required>
      <label>Email :</label>
      <input type="email" name="user_email" required>
      <label>Message :</label>
      <textarea name="message" required></textarea>
      <input type="submit" value="Envoyer !" class="btn">
      <p v-if="successMessage" class="success-message">{{ successMessage }}</p>
      <p v-if="errorMessage" class="error-message">{{ errorMessage }}</p>
    </form>

    
  </div>
  
<div class="coor">
    <h3>Coordonées</h3>
    <a href="tel:0633264292"><p>Téléphone : 06-33-26-42-92</p></a>
    <a href="mailto:lbtr@mickaelportfolio.fr" target="_blank"><p>Mail : lbtr@mickaelportfolio.fr</p></a>
  </div>
</template>

<script>

import emailjs from 'emailjs-com' 

export default {
  data() {
    return {
      formData: {
        name: '',
        firstname: '',
        message: ''
      },
      successMessage: '',
      errorMessage: ''
    };
  },
  methods: {

    sendEmail() {
        emailjs.sendForm('service_cdh1sc9', 'template_rd1kfdm', this.$refs.form, 'JHV4AjyBC3hAWQcKN')
          .then((result) => {
            this.successMessage = "Formulaire envoyé avec succès !";
            this.$refs.form.reset();
              console.log('SUCCESS!', result.text);
          }, (error) => {
            this.errorMessage = "";

              console.log('FAILED...', error.text);
          });
      }

  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Cabin&family=Roboto+Condensed:wght@100&family=Roboto:ital,wght@0,100;1,100&display=swap');


body {
  width: auto;
  height: 1080px;
}

a {
  text-decoration: none;
  color: black;
}

.btn {
  background-color: #8AAEE0;

  font-family: Cabin;
  font-size: x-large;
}

.btn:hover {
  background-color: #B1C9EF;

  color: #fff;
  transition: 0.5s;
}

.coor {
  width: 100%;
  display: block;
  text-align: center;
  font-family: Cabin;
}

.coor > h3 {
  text-decoration: underline;
  text-underline-offset: 5px;
  font-size: x-large;
}

.container {
  margin: 50px auto;
  background: #B1C9EF;
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: black;
  width: 80%;
}

h2 {
  font-size: 36px;
  font-family: Cabin;
  text-decoration: underline;
  text-underline-offset: 8px;
  padding: 20px;
}

label {
  font-family: Cabin;
  font-size: larger;
}

label {
  display: block;
  margin-bottom: 8px;
}


input,
textarea {
  width: 100%;
  padding: 8px;
  margin-bottom: 16px;
  box-sizing: border-box;
  border-radius: 10px;
}


button {
  background-color: #B1C9EF;
  color: #fff;
  padding: 10px 15px;
  border: none;
  cursor: pointer;
  border-radius: 10px;
}

button:hover {
  background-color: #8AAEE0;
}

.success-message {
  color: green;
  margin-top: 10px;
  font-family: Roboto;
  font-size: x-large;
  margin-top: 40px;
  font-weight: bold;
  text-decoration: underline;
  text-underline-offset: 5px;
}

</style>
