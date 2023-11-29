
<body>
    <div class="card">
        <!-- <Image></Image> -->
        <h1>Welkom bij OBA!</h1>
        <h3>Log in or sign up</h3>
        <form action="/action_page.php">
          <input type="text" id="fname" name="firstname" placeholder="E-mailadres of telefoonnummer...">
          <input type="text" id="lname" name="lastname" placeholder="Wachtwoord...">
      
          <div class="buttons">
          <a href="/">Log in</a>
          <a href="/Sign-up">Sign up</a>
        </div>
        </form>
      </div>
    </body>
    
      <style>
        body {
            background-color: #E3E9F9;
        }

        a {
            text-decoration: none;
            width: 20%;
            background-color: red;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        .buttons {
          margin-top: 1em;
        }

      
    input[type=text] {
      text-align: center;
      width: 100%;
      padding: 20px 20px;
      margin: 8px 0;
      display: inline-block;
      border: none;
      border-radius: 4px;
      box-sizing: border-box;
      background-color: #F5F5F5;
    }
    
    /* a {
      width: 50em;
      background-color: red;
      color: white;
      padding: 12px 20px;
      margin: 8px 0;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    } */
    
  a:hover {
    color: black;
      background-color: white;
      border: solid 2px red;
    }
    
    .card {
      text-align: center;
      border-radius: 10px;
      background-color: white;
      padding: 80px;
      width: 40em;
      height: 20em;
      margin: auto;
      margin-top: 10em;
    }
      </style>