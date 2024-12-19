<?php
session_start();
include('dbdata.php');

$email = $conn->real_escape_string($_POST['email']);
$password1 = $conn->real_escape_string($_POST['password1']);
$password2 = $conn->real_escape_string($_POST['password2']);
$firstname = $conn->real_escape_string($_POST['fName']);
$lastname = $conn->real_escape_string($_POST['lName']);
$dateofbirth = $conn->real_escape_string($_POST['dob']);
$mobilenum = $conn->real_escape_string($_POST['mNum']);
$parentsnum = $conn->real_escape_string($_POST['pNum']);
$gender = $conn->real_escape_string($_POST['gender']);
$school = $conn->real_escape_string($_POST['school']);


$sql = "SELECT email FROM user WHERE email='$email'";
$result = $conn->query($sql);



if ($result->num_rows > 0) {
    $_SESSION['status'] = "Account with this email already exists";
    $_SESSION['status_type'] = "";
    header("Location: ../index.php");
} else {
 if ($password1 == $password2) {
    $sql = "INSERT INTO `user`( `email`, `password`, `first Name`, `last name`, `date of brith`, `mobile number`, `parents number`, `gender`, `school`) VALUES ('$email','$password1','$firstname','$lastname','$dateofbirth','$mobilenum','$parentsnum','$gender','$school')";

    if ($conn->query($sql) === TRUE) {
        $_SESSION['status'] = "New account created successfully";
        $_SESSION['status_type'] = "success";
        $_SESSION['user'] = $email;
        header("Location: ../home.php");
    } else {
        echo "$sql" . "$conn->error";
        echo "$spl" . "$conn->error";
    }
 } else {
    $_SESSION['status'] = "Password Doesn't Match";
    $_SESSION['status_type'] = "";
    header("Location: ../register.php");
 }
}
?>