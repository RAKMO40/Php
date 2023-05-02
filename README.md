# Php
Php important questions 
Write a PHP program using expressions and operator (ternary operator, arithmetic operatorsand comparison operators)
Ans:
<?php
$num1 = 10;
$num2 = 5;
$num3 = $num1 > $num2 ? "$num1 is greater"."<br>" : "$num2 is smaller"."<br>";
$num4 = $num1 + $num2;
$num5 = $num1 - $num2;
$num6 = $num1 / $num2;
$num7 = $num1 * $num2;
$num8 = $num1 % $num2;
$num9 = $num1 ** $num2;
$num10 = ($num1==$num2) ? "True" : "false";
$num11 = ($num1===$num2 ) ? "True" : "false";
$num12 = ($num1!=$num2) ? "True" : "false";
$num13 = ($num1!==$num2) ? "True" : "false";
$num14 = ($num1<$num2) ? "True" : "false";
$num15 = ($num1>$num2) ? "True" : "false";
$num16 = ($num1<=$num2) ? "True" : "false";
$num17 = ($num1>=$num2) ? "True" : "false";
$vars=array("$num3","$num4","$num5","$num6","$num7","$num8","$num9","$num10","$num11","$num12","$ num13","$num14","$num15","$num16","$num17",);
foreach($vars as $arr){ echo $arr."<br>";
}
?>
OR

<?php
$a = 10;
$b = 5;
$max = ($a > $b) ? $a : $b;
echo "The maximum of $a and $b is $max\n";
$x = 7;
$y = 3;
$sum = $x + $y;
$difference = $x - $y;
$product = $x * $y;
$quotient = $x / $y;
$remainder = $x % $y;
echo "The sum of $x and $y is $sum\n";
echo "The difference between $x and $y is $difference\n";
echo "The product of $x and $y is $product\n";
echo "The quotient of $x and $y is $quotient\n";
echo "The remainder when $x is divided by $y is $remainder\n";
$p = 5;
$q = 7;
$is_greater = ($p > $q);
$is_equal = ($p == $q);
$is_not_equal = ($p != $q);
echo "Is $p greater than $q? " . ($is_greater ? "Yes" : "No") . "\n";
echo "Is $p equal to $q? " . ($is_equal ? "Yes" : "No") . "\n";
echo "Is $p not equal to $q? " . ($is_not_equal ? "Yes" : "No") . "\n";
?>

Write a PHP program to the use of decision making and control structures using if statement, ifelse statement and switch case statement.
Ans:
<?php
$number = 2;
if ($number % 2 == 0) {
echo "The number is even.";
}
if ($number >= 1 && $number <= 10) { echo "The number is between 1 and 10.";
} else {
echo "The number is not between 1 and 10.";
}
switch ($number) { case 1:
echo "You entered 1."; break;
case 2:
echo "You entered 2.";
break; case 3:
echo "You entered 3."; break;
default:
echo "You did not enter a valid number."; break;
}
?>

Write a PHP program to the use of looping structure using while statement, do while statement.
Ans: 

<?php
$counter = 1;
while ($counter <= 10) { echo $counter . " ";
$counter++;
}
echo "\n";
$counter = 1; do {
echo $counter . " ";
$counter++;
} while ($counter <= 10); echo "\n";
?>

Write a PHP program to the use of looping structure using for statement, for each statement.
Ans:
<?php
for ($i = 1; $i <= 10; $i++) { echo $i . " ";
}
echo "\n";
$array = ["A","B","C","D","E","F","G","H"];
foreach ($array as $alpha) { echo $alpha . " ";
}
echo "\n";
?>

Write a PHP program for creating and manipulating indexed array, associative array and multi-dimensional array
Ans:
<?php
$array = [1, 2, 3, 4, 5];
$associative_array = ['name' => 'John Doe', 'age' => 25];
$multidimensional_array = [[1, 2, 3], [4, 5, 6]];
echo 'Indexed array'.'<br>'; foreach ($array as $number) { echo $number . ' ';
}
echo '<br>';
echo 'Associative array'.'<br>';
foreach ($associative_array as $key => $value) { echo $key . ': ' . $value . '<br>';
}
echo 'Multidimensional array'.'<br>';
foreach ($multidimensional_array as $row) { foreach ($row as $number) {
echo $number . ' ';
}
echo '<br>';
}
?>

Write a PHP program to calculate length of string , to count the no of words in string and tocompare two string using string function.
Ans: 
<?php
$string = "Hello world!";
echo "The length of the string is ".strlen($string);
$string = "This is a sentence with three words.";
echo " The number of words in the string is ".str_word_count($string);
$string1 = "Hello";
$string2 = "World";
$result = strcmp($string1, $string2); if ($result == 0) {
echo "The strings are equal.";
} else if ($result < 0) {
echo " The first string is less than the second string.";
} else {
echo " The first string is greater than the second string.";
}
?>

Write a PHP program using following string function: strrev(),strpos(),strrpos(),str_replace(),ucwords(),strtoupper(),strtolower()
Ans:
<?php
$string = "Hello world!";
echo "The reversed string is ".strrev($string)."<br>";
$string = "Hello world!";
$substring = "o";
echo "The position of the first occurrence of the substring 'o' is ".strpos($string,
$substring)."<br>";
$string = "Hello world!";
$substring = "o";
echo "The position of the last occurrence of the substring 'o' is ".strrpos($string,
$substring)."<br>";
$string = "Hello world!";
$substring = "Hello";
$replacement = "hi";
$new_string = str_replace($substring, $replacement, $string);
echo "The new string is ".str_replace($substring, $replacement, $string)."<br>";
$string = "hello world!";
echo "The new string is ".ucwords($string)."<br>";
$string = "hello world!";
echo "The new string is ".strtoupper($string)."<br>";
$string = "HELLO WORLD!";
echo "The new string is ".strtolower($string);
?>

Write a PHP program to use user define function, variable function and anonymous function.
Ans:
<?php
function multiply($x, $y) {
return $x * $y;
}
$operation = 'multiply';
$result = $operation(4, 5); // Equivalent to calling multiply(4, 5)
echo "Result of variable function: $result\n";
$sum = function($x, $y) {
return $x + $y;
};
$result = $sum(2, 3);
echo "Result of anonymous function: $result\n";
?>

Write a PHP program to create PDF document by using graphics concept.
Ans:
<?php
require_once('fpdf.php');
$pdf = new FPDF();
$pdf->AddPage();
$pdf->SetFont('Arial', 'B', 12);
$pdf->Cell(80,10,'Prof.Sonal Naik');
$pdf->Output('my_first_pdf.pdf', 'I');
?>

Write a PHP program a) to inherit member of superclass in subclass b)create constructor toinitialize object of class by using object oriented concept
Ans: 
<?php
class Animal {
 public $name;
 public $age;
 public function __construct($name, $age) {
 $this->name = $name;
 $this->age = $age;
 }
 public function speak() {
 echo "I am an animal.";
 }
}
class Dog extends Animal {
 public $color;
 public function __construct($name, $age, $color) {
 $this->color = $color;
 echo "Dog Name: $name and age $age and color is $color"."<br>";
 }
 public function bark() {
 echo "Woof!";
 }
}
$dog = new Dog('Fido', 5, 'White');
$dog->speak();
$dog->bark();
?>

Write a PHP program on introspection and serialization
Ans:
<?php
class Person { public $name; public $age;
public function     construct($name, $age) {
$this->name = $name;
$this->age = $age;
}
}
$person = new Person('John Doe', 25);
if (class_exists('Person')) {
echo "The Person class exists.<br>";
} else {
echo "The Person class does not exist.<br>";
}
$class_name = get_class($person);
echo "The class name of the object is $class_name.<br>";
$parent_class = get_parent_class($person);
echo "The parent class of the object is $parent_class.<br>";
if (is_subclass_of($person, 'Person')) {
echo "The object is a subclass of the Person class.<br>";
} else {
echo "The object is not a subclass of the Person class.<br>";
}
$array=array("Red","green","blue");
$serialized_array = serialize($array); echo $serialized_array."<br>";
$unserialized_array = unserialize($serialized_array); print_r($unserialized_array);
?>

Design a web page using following form controls: a)textbox b)radio button c)check box d)button
Ans:
<html>
<head>
<title>Form Controls</title>
</head>
<body>
<form action="<?php $_PHP_SELF?>" method="post">
<input type="text" name="textbox" placeholder="Enter your name">
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
<input type="checkbox" name="fruits[]" value="apple"> Apple
<input type="checkbox" name="fruits[]" value="banana"> Banana
<input type="checkbox" name="fruits[]" value="orange"> Orange
<button type="submit">Submit</button>
</form>
</body>
</html>
<?php
$name = $_POST['textbox'];
$gender = $_POST['gender'];
$fruits = $_POST['fruits'];
echo "Your name is $name.\n";
echo "Your gender is $gender.\n";
echo "Your favorite fruit is: "; foreach ($fruits as $fruit) {
echo "$fruit ";
}
?>

Design a web page using following form controls: a)List box b)hidden field box
Ans: 
<!DOCTYPE html>
<html>
<head>
<title>Simple Form</title>
</head>
<body>
<form action="<?php $_PHP_SELF?>" method="post">
<select name="listbox">
<option value="1">Option 1</option>
<option value="2">Option 2</option>
<option value="3">Option 3</option>
</select>
<input type="hidden" name="hidden_field" value="This is a hidden field">
<button type="submit">Submit</button>
</form>
</body>
</html>
<?php
$listbox_value = $_POST['listbox'];
$hidden_field_value = $_POST['hidden_field'];
echo "The selected option in the list box is $listbox_value.\n";
echo "The value of the hidden field is $hidden_field_value.\n";
?>

Develop a web page with data validation.
Ans:

<!DOCTYPE html>
<body>
<?php
$nerror = $merror = $perror ="";
$name = $email = $phone= "";
$pattern = "^[_a-z0-9-]+(\.[_a-z0-9-]+)* @[a-z0-9-]+(\.[a-z0-9-]+)*(\.[a-z]{2,3})$^"; if($_SERVER["REQUEST_METHOD"]=="POST") {
if(empty($_POST["name"])) {
$nerror = "Name cannot be empty!";
}
else {
$name = test_input($_POST["name"]); if(!preg_match("/^[a-zA-Z-']*$/",$name))
{
$nerror = "Only characters and white spaces allowed";
}
}
if(empty($_POST["email"])) {
$merror = "Email cannot be empty!";
}
else
{
$email = test_input($_POST["email"]); if(!preg_match($pattern, $email)) {
$merror = "Email is not valid";
}
}
if(empty($_POST["phone"])) {
$perror = "Phone no cannot be empty!";
}
else {
$phone = test_input($_POST["phone"]);
if (!preg_match ('/^[0-9]{10}$/', $phone)) {
$perror = "Phone no is not valid";
}
}}
function test_input($data)
{
$data = trim($data);
$data = stripslashes($data);
$data = htmlspecialchars($data); return $data;
}
?>
<p><span class="error">* required field </span></p>
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>"> Name: <input type="text" name="name">
<span class="error">* <?php echo $nerror;?></span><br/><br/> E-mail: <input type="text" name="email">
<span class="error">* <?php echo $merror;?></span><br/><br/> Phone no: <input type="text" name="phone">
<span class="error">* <?php echo $perror;?></span><br/><br/>
<input type="submit" name="submit" value="Submit"></form>
<?php
echo "<h2>Your Input:</h2>"; echo $name; echo "<br>"; echo $email; echo "<br>"; echo $phone; echo "<br>";
?>
</body>
</html>
Write a PHP program to create cookies, modify cookies value and delete cookies.
Ans:
<html>
<?php
$name = "name";
$value = "John Doe";
setcookie($name,$value,time()+(8600*30));//1 day
?>
<html>
<body>
<?php
if (!isset($_COOKIE["name"])){
echo "cookie name'".$name."'is not set!";
} else {
echo "Cookie name ".$name."<br>";
echo "value ".$value;
}
?>
</body>
</html>
Modify cookie
<?php
$name = "name";
$value = "xyz";
setcookie($name,$value,time()+(8600*30));//1 day
?>
<html>
<body>
<p>To modify a cookie, use the setcookie() function again. The setcookie() function will overwrite the existing cookie
with the new values.</p>
<?php
if (!isset($_COOKIE["name"])){
echo "cookie name'".$name."'is not set!";
} else {
echo "Cookie name ".$name."<br>";
echo "value ".$value;
}
?>
</body>
</html>
<html>
<?php
$name = "name";
$value = "xyz";
setcookie($name,$value,time()-(8600*30));//1 day
?>
<html>
<body>
<p>To delete a cookie, set the expiration date of the cookie to a date in the past.</p>
<?php
if (!isset($_COOKIE["name"])){
echo "cookie name'".$name."'is not set!";
} else {
echo "Cookie name ".$name."<br>";
echo "value ".$value;
}
?>
</body>
</html>


Write a PHP program to start session,get session variable and destroy session
Ans:
<?php
session_start();
$_SESSION["name"] = "John Doe";
$value = $_SESSION["name"];
echo $value;
session_destroy();
?>

Write a PHP program for sending and receiving plain text message (sending email).
Ans:
<?php
$to = "recipient@example.com";
$subject = "This is a test email";
$message = "This is the message body.";
mail($to, $subject, $message);
if (mail($to, $subject, $message)) {
echo "The email was sent successfully.";
} else {
echo "The email was not sent successfully.";
}
?>
Write a PHP program to create database and creation of table
Ans:
<?php
$servername = "localhost";
$username = "root";
$password = " ";
$conn = mysqli_connect($servername, $username, $password);
if (!$conn) {
die("Connection failed: " . mysqli_connect_error());
}
$sql = "CREATE DATABASE myDB";
if (mysqli_query($conn, $sql)) {
echo "Database created successfully";
} else {
echo "Error creating database: " . mysqli_error($conn);
}
mysqli_select_db($conn, "myDB");
$sql = "CREATE TABLE customers (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
firstname VARCHAR(30) NOT NULL, lastname VARCHAR(30) NOT NULL, email VARCHAR(50),
reg_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
)";
if (mysqli_query($conn, $sql)) {
echo "Table customers created successfully";
} else {
echo "Error creating table: " . mysqli_error($conn);
}
mysqli_close($conn);
?>

Write a PHP program to Inserting and retrieving the query result operations and Update ,Deleteoperations on table data.
Ans:
<?php
$servername = "localhost";
$username = "username";
$password = "password";
$dbname = "myDB";
$conn = mysqli_connect($servername, $username, $password, $dbname);
if (!$conn) {
die("Connection failed: " . mysqli_connect_error());
}
$sql = "INSERT INTO customers (firstname, lastname, email) VALUES ('John', 'Doe', 'john@example.com')"; if (mysqli_query($conn, $sql)) {
echo "New record created successfully";
} else {
echo "Error: " . $sql . "<br>" . mysqli_error($conn);
}
$sql = "SELECT * FROM customers";
$result = mysqli_query($conn, $sql); if (mysqli_num_rows($result) > 0) {
while($row = mysqli_fetch_assoc($result)) {
echo "id: " . $row["id"]. " - Name: " . $row["firstname"]. " " . $row["lastname"]. " - Email: " .
$row["email"]. "<br>";
}
} else {
echo "0 results";
}
$sql = "UPDATE customers SET email='johndoe@example.com' WHERE id=1"; if (mysqli_query($conn, $sql)) {
echo "Record updated successfully";
} else {
echo "Error updating record: " . mysqli_error($conn);
}
