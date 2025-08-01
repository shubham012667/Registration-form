
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
    <style>
        .form-group {
            margin-bottom: 1rem;
        }
        .error {
            color: red;
        }
    </style>
</head>
<body>
    <h2>Student Registration Form</h2>
    <form action="/submit" method="post">
        <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            <span class="error" aria-live="polite"></span>
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <span class="error" aria-live="polite"></span>
        </div>
        <div class="form-group">
            <label for="age">Age:</label>
            <input type="number" id="age" name="age" min="18" max="100" required>
            <span class="error" aria-live="polite"></span>
        </div>
        <button type="submit">Submit</button>
    </form>
    <script>
        const form = document.querySelector('form');
        const nameInput = document.getElementById('name');
        const emailInput = document.getElementById('email');
        const ageInput = document.getElementById('age');
        form.addEventListener('submit', function(event) {
            let isValid = true;
            if (!nameInput.validity.valid) {
                nameInput.nextElementSibling.textContent = 'Please enter a valid name.';
                isValid = false;
            } else {
                nameInput.nextElementSibling.textContent = '';
            }
            if (!emailInput.validity.valid) {
                emailInput.nextElementSibling.textContent = 'Please enter a valid email address.';
                isValid = false;
            } else {
                emailInput.nextElementSibling.textContent = '';
            }
            if (!ageInput.validity.valid) {
                ageInput.nextElementSibling.textContent = 'Please enter a valid age between 18 and 100.';
                isValid = false;
            } else {
                ageInput.nextElementSibling.textContent = '';
            }
            if (!isValid) {
                event.preventDefault(); // Prevent form submission if validation fails
            }
        });
    </script>
</body>
</html>
