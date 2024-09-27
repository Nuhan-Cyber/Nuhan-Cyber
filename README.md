<!DOCTYPE html>
<html>
<head>
  <title>Camera Access</title>
</head>
<body>
  <h1>Click the Button Below to Access the Camera</h1>
  <button id="cameraButton">Click here to access your camera</button>
  <br><br>
  <video id="video" width="640" height="480" autoplay></video>

  <script>
    document.getElementById('cameraButton').addEventListener('click', async function() {
      const stream = await navigator.mediaDevices.getUserMedia({ video: true });
      document.getElementById('video').srcObject = stream;
    });
  </script>
</body>
</html>
