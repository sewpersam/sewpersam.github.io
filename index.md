<DOCTYPE!>
  <html>
    <head>
    </head>
      <style>
	#banner {
	  position: fixed;
	  object-fit: cover;
	  width: 100%;
	  background-size: cover;
	  margin: 0!important;
	  height: 25vw;
	  -webkit-mask-image:-webkit-gradient(linear, left top, left bottom, from(rgba(0,0,0,1)), to(rgba(0,0,0,0)));
      mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
	}
	
	#logo {
	  position: fixed;
	  left: 50%;
	  margin-left: -160px;  
	  width: 25%  
	}

	#buttonContainer {
	  position: relative;
	  width: 80vw;
	  height: 30vw;
	  margin: auto;
	  top: 20vw;
	}

	#quizButton {
	  float: left;
	  background-color: rgba(138, 138, 138, 0.5);
	  width: 18vw;
	  height: 26vw;
	  box-shadow: 5px 10px 20px 10px rgba(0, 0, 0, 0.5);
	  color: white;
	}

	#clueHunt {
	  float: right;
	  background-color: rgba(138, 138, 138, 0.5);
	  width: 18vw;
	  height: 26vw;
	  box-shadow: 5px 10px 20px 10px rgba(0, 0, 0, 0.5);
	}

	#joinHuntButton {
	  background-color: rgb(59, 59, 59);
	  border: none;
	  border-radius: 50px;
	  display: none;
	  width: 20%;
	  height: 15%;
	  position: absolute;
  	  top: 40%;
	  left: 89%;
	  transform: translate(-50%, -50%);
  	  -ms-transform: translate(-50%, -50%); 
	  color: white;
	  font-size: 1vw;
	  margin: auto;
	}
	/*Branch Info*/
	#branchLogo{
	  width: 100%;
	  padding-top: 12%;
	  margin: auto;
	}

	#branchQuiz {
	  background-color: rgb(59, 59, 59);
	  border: none;
	  border-radius: 50px;
	  display: none;
	  width: 20%;
	  height: 15%;
	  position: absolute;
  	  top: 40%;
	  left: 11%;
	  transform: translate(-50%, -50%);
  	  -ms-transform: translate(-50%, -50%); 
	}
	#branchQuizText {
	  color: white;
	  font-size: 1vw;
	  margin: auto;
	}
	/* Account Info CSS Below */
	#logIn {
	  margin: auto;
	  background-color: rgba(40, 110, 220, 0.5);
	  width: 24vw;
	  height: 30vw;
	  box-shadow: 5px 10px 20px 10px rgba(0, 0, 0, 0.5);
	}

	#logInHeader {
	  font-size: 1.7vw;
	  font-family: Traveling _Typewriter;
	  font-weight: bold;
	  color: white;
	  text-align: center;
	  padding: 3% 6% 6% 6%;
	  border: none;
	  background-color: Transparent;
	}

	#usernameDiv {
	  font-size: 3vw;
	  font-family: Traveling _Typewriter;
	  font-weight: bold;
	  color: white;
	  text-align: center;
	  margin-top: -0px;
	  padding: 0% 3% -50% 3%;
	}

	#userInfo {
	  display: none;
	  font-family: Traveling _Typewriter;
	  font-weight: bold;
	  color: white;
	  text-align: center;
	}

	#currentBookText {
	  font-size: 1.4vw;
	}

	#currentBook {
	  font-size: 2.4vw;
	}

	#branchText {
	  font-size: 1.4vw;
	}

	#branch {
	  font-size: 2.4vw;
	}

	#logInButton {
	  border: none;
	  width: 92%;
	  height: 6vw;
	  margin: auto;
	  display: flex;
  	  justify-content: center;
	  border-radius: 15px;
	  background-color: white;
	  font-size: 2vw;
	  width: 90%;
	  padding: 20px;
	}

	
	
	.button {
	  font-family: Times New Roman;
	  font-weight: bold;
  	  display: inline-block;
  	  border: none;
  	  text-align: center;
  	  transition: all 0.5s;
  	  cursor: pointer;
  	  margin: 5px;
	}

	.button span {
  	  cursor: pointer;
  	  display: inline-block;
  	  position: relative;
  	  transition: 0.5s;
	}

	.button span:after {
  	  content: '\00bb';
  	  position: absolute;
  	  opacity: 0;
  	  top: 0;
  	  right: -20px;
  	  transition: 0.5s;
	}

	.button:hover span {
  	  padding-right: 25px;
	}

	.button:hover span:after {
  	  opacity: 1;
  	  right: 0;
	}

	#createAccountText {
	  font-size: 1.5vw;
	  font-family: Traveling _Typewriter;
	  font-weight: bold;
	  color: white;
	  text-align: center;
	  padding: 3% 6% -5% 6%;
	}

	#createAccountButton {
	  margin: auto;
	  display: flex;
  	  justify-content: center;
	  background-color: white;
	  border-radius: 15px;
	  font-size: 2vw;
	  width: 90%;
	  padding: 20px;
	}
	/* Clue Hunt CSS Below */
	#questionMark {
	  text-align: center;
	  font-size: 26vw;
	  color: rgba(0, 0, 0, 0.822);
	  margin: auto;
	  display: block;
	}
      </style>
    <body onload="resizeObjects()" onresize="resizeObjects()" style="background-size: cover; margin: 0;" background="indexBack1.jpg">
      <img id="banner" src="techBanner2.jpg" alt="Banner Image"></img>
      <img id="logo" src="39cluesLogo2.png" alt="39 Clues Logo"></img>
      <div id="buttonContainer">
        <div id="quizButton"> 
		  <img  id="branchLogo" src="branchLogo2.png">
		  <button class="button" id="branchQuiz"><span id="branchQuizText">Find your branch here!</span></button>
	    </div>
	    <div id="clueHunt">
		  <h1 id="questionMark">?</h1>
		  <button class="button" id="joinHuntButton"><span>Join the hunt today!</span></button>
	    </div>
	    <div id="logIn">
	      <button onclick="adminInfo()" id="logInHeader">To find out which branch you belong to and start hunting the clues, you must log in.</button>
	      <div id="usernameDiv">
	      </div>
	      <div id="userInfo">
	        <p id="currentBookText">Current "Book" Clue:</p>
	    	<p id="currentBook"></p>
	    	<p id="branchText">Your Branch:</p>
	    	<p id="branch"></p>
	  	  </div>
	      <button  onclick="loggedIn()" class="button" id="logInButton">
	        <span id="logInText">Log In</span>
          </button>
		  <p id="createAccountText">Don't have an account? No problem. Create one here!</p>
	  	  <button class="button" id="createAccountButton">
	        <span style="font-size: 1vw;" id="logInText">Create Account</span>
          </button>
	    </div>
      </div>
      <script>
		  let username = "Username"
		  let currentBook = "The Black Circle"
		  let branch = "Lucian"
		  let adminAccount = true
		  //Functions
	function adminInfo(){
		if (adminAccount = true){
			window.location.assign("file:///C:/Users/Hp-Omen/Documents/Coding/39%20Clues/createAccount.html")
		}
	}
	function loggedIn(){
		document.getElementById("quizButton").style.backgroundColor = "rgba(40, 110, 220, 0.5)";
		document.getElementById("clueHunt").style.backgroundColor = "rgba(40, 110, 220, 0.5)";
		document.getElementById("logInHeader").innerHTML = "Welcome";
		var htmlTag = document.createElement("p");
		var text = document.createTextNode(username);
		htmlTag.appendChild(text);

		var element = document.getElementById("usernameDiv");
	    element.appendChild(htmlTag);
		document.getElementById("usernameDiv").style.marginTop = "-30px";
		//Hide Login Button/Info
		var x = document.getElementById("logInButton");
    	x.style.display = "none";
		var x = document.getElementById("createAccountButton");
    	x.style.display = "none";
  	    var x = document.getElementById("createAccountText");
    	x.style.display = "none";
  		//Add User Info
		var x = document.getElementById("userInfo");
    	x.style.display = "block";
		document.getElementById("currentBook").innerHTML = currentBook;
		document.getElementById("branch").innerHTML = branch;
		//Branch Quiz Content
		document.getElementById("branchLogo").src = "branchLogo1.png";
		document.getElementById("branchQuiz").style.display = "inline-block";
		//Clue Hunt Content
		document.getElementById("questionMark").style.display = "none";
		document.getElementById("joinHuntButton").style.display = "inline-block";
		//Admin Content
		if (adminAccount == true) {
			document.getElementById("logInHeader").innerHTML = "Welcome admin account";
		}



	}
	function resizeObjects() {
	  //Resizing Logo
	  var logoWidth = document.getElementById("logo");
	  var halfLogoWidth = logoWidth.offsetHeight / 1.52;
	  document.getElementById("logo").style.marginLeft = halfLogoWidth * -1;
	}

	let signedIn = localStorage.getItem("signedIn");
	if (loggedIn == true){
	  loggedIn()
	} 
	
	
      </script>
    </body>
  </html>
