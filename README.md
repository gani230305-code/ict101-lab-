<!DOCTYPE html>
<html>
<head>
    <title>ICT 101 - Lab Activity 3</title>
</head>
<body>

<h1>ICT 101 – Lab Activity 3</h1>

<h2>Task 1: JavaScript Array</h2>
<p id="arrayOutput"></p>

<h2>Task 2: Grade Calculator</h2>
Enter Marks:
<input type="number" id="marks">
<button onclick="calculateGrade()">Calculate Grade</button>
<p id="gradeResult"></p>

<h2>Task 3: User Information Form</h2>
Name: <input type="text" id="name"><br><br>
Email: <input type="email" id="email"><br><br>
Age: <input type="number" id="age"><br><br>
<button onclick="validateForm()">Submit</button>

<p id="formMessage"></p>

<script>
var subjects = ["ICT", "Maths", "English", "Science"];
document.getElementById("arrayOutput").innerHTML =
    "Subjects are: " + subjects.join(", ");

function calculateGrade() {
    var marks = document.getElementById("marks").value;
    var grade;
    if (marks >= 90) grade = "A";
    else if (marks >= 80) grade = "B";
    else if (marks >= 70) grade = "C";
    else if (marks >= 60) grade = "D";
    else grade = "F";
    document.getElementById("gradeResult").innerHTML =
        "Your Grade is: " + grade;
}

function validateForm() {
    var name = document.getElementById("name").value;
    var email = document.getElementById("email").value;
    var age = document.getElementById("age").value;

    if (name === "" || email === "" || age === "") {
        document.getElementById("formMessage").innerHTML =
            "All fields are required!";
    } else if (age < 18) {
        document.getElementById("formMessage").innerHTML =
            "Age must be over 18!";
    } else {
        document.getElementById("formMessage").innerHTML =
            "Form submitted successfully!";
    }
}
</script>

</body>
</html>
