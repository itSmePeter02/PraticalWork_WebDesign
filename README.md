<!DOCTYPE html>
<html>
<head>
<style>
body{
background: url("minion.jpg");
}
label{
display: inline-block;
width: 200px;
margin-bottom: 5px;
}
h3{
text-align:center;
}
</style>
<title>Bloom College Student Registration Form</title>
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

<div class="container bg-warning p-4 mt-5 " style="max-width:700px;border-radius: 8px">
<h3 class="text-center">BLOOM COLLEGE</h3>
<p class="text-center">Student Registration Form</p>
<hr>
<form  id="studentForm">

<label for="image">Student image:</label>
<input type="file" id="image" accept="image/*">
<small>(less than 5 Mb)</small><br>


<label for="studentName">Student Name:</label>
<input type="text" id="studentName" placeholder="Full name" onBlur = "ChangeColor(this)" onChange = "ChangetoUpperCase(this)" style = "width:400px"><br>

<label for="fatherName">Father's Name:</label>
<input type="text" id="fatherName" placeholder="Father's full name" onBlur = "ChangeColor(this)" onChange = "ChangetoUpperCase(this)" style = "width:400px"><br>

<label for="motherName">Mother's Name:</label>
<input type="text" id="motherName" placeholder="Mother's full name" onBlur = "ChangeColor(this)" onChange = "ChangetoUpperCase(this)" style = "width:400px"><br>

<label>Gender:</label>
<input type="radio" id="male"  value="Male"> Male
<input type="radio" id="female"  value="Female"> Female<br>

<label for="dob">Date of Birth:</label>
<input type="date" id="dob" style = "width:400px"><br>

<label for="email">E-mail:</label>
<input type="email" id="email" placeholder="email@example.com" onFocus = "ChangeHighlight(this)" style = "width:400px" ><br>

<label for="level">Level:</label>
<select id="level" style = "width:400px">
<option value="Bachelor">Bachelor</option>
<option value="Phd">Phd</option>
</select><br>

<label for="department">Department:</label>
<select id="department" style = "width:400px">
<option value="Computer Engineering">Computer Engineering</option>
<option value="Electrical Engineering">Electrical Engineering</option>
<option value="Mechanical Engineering">Mechanical Engineering</option>
</select><br>

<label for="mobile">Tel/Mobile:</label>
<input type="tel" id="mobile" placeholder="01x-xxx xxxx" onFocus = "ChangeHighlight(this)" style = "width:400px"><br>

<hr>
<h3>Address</h3>

<label for="state">State:</label>
<input type="text" id="state" placeholder="State" onBlur = "ChangeColor(this)" onChange = "ChangetoUpperCase(this)" style = "width:400px"><br>

<label for="city">City:</label>
<input type="text" id="city" placeholder="City" onBlur = "ChangeColor(this)" onChange = "ChangetoUpperCase(this)" style = "width:400px"><br>

<label for="postcode">Postcode:</label>
<input type="text" id="postcode" placeholder="Postcode" onBlur = "ChangeColor(this)" style = "width:400px"><br>


<div class ="text-center"><br>
<button type ="submit" class = "btn btn-success" >Register</button>
<button type = "reset" class = "btn btn-danger">Reset</button> 
<hr>

</div>
</form>


</div>
<div class = "modal fade" id ="SuccessModal" tabindex = "-1" aria-hidden = "true">
<div class = "modal-dialog modal-dialog-centered">
<div class = "modal-content">
<div class = "modal-header bg-success text-white">
<h5 class = "modal-title">Register</h5>
<button type ="button" class ="btn-close btn-close-white" data-bs-dismiss = "modal"></button>
</div>
<div class = "modal-body">
Your Details Have Been Saved
</div>
</div>
</div>
</div>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
<script>


function ChangeColor(element){
element.style.backgroundColor = "yellow";
}
function ChangetoUpperCase(element){
element.value = element.value.toUpperCase();
}
function ChangeHighlight(element){
element.style.backgroundColor = "pink";
}
function showSuccessModal(e){
e.preventDefault();
new bootstrap.Modal(document.getElementById("SuccessModal")).show();
}
document.getElementById("studentForm").addEventListener("submit",showSuccessModal);

</script>

</body>
</html>
