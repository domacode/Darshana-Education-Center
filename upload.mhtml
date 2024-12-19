<?php
if ($_SERVER['REQUEST_METHOD'] === 'POST') {
    // Check if the file is uploaded
    if (isset($_FILES['profilePhoto']) && $_FILES['profilePhoto']['error'] === 0) {
        $targetDir = "uploads/";
        $fileName = basename($_FILES["profilePhoto"]["name"]);
        $targetFilePath = $targetDir . $fileName;

        // Check file type
        $fileType = strtolower(pathinfo($targetFilePath, PATHINFO_EXTENSION));
        $allowedTypes = ["jpg", "jpeg", "png", "gif"];

        if (in_array($fileType, $allowedTypes)) {
            // Move file to the target directory
            if (move_uploaded_file($_FILES["profilePhoto"]["tmp_name"], $targetFilePath)) {
                echo "Profile photo uploaded successfully!";
                // Save the path to the database (if applicable)
                // Redirect back to the profile page or display the updated photo
            } else {
                echo "Error uploading file.";
            }
        } else {
            
            $_SESSION['status'] = "Only JPG, JPEG, PNG, and GIF files are allowed.";
            $_SESSION['status_type'] = "";
        }
    } else {
        echo "No file uploaded or there was an error.";
    }
}
?>
