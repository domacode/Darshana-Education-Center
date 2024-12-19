<?php
include 'dbdata.php'; // Include your database connection

if (isset($_GET['query']) && !empty($_GET['query'])) {
    $searchQuery = $_GET['query'];
    $query = $_GET['query'];
    $query = htmlspecialchars($query); // Sanitize the input
    $query = "%{$query}%"; // Prepare for SQL LIKE search

    // Prepare and execute the SQL statement
    $stmt = $conn->prepare("SELECT * FROM your_table WHERE column_name LIKE ?");
    $stmt->bind_param("s", $query);
    $stmt->execute();
    $result = $stmt->get_result();

    if ($result->num_rows > 0) {
        echo "<h3>Search Results:</h3><ul>";
        while ($row = $result->fetch_assoc()) {
            echo "<li><a href='item.php?id=" . $row['id'] . "'>" . $row['name'] . "</a></li>";
        }
        echo "</ul>";
    } else {
        echo "<p>No results found for '" . htmlspecialchars($_GET['query']) . "'</p>";
    }

    $stmt->close();
} else {
    echo "<p>No search query provided.</p>";
}

$conn->close();
?>




