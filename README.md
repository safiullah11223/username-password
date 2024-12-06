1.	<!DOCTYPE html>  
2.	<head>  
3.	<title> Using fucntions   
4.	</title>  
5.	</head>  
6.	<?php  
7.	$Number_no_1 = $_POST['Number_no_1ber'];  
8.	$Number_no_2 = $_POST['Number_no_2ber'];  
9.	$Result = $_POST['Result'];  
10.	function MyCalculator($Number1,$Number2, $Result)   
11.	// set $Result as parameter  
12.	{  
13.	switch($Result)  
14.	{  
15.	case "Addition":   
16.	// here you have to use colons not semi-colons  
17.	$compute = $Number1 + $Number2;   
18.	break;  
19.	case "Subtraction":  
20.	$compute = $Number1 - $Number2;   
21.	break;  
22.	case "Multiplication":  
23.	$compute = $Number1 * $Number2;   
24.	break;  
25.	case "Division":  
26.	$compute = $Number1 / $Number2;   
27.	break;  
28.	}  
29.	return $compute; // returning variable  
30.	}  
31.	echo "$Result <br /> <br /> 1st Number: $Number_no_1 <br /> 2nd Number: $Number_no_2 <br /><br />";  
32.	echo "Answer is:" .MyCalculator($Number_no_1,$Number_no_2, $Result);  
33.	// you need to pass $Result as argument of that function  
34.	?>  
35.	<body>  
36.	<div id="page-wrap">  
37.	<h1>Calculator by Nirnay</h1>  
38.	<form action="" method="post" id="quiz-form">  
39.	<p>  
40.	<input type="number" name="Number_no_1" id="Number_no_1" required="required" value="<?php echo $Number_no_1; ?>" /> <b>First Number</b>  
41.	</p>  
42.	<p>  
43.	<input type="number" name="Number_no_2" id="Number_no_2" required="required" value="<?php echo $Number_no_2; ?>" /> <b>Second Number</b>  
44.	</p>  
45.	<p>  
46.	<input readonly="readonly" name="CalculatorResult" value="<?php echo $CalculatorResult; ?>"> <b>CalculatorResult</b>  
47.	</p>  
48.	<input type="submit" name="operator_specified" value="Sum" />  
49.	<input type="submit" name="operator_specified" value="Subtraction" />  
50.	<input type="submit" name="operator_specified" value="Multiplication" />  
51.	<input type="submit" name="operator_specified" value="Division" />  
52.	</form>  
53.	</div>  
54.	</body>  
55.	</html>  





