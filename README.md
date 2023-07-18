# robot_move
php

<!DOCTYPE html>

<html>
	
<head>
	
	<title>Robot Control</title>
 
	<style>
 
		#map {
  
			width: 500px;
   
			height: 500px;
   
			background-color: #eee;
   
			position: relative;
   
		}
  
		#robot {
  
			width: 50px;
   
			height: 50px;
   
			background-color: blue;
   
			position: absolute;
   
			top: 50%;
   
			left: 50%;
   
			transform: translate(-50%, -50%);
   
		}
  
	</style>
 
</head>

<body>
	
	<h1>Robot Control</h1>
 
	<div id="map">
 
		<div id="robot"></div>
  
	</div>
 
	<form method="post">
 
		<button type="submit" name="forward">Forward</button>
  
		<button type="submit" name="backward">Backward</button>
  
		<button type="submit" name="right">Right</button>
  
		<button type="submit" name="left">Left</button>
  
	</form>
 

	<?php
 
	// Check if a button was clicked
 
	if (isset($_POST['forward'])) {
 
		// Code to move the robot forward
  
		echo '<script>document.getElementById("robot").style.top = (parseFloat(document.getElementById("robot").style.top) - 50) + "px";</script>';
  
	} elseif (isset($_POST['backward'])) {
 
		// Code to move the robot backward
  
		echo '<script>document.getElementById("robot").style.top = (parseFloat(document.getElementById("robot").style.top) + 50) + "px";</script>';
  
	} elseif (isset($_POST['right'])) {
 
		// Code to turn the robot right
  
		echo '<script>document.getElementById("robot").style.transform = "rotate(90deg)";</script>';
  
	} elseif (isset($_POST['left'])) {
 
		// Code to turn the robot left
  
		echo '<script>document.getElementById("robot").style.transform = "rotate(-90deg)";</script>';
  
	}
 
	?>
 
</body>

</html>

#code explain
This code creates a map and creates four buttons (forward, backward, right, left) but it is not linked to mysql

and there is a problem that some buttons may not work

