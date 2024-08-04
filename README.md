<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>sweet love</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: 'Helvetica', sans-serif;
            font-size: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;ffmpeg -i

            margin: 0;
        }
        .typing-container {
            white-space: pre-wrap;
            overflow: hidden;
        }
    </style>
</head>
<body>
    <div class="typing-container" id="typing-container"></div>
    <audio src="ffmpeg -i 1c2690d1b29d558ebd41357082c53944.mp4 -vn -acodec mp3 output.mp3"
 autoplay style="display:none;"></audio>
    <script>
        const lyrics = [
            { text: "Cause I'll be waiting for your love", speed: 80 },
            { text: "Let's fly away together", speed: 70 },
            { text: "Let's get this dream forever", speed: 50 },
            { text: "Let's dance like we're in heaven", speed: 60 },
            { text: "Just give me your sweet love", speed: 60 },
            { text: "Let's fly away together", speed: 80 },
            { text: "Let's get this dream forever", speed: 80 },
            { text: "Let's dance like we're in heaven", speed: 80 },
            { text: "Just give me your sweet love", speed: 60 },
        ];

        const delays = [0.9, 2.0, 3.7, 5.4, 7.1, 8.8, 10.5, 12.2, 13.9];
        const container = document.getElementById('typing-container');

        async function typeLyrics() {
            for (let i = 0; i < lyrics.length; i++) {
                const { text, speed } = lyrics[i];
                const delay = i === 0 ? delays[i] : delays[i] - delays[i - 1];
                
                await new Promise(r => setTimeout(r, delay * 1000));
                
                for (const char of text) {
                    container.textContent += char;
                    await new Promise(r => setTimeout(r, speed));
                }
                container.textContent += '\n';
            }
        }

        typeLyrics();
    </script>
</body>
</html>

