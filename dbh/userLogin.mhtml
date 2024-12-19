<?php
session_start();
include('dbdata.php');

$email = $conn->real_escape_string($_POST['email']);
$password = $conn->real_escape_string($_POST['password']);

$sql = "SELECT * FROM user WHERE email='$email'";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    $row = $result->fetch_assoc();
    $storedPassword = $row['password'];

    if ($storedPassword == $password) {
        $_SESSION['status'] = "Welcome to the D.E.C!";
        $_SESSION['status_type'] = "success";
        $_SESSION['user'] = $email;
        header("Location: ../home.php");
    } else {
        $_SESSION['status'] = "Incorrect Password";
        $_SESSION['status_type'] = "";
        header("Location: ../index.php");
    }
} else {
    $_SESSION['status'] = "Account Not Found. Create a New Account.";
    $_SESSION['status_type'] = "";
    header("Location: ../register.php");
}
?>