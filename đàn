<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Piano Online</title>
  <style>
    body { text-align: center; font-family: sans-serif; }
    h1 { margin-top: 20px; }
    .piano { display: flex; justify-content: center; margin-top: 40px; position: relative; }
    .key {
      width: 60px; height: 220px; margin: 1px;
      border: 1px solid black; background: white;
      display: flex; align-items: flex-end; justify-content: center;
      cursor: pointer; user-select: none;
      position: relative; z-index: 1;
    }
    .key:active { background: #ddd; }
    .black {
      width: 40px; height: 140px;
      background: black; color: white;
      position: absolute; top: 0;
      margin-left: -20px; margin-right: -20px;
      z-index: 2;
    }
    .black:active { background: #444; }
  </style>
</head>
<body>
  <h1>🎹 Piano Online (C4 → C5)</h1>
  <div class="piano">
    <!-- Phím trắng -->
    <div class="key" data-note="C4">C</div>
    <div class="key" data-note="D4">D</div>
    <div class="key" data-note="E4">E</div>
    <div class="key" data-note="F4">F</div>
    <div class="key" data-note="G4">G</div>
    <div class="key" data-note="A4">A</div>
    <div class="key" data-note="B4">B</div>
    <div class="key" data-note="C5">C</div>

    <!-- Phím đen (nằm đè lên) -->
    <div class="key black" style="left: 90px;" data-note="C#4">C#</div>
    <div class="key black" style="left: 150px;" data-note="D#4">D#</div>
    <div class="key black" style="left: 270px;" data-note="F#4">F#</div>
    <div class="key black" style="left: 330px;" data-note="G#4">G#</div>
    <div class="key black" style="left: 390px;" data-note="A#4">A#</div>
  </div>

  <script>
    const notes = {
      "C4": "https://piano-sounds.s3.us-east-2.amazonaws.com/C4.mp3",
      "C#4": "https://piano-sounds.s3.us-east-2.amazonaws.com/Cs4.mp3",
      "D4": "https://piano-sounds.s3.us-east-2.amazonaws.com/D4.mp3",
      "D#4": "https://piano-sounds.s3.us-east-2.amazonaws.com/Ds4.mp3",
      "E4": "https://piano-sounds.s3.us-east-2.amazonaws.com/E4.mp3",
      "F4": "https://piano-sounds.s3.us-east-2.amazonaws.com/F4.mp3",
      "F#4": "https://piano-sounds.s3.us-east-2.amazonaws.com/Fs4.mp3",
      "G4": "https://piano-sounds.s3.us-east-2.amazonaws.com/G4.mp3",
      "G#4": "https://piano-sounds.s3.us-east-2.amazonaws.com/Gs4.mp3",
      "A4": "https://piano-sounds.s3.us-east-2.amazonaws.com/A4.mp3",
      "A#4": "https://piano-sounds.s3.us-east-2.amazonaws.com/As4.mp3",
      "B4": "https://piano-sounds.s3.us-east-2.amazonaws.com/B4.mp3",
      "C5": "https://piano-sounds.s3.us-east-2.amazonaws.com/C5.mp3"
    };

    document.querySelectorAll(".key").forEach(key => {
      key.addEventListener("click", () => {
        const note = key.dataset.note;
        if (notes[note]) {
          const audio = new Audio(notes[note]);
          audio.play();
        }
      });
    });
  </script>
</body>
</html>
