<body>
    <h1>> Word nu lid</h1>
<form>
    <fieldset>
      <legend>Persoonlijke Gegevens</legend>
      <label for="Geslacht">Geslacht</label>
      <input id="Geslacht" required type="text">
  
      <label for="Voormaan">Voornaam</label>
      <input id="Voornaam" required type="text">
      <p class="feedback">👍</p>

      <label for="Tussenvoegsel">Tussenvoegsel</label>
      <input id="Tussenvoegsel" required type="text">
      <p class="feedback">👍</p>

      <label for="Achternaam">Achternaam</label>
      <input id="Achternaam" required type="text">
      <p class="feedback">👍</p>

      <label for="Geboortedatum">Geboortedatum</label>
      <input id="Geboortedatum" required type="text">
      <p class="feedback">👍</p>
     </fieldset>
  
     <fieldset>
        <legend>Contact Gegevens</legend>
        <label for="Adres">Adres (straat en huisnummer)</label>
        <input id="Adres" required type="text">
    
        <label for="Postcode">Postcode (formaat: 1000 AA)</label>
        <input id="Postcode" required type="text">
        <p class="feedback">👍</p>
  
        <label for="Woonplaats">Woonplaats</label>
        <input id="Woonplaats" required type="text">
        <p class="feedback">👍</p>
  
        <label for="Emailadres">E-mailadres</label>
        <input id="Emailadres" required type="text">
        <p class="feedback">👍</p>

        <label for="Emailadres">Bevestiging E-mailadres</label>
        <input id="Emailadres" required type="text">
        <p class="feedback">👍</p>
  
        <label for="Telefoon">Telefoon </label>
        <input id="Telefoon" required type="text">
        <p class="feedback">👍</p>
  
       </fieldset>

       <fieldset>
        <legend>Automatische incasso</legend>
        <label for="IBAN">IBAN (voorbeeld: NL11 INGB 1234 5678 90)</label>
        <input id="IBAN" required type="text">
    
        <label for="Benaming">Op naam van</label>
        <input id="Benaming" required type="text">
        <p class="feedback">👍</p>
  
       </fieldset>


    <fieldset>
      <legend>Online</legend>
      <label for="url">Website url</label>
      <input id="url" type="url" placeholder required>
      <p class="tooltip">http://</p>
  
      <label for="mail" >E-mail</label>
      <input id="mail" type="email" required>  
      <p class="feedback">👍</p>
    </fieldset>

    <a href="/" target="_blank">WORD LID</a>
  </form>
</body>


  <style>

* {
  box-sizing:border-box;
}
:root {
    --oba-light-blue: #E3E9F9;
    --oba-red: #FF0000;
}
html {
  font:100% / 250% "Monaco";
  padding:0;
  margin:0;
}
body {
  font-size: 1em;
  padding:2em;
  margin:0;
  background-color: var(--oba-light-blue);
}

@media only screen and (max-width: 600px) {
  body {
    padding: 0;
  }
}

form {
  display:flex;
  flex-direction:column;
  transition: all .2s;
  padding:1em;
  max-width:30rem;
  margin:0 auto;
  overflow:hidden;
  /* height:100vh */
}
form:invalid {
  background: var(--oba-light-blue);
}
fieldset {
  display:flex;
  flex-direction:column;
  justify-content:center;
  margin-bottom: 1em;
  border:none;
  transition: all .2s;
  padding:1em 1em 0;
  position: relative;
}
fieldset + fieldset {
  opacity:0;
  transition:.25s .25s;
  transform:translateX(-120%)
}
fieldset:valid + fieldset {
  opacity:1;
  transform:translateX(0)
}
fieldset:valid p {
  display:block;
  color: White;
  background:seaGreen;
}
/* fieldset:invalid {
  background: rgba(255, 224, 13, .2);
}  */
fieldset:invalid p{
  display:none;
}
legend {
  font-weight:bold;
  transform: translateY(1.5rem);
  font-size: 1.5em;
  margin-bottom: 2rem;
  position: relative;
  z-index:5;
  color: var(--oba-red)
}

label {
    font-weight: bolder;
}
input {
  border-color:#000;
  padding:.25em;
  font-size: 1.25em;
  margin-bottom: 1em;
  width:100%;
  transition:all .1   s;
  z-index:2;
  border-radius: 0.5em;
}
input:valid {
  border-color:seaGreen;
  background-color: rgb(232, 245, 233);
} 
input:invalid {
  border-color: var(--oba-ligh);
  /* background: rgba(255, 224, 13, .2); */
}
input:focus {
  transform: scale(1.01, 1.01);
  outline:none;
  box-shadow:0 0 0 3px rgba(0,0,0,.25)
}
input:focus + p.tooltip {
  display:block;
  opacity:1;
  margin-top:-1.3em;
}
input:disabled {
  border-color:#eee;
  background-color: #f9f9f9;
}
input::placeholder {
  color:rgba(0,0,0,.25);
  font-style:italic;
}
button {
  font-size: 1.25em;
  flex:0 0 2em;
  transition:all .2s .2s;
  opacity:0;
  width:6em;
  border-radius:.5rem;
  background-color:seaGreen;
  color:white;
  outline:none;
  border:none;
  box-shadow:0 0 5px rgba(0,0,0,0.2)
}
form:valid button {
  opacity:1
}
button:focus {
  transform: scale(1.1, 1.1);
}
.tooltip { 
  z-index:1;
  color:DodgerBlue;
  padding:.25em;
  background:AliceBlue;
  border: 1px solid currentColor;
  font-style:italic;
  transition:all .2s;
  margin-top:-3em;
  opacity:0;
  padding:.25rem;
}
.feedback {
  position: absolute;
  top: -2em;
  right: 1em;
  width: 2rem;
  height: 2rem;
  text-align: center;
  line-height: 2rem;
  border-radius: 50%;
  transform:translateY(-3rem);
  z-index:10;
  transition:.25s;
}
fieldset:valid .feedback {
  transform:translateY(0)
}

a:link, a:visited {
  background-color: #f44336;
  border-radius: 0.5em;
  color: white;
  padding: 14px 25px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
}

a:hover, a:active {
  background-color: red;
}
  </style>