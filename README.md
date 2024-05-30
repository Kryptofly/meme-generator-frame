# meme-generator-frame
meme-generator-frame for warpcast
Yes, you need to create a repository and put the HTML code into a file. Here's how you can do it:

Create a Repository: First, create a new repository on GitHub (or any Git provider you prefer).

Add the HTML File: In your new repository, create a file named index.html and paste the HTML code into this file. Here's the file format:

html
Αντιγραφή κώδικα
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meme Generator</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; }
        #meme { max-width: 100%; }
    </style>
</head>
<body>
    <h1>Meme Generator</h1>
    <input type="text" id="topText" placeholder="Top Text"><br><br>
    <input type="text" id="bottomText" placeholder="Bottom Text"><br><br>
    <button onclick="generateMeme()">Generate Meme</button>
    <br><br>
    <img id="meme" src="" alt="Your Meme">
    <script>
        function generateMeme() {
            const topText = document.getElementById('topText').value;
            const bottomText = document.getElementById('bottomText').value;
            const memeUrl = `https://api.memegen.link/images/custom/${topText}/${bottomText}.png`;
            document.getElementById('meme').src = memeUrl;
        }
    </script>
</body>
</html>
Detailed Steps:
Step 1: Create a New Repository
Go to GitHub: Navigate to GitHub.
New Repository: Click on the "New" button to create a new repository.
Repository Name: Give your repository a name, for example, meme-generator-frame.
Visibility: Choose the visibility (public or private) based on your preference.
Create Repository: Click the "Create repository" button.
Step 2: Add index.html to the Repository
Add File: Click on "Add file" and then "Create new file".
File Name: Name the file index.html.
Paste Code: Paste the HTML code into the editor.
Commit Changes: Scroll down and click "Commit new file" to save the file to your repository.
Step 3: Deploy with Vercel
Sign Up / Log In: Go to Vercel and sign up or log in.
New Project: Click on "New Project".
Import from Git: Choose "Import from Git Repository".
Authorize: Authorize Vercel to access your GitHub account if prompted.
Select Repository: Select the repository you just created (e.g., meme-generator-frame).
Project Settings: Configure the project settings. Ensure the framework is set to "Other".
Deploy: Click on the "Deploy" button.
Step 4: Get the URL and Embed in Warpcast
Get URL: Once the deployment is complete, you will receive a public URL.
Embed Code: Use the following JSON to embed your Frame in Warpcast:
json
Αντιγραφή κώδικα
{
  "type": "frame",
  "url": "https://your-deployed-frame-url.vercel.app",
  "description": "Generate memes instantly!"
}
Add to Warpcast: Go to your Warpcast account and use the above JSON to add your Frame.
By following these steps, you will have your HTML code in a repository, deployed on Vercel, and embedded in Warpcast.
