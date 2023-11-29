
<body>
    <div>
        <!-- <Image></Image> -->
        <h1>Welkom bij OBA!</h1>
        <h3>Log in or sign up</h3>
        <form action="/action_page.php">
          <input type="text" id="fname" name="firstname" placeholder="E-mailadres of telefoonnummer...">
          <input type="text" id="lname" name="lastname" placeholder="Wachtwoord...">
      
          <input type="submit" value="Log in">
          <input type="submit" value="Sign up">
        </form>
      </div>
    </body>
    
      <style>
        body {
            background-color: #E3E9F9;
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
    
    input[type=submit] {
      width: 20%;
      background-color: red;
      color: white;
      padding: 14px 20px;
      margin: 8px 0;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
    
    input[type=submit]:hover {
      background-color: #45a049;
    }
    
    div {
      text-align: center;
      border-radius: 10px;
      background-color: white;
      padding: 80px;
      width: 40em;
      height: 20em;
    }
      </style>