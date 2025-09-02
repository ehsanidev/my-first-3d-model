My First 3D Model

A beginner-friendly project to learn the fundamentals of loading and displaying 3D models on the web using Three.js, including environment lighting.

./screenshot.png 🔺 Screenshot of the 3D model rendering

🚀 Live Demo

You can view the live project here:
https://3dteapot.netlify.app

📁 Project Structure

```
my-first-3d-model/
├── index.html
├── index.js
├── package.json
├── model/
│   ├── teapot.glb          # The 3D model file
│   └── environment.hdr     # HDRI environment map for realistic lighting
├── assets/
│   └── screenshot.png      # Project screenshot
└── README.md
```

🛠️ Tech Stack

· Three.js: The main 3D library for rendering.
· Vite (or similar tool): Suggested by package.json for bundling and development.
· HTML5: The structure of the web page.
· Vanilla JavaScript: Logic for loading and controlling the 3D scene.
· GLTFLoader: Three.js component for loading .glb/.gltf models.
· RGBELoader: Three.js component for loading .hdr environment maps.

✨ Features

· Loads and displays a 3D model (.glb format) in a web browser.
· Basic scene setup with a camera, lights, and a renderer.
· Simple orbit controls to allow users to drag and view the model from different angles.
· Includes an HDRI environment map (.hdr file) for realistic image-based lighting (currently commented out in the code).

🧠 Learning Objectives

This project was built to understand:

· How to set up a basic Three.js scene.
· How to load and display 3D models using GLTFLoader.
· The role of lights and environment maps for realistic rendering.
· How to use OrbitControls for user interaction.
· The difference between local development and production deployment.

⚠️ Current Challenge

The 3D model fails to load when deployed to free hosting platforms like Netlify.

· The Problem: The model (.glb file) do not appear on the live site, even though they work perfectly on the local development server.
· Potential Causes:
  · Incorrect file paths in the code after deployment.
  · The asset files are not being included in the deployment build or are being ignored.
  · The server might not be configured to serve .glb file with the correct MIME type (model/gltf-binary for .glb, image/hdr for .hdr).
· Next Steps: I am actively investigating Netlify's deployment configuration and asset handling to resolve this issue.

🔧 Code Note: Environment Map

The code includes the necessary setup for using an HDRI environment map for realistic lighting, but it is currently commented out for debugging the main model loading issue.

```javascript
// Code to load the HDR environment map is present but commented out.
// new RGBELoader().load( './model/environment.hdr', function ( texture ) {
//     scene.environment = texture;
//     scene.background = texture;
// } );
```

🚧 Future Improvements

· Fix the deployment issue on Netlify/Vercel.
· Uncomment and activate the HDR environment lighting.
· Add more interactive controls (zoom in/out, reset view).
· Implement a loading animation while the model and environment are being fetched.
· Experiment with different models and environments.

📦 Installation & Local Run

This project uses a package manager (as indicated by package.json). To run it locally:

1. Clone the repository
   ```bash
   git clone https://github.com/ehsanidev/my-first-3d-model.git
   cd my-first-3d-model
   ```
2. Install dependencies
   ```bash
   npm install
   ```
3. Run the development server
   ```bash
   npm run dev
   ```
   Open the provided local URL (e.g., http://localhost:5173) in your browser.

---

👩‍💻 Developer

· [GitHub](https://github.com/ehsanidev)
· [LinkedIn](https://linkedin/in/zahraehsani)
