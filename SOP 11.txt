<html>
	<head>
		<title>PHP program to count the number of vowels, consonants and whitespaces of a given line of text</title>
	</head>
	<body>
		<form method="post">
			<table border="0"> 
				<tr> <td> <input type="text" name="input" value="enter" placeholder="Enter input"/> </td> </tr>
				<tr> <td> <input type="submit" name="submit" value="Submit"/> </td> </tr>
			</table>
		</form>
		<?php
			function vowels()
			{
			if(isset($_POST['submit']))
				{
				$str = $_POST['input'];
				$str1 = $str;
				echo "Given input :".$str1."\n";
				$vCount = 0;
				$cCount = 0;
				$str = strtolower($str);
				for($i = 0; $i < strlen($str); $i++)
					{
					if( $str[$i] == 'a' || $str[$i] == 'e' || $str[$i] == 'i' || $str[$i] == 'o' || $str[$i] == 'u')
						{
						$vCount++;
						}
					}
				echo "Number of vowels : " , $vCount."</br>";
				}
			}
			vowels();
		?>
	</body>
</html>
