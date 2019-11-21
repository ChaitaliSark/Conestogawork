<html>
<head>
<title> Assignment 4 </title>
<style> body {
background-image:url(sirpi-floral-leaf-pattern-wallpaper-metallic-glitter-heavy-weight-20590-p3723-9033_medium.jpg)
}
</style>
<script src='vali.js'></script>
</head>
<h1 style="font-family: Times New Roman;"><b>Enter Information: </b></h1>
<br> 
<header>
<form name="myForm" action="insert.php" method="post" onsubmit="return xyz()" >
<table>

<tr><td>Seller Name:</td>
<td><input type="text" placeholder="Seller Name" name="SellerName" id= "SellerName"/> </td> </tr>

<tr><td>Address:</td>
<td><input type="text" placeholder="Address" name="Addr" id= "Addr"/> </td></tr>

<tr><td>City:</td>
<td><input type="text" placeholder="City" name="City" id= "City"/> </td></tr>

<tr><td>Phone Number:</td>
<td><input type="tel" pattern="^[(]{0,1}[0-9]{3,3}[)/-]{0,1}[0-9]{3,3}[-]{1,1}[0-9]{4,4}$" placeholder="123-456-7891" name="Phone" id= "Phone"/> </td></tr>

<tr><td>Email Address:</td>
<td><input type="email" pattern="[a-zA-Z0-9.-_]{1,}@[a-zA-Z.-]{2,}[.]{1}[a-zA-Z]{2,}" placeholder="Email Address" name="Email" id= "Email"/> </td></tr>

<tr><td>Vehicle Make:</td>
<td><input type="text" placeholder="Vehical Make" name="Make" id= "Make"/> </td></tr>

<tr><td>Vehicle Model:</td>
<td><input type="text" placeholder="Vehical Model" name="Model" id= "Model"/> </td></tr>

<tr><td>Vehicle Year:</td>
<td><input type="text" placeholder="Vehical Year" name="Year" id= "Year"/> </td></tr>

<tr><td> </td>
<td> <input type="Submit" value="Submit"> <a href="Page1.html"><button> Home</button> </a> </td></tr>

</table>
</form>
</header>
</html>
