<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Calculater</title>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link
		href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&family=Merriweather+Sans:ital,wght@0,300..800;1,300..800&family=Merriweather:ital,opsz,wght@0,18..144,300..900;1,18..144,300..900&family=Open+Sans:ital,wght@0,300..800;1,300..800&display=swap"
		rel="stylesheet">
	<link rel="stylesheet" href="style.css">
</head>
<body>
	<div class="BOX">
		<div class="calculater">
			<div class="calculater-header" id="display"> </div>
			<div class="calculater-main">
				<button onclick="cl()" id="clearbtn" class="btn">C</button>
				<button onclick="delet()" id="delbtn" class="btn">DEL</button>
				<button onclick="cal('%')" id="modulbtn" class="btn">%</button>
				<button onclick="cal('/')">/</button>
				<button onclick="cal(9)">9</button>
				<button onclick="cal(8)">8</button>
				<button onclick="cal(7)">7</button>
				<button onclick="cal('*')" id="symbol">*</button>
				<button onclick="cal(6)">6</button>
				<button onclick="cal(5)">5</button>
				<button onclick="cal(4)">4</button>
				<button onclick="cal('-')" id="symbol">-</button>
				<button onclick="cal(3)">3</button>
				<button onclick="cal(2)">2</button>
				<button onclick="cal(1)">1</button>
				<button onclick="cal('+')" id="symbol">+</button>
				<button onclick="cal(0)" style="border-radius:50px;width: 100px; height: 45px;">0</button>
				<button onclick="cal('.')" id="symbol">.</button>
				<button onclick="show()" id="symbol" style="width: 65px;border-radius:30px;" class="show">=</button>
			</div>
		</div>
	</div>
	<script>
		let arr = [];
		function cal(a) {
			arr.push(a);
			let str = arr.join("");
			let value = document.getElementById('display');
			value.innerText = str;
		}
		function show() {
			let str = arr.join("")
			console.log(str);
			let value = eval(str);
			let result = document.getElementById('display');
			result.innerText = value;
			if (value === undefined) {
				let result = document.getElementById('display');
				result.innerText = "0";
			}
		}
		function delet() {
			console.log(arr);
			arr.pop();
			let str = arr.join("");
			let result = document.getElementById('display');
			result.innerText = str;
		}
		function cl() {
			arr.splice(0, arr.length);
			let result = document.getElementById('display');
			result.innerText = "";
		}
	</script>
</body>

</html>
