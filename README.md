<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Research Output Demos</title>
    <!-- Add CSS for Flexbox and Styling -->
    <style>
        .section {
            margin-top: 40px;
        }
        .audio-row {
            display: flex;
            justify-content: space-around;
            align-items: center;
            flex-wrap: wrap;
            gap: 20px;  /* Space between elements */
            margin-bottom: 30px;  /* Space after each row */
        }
        .audio-item {
            flex: 1;
            text-align: center;
            min-width: 200px; /* Ensures space allocation for audio clips */
        }
        audio {
            width: 100%;
        }
        .section img {
            width: 80%;
            margin: 20px auto;
            display: block;
        }

        /* Video section styles */
        .video-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
            align-items: start;
            margin-top: 10px;
        }
        .video-item {
            text-align: center;
        }
        .video-item video {
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        .video-item figcaption {
            font-size: 0.95rem;
            color: #444;
            margin-top: 6px;
        }
        .section h1 small {
            font-weight: normal;
            font-size: 0.7em;
            color: #666;
        }
    </style>
</head>

<body>

<p>
  This is the page showcasing some of my research topics' output demos,
  for my creative works:
  (<a href="https://shinxinyangdemo.github.io" target="_blank">
  shinxinyangdemo.github.io</a>)
</p>

<!-- ✅ First Section: Dominant-Note–Conditioned Generation & Editing (Pilot) -->
<div class="section">
  <h1>
    Dominant-Note–Conditioned Generation &amp; Editing
    <small>(pilot results; work in progress)</small>
  </h1>

  <p>
    Early experiments on music <b>generation</b> and <b>editing</b> using a simple harmonic control signal:
    the <b>smoothed dominant note</b> estimated from a chromagram.
  </p>

  <!-- Disclaimer -->
  <div class="disclaimer">
    <p><b>Disclaimer.</b> The generation model is trained on a <b>licensed dataset</b> for research in generative music.
      The editing demos include short excerpts from songs I personally enjoy; these tracks are used <b>only for qualitative evaluation</b>
      and are <b>not used for training</b>.
    </p>
  </div>

  <!-- Method overview -->
  <div class="method">
    <h3>How it works (high level)</h3>
    <ul>
      <li>
        <b>Generation:</b> input a <b>chromagram</b> → compute a <b>temporally smoothed dominant-note trajectory</b> →
        generate <b>44.1 kHz stereo</b> audio conditioned on that trajectory.
      </li>
      <li>
        <b>Editing:</b> take any source audio → extract its chromagram → set / modify the dominant-note condition →
        perform inversion-based editing to keep parts of the original character while steering harmonic content toward the target dominant notes.
      </li>
    </ul>

    <p class="note">
      This is intended as a potential musician-facing editing tool: it can operate on <b>full mixed songs</b> (not just isolated stems),
      where traditional DAW workflows often struggle to “surgically” decouple and rewrite harmonic content.
    </p>
  </div>

  <div class="video-grid">
    <figure class="video-item">
      <video controls preload="metadata" playsinline>
        <source src="generate_2.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <figcaption><b>Generating:</b> dominant-note conditioned music generation.</figcaption>
    </figure>

    <figure class="video-item">
      <video controls preload="metadata" playsinline>
        <source src="edit_2.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <figcaption><b>Editing:</b> inversion-based editing guided by a dominant-note condition.</figcaption>
    </figure>
  </div>
</div>


    <!-- First Section: GNN Guided Mashup Generation -->
    <div class="section">
        <h1>Graph Neural Network Guided Music Mashup Generation</h1>

<!-- Audio Rows -->
<div class="audio-row">
    <div class="audio-item">
        <h3>Original 1</h3>
        <audio controls>
            <source src="original_1.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Original 2</h3>
        <audio controls>
            <source src="original_12.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Mashup 1</h3>
        <audio controls>
            <source src="mashup_1.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
</div>

<div class="audio-row">
    <div class="audio-item">
        <h3>Original 1</h3>
        <audio controls>
            <source src="original_2.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Original 2</h3>
        <audio controls>
            <source src="original_22.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Mashup 2</h3>
        <audio controls>
            <source src="mashup_2.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
</div>

<div class="audio-row">
    <div class="audio-item">
        <h3>Original 1</h3>
        <audio controls>
            <source src="original_3.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Original 2</h3>
        <audio controls>
            <source src="original_32.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Mashup 3</h3>
        <audio controls>
            <source src="mashup_3.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
</div>

<div class="audio-row">
    <div class="audio-item">
        <h3>Original 1</h3>
        <audio controls>
            <source src="original_4.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Original 2</h3>
        <audio controls>
            <source src="original_42.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Mashup 4</h3>
        <audio controls>
            <source src="mashup_4.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
</div>

<div class="audio-row">
    <div class="audio-item">
        <h3>Original 1</h3>
        <audio controls>
            <source src="original_5.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Original 2</h3>
        <audio controls>
            <source src="original_52.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
    <div class="audio-item">
        <h3>Mashup 5</h3>
        <audio controls>
            <source src="mashup_5.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
    </div>
</div>

<p>Original 1 provides the vocals and instrumentals, original 2 provides the instrumentals, the mashup instrumental is rearranged through the network which is a fusion of both originals</p>

<p align="center">
  <img src="gnn_model_overview.jpg" width="700"><br>
</p>


    </div>

    <!-- Second Section: Diffusion Models for Automatic Music Mixing -->
    <div class="section">
        <h1>Diffusion Models for Automatic Music Mixing</h1>


        <!-- Audio Rows -->
        <div class="audio-row">
            <div class="audio-item">
                <h3>Imbalanced Input 1</h3>
                <audio controls>
                    <source src="imbalanced_input_1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
            <div class="audio-item">
                <h3>Diffusion Mix 1</h3>
                <audio controls>
                    <source src="diffusion_mix_1.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
        </div>

        <div class="audio-row">
            <div class="audio-item">
                <h3>Imbalanced Input 2</h3>
                <audio controls>
                    <source src="imbalanced_input_2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
            <div class="audio-item">
                <h3>Diffusion Mix 2</h3>
                <audio controls>
                    <source src="diffusion_mix_2.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
        </div>

        <div class="audio-row">
            <div class="audio-item">
                <h3>Imbalanced Input 3</h3>
                <audio controls>
                    <source src="imbalanced_input_3.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
            <div class="audio-item">
                <h3>Diffusion Mix 3</h3>
                <audio controls>
                    <source src="diffusion_mix_3.wav" type="audio/wav">
                    Your browser does not support the audio element.
                </audio>
            </div>
        </div>

    </div>

<script>
  const audios = Array.from(document.querySelectorAll('audio'));
  audios.forEach(a => {
    a.addEventListener('play', () => {
      audios.forEach(b => {
        if (b !== a && !b.paused) b.pause();
      });
    });
  });
</script>
    
<h1>End</h1>

</body>
</html>
