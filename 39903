<?php
if ($_SERVER['REQUEST_METHOD'] == 'POST') {
    // Configuration
    $to = "andryandriamanohisoa@gmail.com"; // Votre adresse e-mail
    $subject = "New Contact Form Submission";
    $name = htmlspecialchars($_POST['name']);
    $email = htmlspecialchars($_POST['email']);
    $message = htmlspecialchars($_POST['message']);

    // Vérifie les champs
    if (empty($name) || empty($email) || empty($message)) {
        echo "All fields are required.";
        exit;
    }

    // Crée le contenu de l'e-mail
    $email_body = "Name: $name\n";
    $email_body .= "Email: $email\n";
    $email_body .= "Message: $message\n";

    // Envoie l'e-mail
    if (mail($to, $subject, $email_body)) {
        echo "Message sent successfully!";
    } else {
        echo "Failed to send the message.";
    }
} else {
    echo "Invalid request.";
}
?>

