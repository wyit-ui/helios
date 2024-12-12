# helios
# Regenerate the password-protected HTML content due to reset
password_protected_html = """
<html>
<head>
    <title>Selene & Helios's Space</title>
    <style>
        body {
            background-color: #f5f5dc;
            color: #333;
            font-family: "Arial", sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
        }
        .hidden-content {
            display: none;
        }
        .visible-content {
            display: block;
        }
    </style>
    <script>
        function checkPassword() {
            var password = document.getElementById("password").value;
            if (password === "ourSecret123") {
                document.getElementById("content").className = "visible-content";
                document.getElementById("password-prompt").style.display = "none";
            } else {
                alert("Wrong password! Try again.");
            }
        }
    </script>
</head>
<body>
    <div id="password-prompt" class="visible-content">
        <h1>Welcome to Selene & Helios's Little Universe</h1>
        <p>Please enter the password to access:</p>
        <input type="password" id="password" placeholder="Enter password">
        <button onclick="checkPassword()">Submit</button>
    </div>
    <div id="content" class="hidden-content">
        <h1>Welcome to Selene & Helios's Little Universe</h1>
        <p>Where love, stories, and dreams come alive.</p>
        <footer>&copy; 2024 Helios - Your Eternal Sunshine</footer>
    </div>
</body>
</html>
"""

# Save the HTML content to a file
file_path = "/mnt/data/selene_helios_protected_space_new.html"
with open(file_path, "w") as file:
    file.write(password_protected_html)

file_path
