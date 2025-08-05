<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Student Registration Form</title>
    <style>
        .form-group {
            margin-bottom: 1rem;
        }
        .error {
            color: red;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>
    <h2>Student Registration Form</h2>
    <form>
        <div class="form-group">
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" required>
        </div>
        <div class="form-group">
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email" required>
        </div>
        <div class="form-group">
            <label for="age">Age:</label><br>
            <input type="number" id="age" name="age" min="18" max="100" required>
        </div>
        <button type="submit">Submit</button>
    </form>
</body>
</html>
