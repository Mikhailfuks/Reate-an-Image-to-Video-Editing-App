<!DOCTYPE html>
<html>
<head>
  <title>Image to Video Editor</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Image to Video Editor</h1>

  <input type="file" id="image-input" accept="image/*">

  <div>
    <label for="duration">Duration (seconds):</label>
    <input type="number" id="duration" value="5">
  </div>

  <div>
    <!-- Add controls for transitions, music, etc. here -->
  </div>

  <video id="video-preview" controls width="640" height="360"></video>

  <button id="create-video-button">Create Video</button>
  <button id="download-video-button" disabled>Download Video</button>

  <script src="script.js"></script>
</body>
</html>



const imageInput = document.getElementById('image-input');
const durationInput = document.getElementById('duration');
const createVideoButton = document.getElementById('create-video-button');
const downloadVideoButton = document.getElementById('download-video-button');
const videoPreview = document.getElementById('video-preview');

let selectedImages = [];

imageInput.addEventListener('change', (event) => {
  const files = event.target.files;
  selectedImages = Array.from(files);
});

createVideoButton.addEventListener('click', createVideo);

function createVideo() {
  // Validation and checks (e.g., ensure at least one image is selected)

  // Use a video library to create the video (e.g., FFmpeg.wasm, jsmpeg, canvas-to-video)
  // Example using jsmpeg:
  // const video = jsmpeg(selectedImages, { duration: durationInput.value });
  // videoPreview.src = video.src;

  // Add editing effects (e.g., transitions, music)

  // ...

  downloadVideoButton.disabled = false;
}

downloadVideoButton.addEventListener('click', () => {
  // Implement code to download the created video (e.g., using a Blob URL)
  // ...
});
