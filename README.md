<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Teen Wealth Ambition</title>
    <style>
        /* Basic CSS for styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
        }
        nav {
            background-color: #444;
            padding: 10px;
            text-align: center;
        }
        nav a {
            color: #fff;
            text-decoration: none;
            margin: 0 10px;
        }
        section {
            padding: 20px;
        }
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 10px;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Teen Wealth Ambition</h1>
    </header>
    <nav>
        <a href="#">Home</a>
        <a href="#">Profile</a>
        <a href="#">Friends</a>
        <a href="#">Logout</a>
    </nav>
    <section>
        <h2>Post Something</h2>
        <textarea id="postContent" rows="4" cols="50" placeholder="What's on your mind?"></textarea>
        <br>
        <button onclick="post()">Post</button>
    </section>
    <section id="posts">
        <!-- Posts will be displayed here -->
    </section>
    <footer>
        &copy; 2024 Teen Wealth Ambition
    </footer>

    <script>
        // Basic JavaScript for posting functionality
        function post() {
            var content = document.getElementById('postContent').value;
            if (content.trim() === '') {
                alert('Please enter some content!');
                return;
            }
            var postElement = document.createElement('div');
            postElement.className = 'post';
            postElement.innerHTML = '<p>' + content + '</p>';
            document.getElementById('posts').appendChild(postElement);
            document.getElementById('postContent').value = '';
        }
    </script>
</body>
</html>

