# code

<!DOCTYPE html>

<html>
	
<head>
	
	<title>Draw Square with Buttons</title>
 
	<script> 
 
		var canvas, ctx;
  
		var x = 50, y = 50;
  
		var size = 50;

		function init() {
  
			canvas = document.getElementById("myCanvas");
   
			ctx = canvas.getContext("2d");

			drawSquare();
		}

		function drawSquare() {
  
			ctx.clearRect(0, 0, canvas.width, canvas.height);
   
			ctx.beginPath();
   
			ctx.lineWidth = 5; // Set line width to 5 pixels
   
			ctx.rect(x, y, size, size);
   
			ctx.stroke();
		}

		function moveSquare(direction) {
  
			switch(direction) {
   
				case "up":
    
					y -= 10;
     
					break;
     
				case "down":
    
					y += 10;
     
					break;
     
				case "left":
    
					x -= 10;
     
					break;
     
				case "right":
    
					x += 10;
     
					break;
			}

			drawSquare();
		}
  
	</script>
 
</head>

<body onload="init()">
	
	<canvas id="myCanvas" width="300" height="300"></canvas>
 
	<br>
 
	<button onclick="moveSquare('up')">Up</button>
 
	<button onclick="moveSquare('down')">Down</button>
 
	<button onclick="moveSquare('left')">Left</button>
 
	<button onclick="moveSquare('right')">Right</button>
 
</body>

</html>
