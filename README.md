<html>
    <head>
        <title>Form title</title>
        <style>
        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            background: linear-gradient(120deg, #e3f0ff 0%, #f7e8ff 100%);
            margin: 0;
            padding: 0;
            min-height: 100vh;
        }
        .container {
            max-width: 520px;
            margin: 0 auto;
            padding: 0 16px;
        }
        header {
            color: #5e35b1;
            font-size: 2em;
            text-align: center;
            margin-top: 36px;
            font-weight: 700;
            letter-spacing: 2px;
            text-shadow: 0 2px 8px rgba(94,53,177,0.08);
        }
        form {
            background: rgba(255,255,255,0.95);
            max-width: 440px;
            margin: 56px auto;
            padding: 40px 32px;
            border-radius: 18px;
            box-shadow: 0 8px 32px rgba(94,53,177,0.12), 0 1.5px 0 #e3e8ee;
            border: 1px solid #e3e8ee;
            backdrop-filter: blur(2px);
            position: relative;
            transition: box-shadow 0.2s, transform 0.2s;
        }
        form:hover {
            box-shadow: 0 12px 36px rgba(94,53,177,0.18), 0 2px 0 #e3e8ee;
            transform: translateY(-2px) scale(1.01);
        }
        label {
            display: block;
            margin-bottom: 8px;
            color: #374151;
            font-weight: 600;
            letter-spacing: 0.3px;
            font-size: 1.07em;
        }
        input[type="text"],
        input[type="number"],
        input[type="email"],
        input[type="date"],
        input[type="tel"],
        textarea,
        select {
            width: 100%;
            padding: 14px;
            margin-bottom: 22px;
            border: 1.5px solid #cfd8dc;
            border-radius: 8px;
            font-size: 1.08em;
            box-sizing: border-box;
            background: linear-gradient(90deg, #f7fafc 0%, #e3f0ff 100%);
            transition: border-color 0.2s, box-shadow 0.2s;
            box-shadow: 0 1px 4px rgba(94,53,177,0.04);
        }
        input:focus,
        textarea:focus,
        select:focus {
            border-color: #5e35b1;
            box-shadow: 0 0 0 3px rgba(94,53,177,0.18);
            outline: none;
        }
        button,
        input[type="submit"] {
            background: linear-gradient(90deg, #5e35b1 0%, #7e57c2 100%);
            color: #fff;
            border: none;
            padding: 16px 0;
            width: 100%;
            border-radius: 8px;
            font-size: 1.12em;
            font-weight: 700;
            cursor: pointer;
            transition: background 0.2s, box-shadow 0.2s, transform 0.1s;
            box-shadow: 0 2px 12px rgba(94,53,177,0.10);
            letter-spacing: 0.5px;
        }
        button:hover,
        input[type="submit"]:hover {
            background: linear-gradient(90deg, #4527a0 0%, #5e35b1 100%);
            box-shadow: 0 6px 20px rgba(94,53,177,0.18);
            transform: translateY(-2px) scale(1.02);
        }
        textarea {
            min-height: 80px;
            resize: vertical;
        }
        hr {
            margin: 24px 0;
            border: none;
            border-top: 1.5px solid #e3e8ee;
        }
        </style>
    </head>
    <body>
        <div class="container">
            <header><h1>Form</h1></header>
            <form action="submit_form.php" method="post">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" placeholder="name" required><br>

                <label for="age">Age:</label>
                <input type="number" id="age" name="age" placeholder="age" required><br>

                <label for="birthdate">Birth date:</label>
                <input type="date" id="birthdate" name="birthdate" required><br>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required><br>

                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" placeholder="123-456-7890" required><br>

                <label for="gender">Gender:</label>
                <select id="gender" name="gender" required>
                    <option value="">Select</option>
                    <option value="male">Male</option>
                    <option value="female">Female</option>
                    <option value="other">Other</option>
                </select><br>

                <label for="address">Address:</label>
                <input type="text" id="address" name="address" placeholder="address" required><br>

                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea><hr>

                <button type="submit">Submit</button>
            </form>
        </div>
    </body>
</html>

<script>
document.querySelector('form').addEventListener('submit', function(e) {
    e.preventDefault();
    document.body.innerHTML = `
        <div class="container">
            <header><h1>Thank You!</h1></header>
            <p><h3><b>Your form has been submitted successfully.</b></h3></p>
        </div>
    `;
});
</script>
