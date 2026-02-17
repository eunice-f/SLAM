<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>StrucLine-SLAM Project Page</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<!-- Optional: social preview (replace later) -->
<meta property="og:title" content="StrucLine-SLAM: A Lightweight and Fully Geometric SLAM System for Structure-Dominant Environments">
<meta property="og:description" content="Real-time stereo SLAM with line segments as primary geometric primitives for structured, texture-sparse environments.">
<meta property="og:image" content="teaser.png">

<style>
body{
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
  margin:0;
  background:#fff;
  color:#222;
  line-height:1.65;
}
.container{
  max-width:900px;
  margin:auto;
  padding:50px 20px;
}

h1{
  font-size:3.0em;
  text-align:unset;
  margin-bottom:15px;
  line-height:1.25;
  font-weight:600;
}
.main-title{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:10px;
  text-align:left;
}
.main-title img{ height:2.5em; }

.authors{
  text-align:center;
  font-size:1.15em;
  margin-bottom:6px;
}
.authors span{ margin:0 6px; }

.affiliation{
  text-align:center;
  color:#666;
  margin-bottom:18px;
}

.badges{
  text-align:center;
  margin:10px 0 26px 0;
  color:#666;
  font-size:14px;
}
.badges span{
  display:inline-block;
  margin:6px 6px 0 6px;
  padding:6px 10px;
  border:1px solid #eee;
  border-radius:999px;
  background:#fafafa;
}

.links{
  text-align:center;
  margin:26px 0 10px 0;
}
.links a{
  display:inline-block;
  margin:6px;
  padding:11px 20px;
  border-radius:9px;
  text-decoration:none;
  color:white;
  background:#2d6cdf;
  font-weight:600;
  font-size:15px;
  transition:.2s;
}
.links a:hover{
  background:#1b4fb3;
  transform:translateY(-1px);
}
.links a.secondary{
  background:#111;
}
.links a.secondary:hover{
  background:#000;
}
.links a.disabled{
  pointer-events:none;
  cursor:default;
  opacity:.45;
}
.links a.disabled:hover{
  background:#2d6cdf;
  transform:none;
}

.nav{
  text-align:center;
  margin:10px 0 0 0;
  font-size:14px;
}
.nav a{
  color:#2d6cdf;
  text-decoration:none;
  margin:0 10px;
}
.nav a:hover{ text-decoration:underline; }

.section{ margin-top:55px; }
h2{
  border-bottom:2px solid #eee;
  padding-bottom:6px;
  font-weight:600;
}
p{ font-size:17px; }
ul{ font-size:17px; padding-left:22px; }
.caption{
  margin-top:10px;
  color:#444;
  font-size:15px;
}
.callout{
  background:#f7f9ff;
  border:1px solid #e6ecff;
  border-radius:12px;
  padding:14px 16px;
  margin-top:14px;
  font-size:16px;
}
.kpi{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:14px;
  margin-top:14px;
}
.kpi .card{
  border:1px solid #eee;
  border-radius:12px;
  padding:14px;
  background:#fff;
  box-shadow:0 4px 18px rgba(0,0,0,.04);
}
.kpi .big{ font-size:20px; font-weight:700; }
.kpi .small{ font-size:13px; color:#666; margin-top:4px; }

.video{
  position:relative;
  padding-bottom:56.25%;
  height:0;
  overflow:hidden;
  border-radius:12px;
  box-shadow:0 4px 18px rgba(0,0,0,.08);
}
.video iframe{
  position:absolute;
  top:0; left:0;
  width:100%; height:100%;
  border:0;
}
.teaser{
  width:100%;
  border-radius:12px;
  box-shadow:0 4px 18px rgba(0,0,0,.08);
}

pre{
  background:#f6f6f6;
  padding:18px;
  overflow-x:auto;
  border-radius:10px;
  font-size:14px;
}

hr.sep{
  border:none;
  border-top:1px solid #eee;
  margin:24px 0;
}

/* ---------- YouTube grid ---------- */
.yt-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:28px;
  max-width:900px;
  margin:0 auto;
}
.yt-card{ text-align:center; }
.yt-wrap{
  position:relative;
  width:100%;
  padding-bottom:56.25%;
  border-radius:12px;
  overflow:hidden;
  box-shadow:0 4px 18px rgba(0,0,0,.08);
  background:#000;
}
.yt-wrap iframe{
  position:absolute;
  inset:0;
  width:100%;
  height:100%;
  border:0;
}
.yt-label{
  margin-top:6px;
  font-size:14px;
  font-weight:600;
  color:#333;
}
.section-caption{
  margin-top:12px;
  font-size:15px;
  color:#444;
  line-height:1.55;
}

.footer{
  text-align:center;
  margin-top:70px;
  font-size:.9em;
  color:#888;
}

@media (max-width:800px){
  h1{ font-size:2.2em; }
  .kpi{ grid-template-columns:1fr; }
}
@media (max-width:700px){
  .yt-grid{ grid-template-columns:1fr; }
}
</style>

<script>
  // Smooth scroll for anchor links
  document.addEventListener("click", function(e){
    const a = e.target.closest('a[href^="#"]');
    if(!a) return;
    const id = a.getAttribute("href").slice(1);
    const el = document.getElementById(id);
    if(!el) return;
    e.preventDefault();
    el.scrollIntoView({behavior:"smooth", block:"start"});
    history.pushState(null, "", "#"+id);
  });
</script>
</head>

<body>
<div class="container">

  <h1 class="main-title">
    StrucLine-SLAM: A Lightweight and Fully Geometric SLAM System for Structure-Dominant Environments
  </h1>

  <div class="authors">
    <span>Anonymous Authors</span>
  </div>

  <div class="affiliation">
    Affiliation withheld for anonymous review
  </div>

  <div class="badges">
    <span>Stereo SLAM</span>
    <span>Line-first Geometry</span>
    <span>CPU-only / No Learning</span>
    <span>Structured & Texture-sparse Scenes</span>
    <span>New Dataset: StructScenes</span>
  </div>

  <div class="links">
    <!-- Replace these URLs later -->
    <a href="https://www.youtube.com/watch?v=REPLACE_WITH_PROJECT_VIDEO" target="_blank" rel="noopener noreferrer">Video</a>
    <a href="paper.pdf" target="_blank" rel="noopener noreferrer">Paper (PDF)</a>
    <a class="disabled" title="Replace with your repo link">Code</a>
    <a class="disabled" title="Replace with your dataset link">Dataset</a>
    <a class="secondary" href="#citation">BibTeX</a>
  </div>

  <div class="nav">
    <a href="#abstract">Abstract</a>
    <a href="#overview">Overview</a>
    <a href="#method">Method</a>
    <a href="#dataset">StructScenes</a>
    <a href="#results">Results</a>
    <a href="#ablation">Ablations</a>
    <a href="#citation">Citation</a>
  </div>

  <!-- ================= Abstract ================= -->
  <div id="abstract" class="section">
    <h2>Abstract</h2>
    <p>
      Visual SLAM often struggles in structured environments such as corridors, workshops, or photovoltaic fields,
      where textures are sparse and visual cues are repetitive. While line segments offer stable geometric cues in such settings,
      most systems treat them as auxiliary features. We present <strong>StrucLine-SLAM</strong>, a real-time stereo SLAM system that uses line features
      as the main geometric elements for tracking and mapping. The system introduces <strong>sharpness-based filtering</strong>,
      <strong>direction-consistent stereo matching</strong>, and <strong>endpoint-based triangulation</strong>, all based on classical geometric principles
      without relying on GPU acceleration or learning-based techniques. We evaluate it on EuRoC, selected TartanAir sequences,
      and a new <strong>StructScenes</strong> SLAM dataset with nine real-world structured scenes and ground-truth poses.
      StrucLine-SLAM achieves higher trajectory accuracy and clearer structural maps than baselines such as ORB-SLAM3 and ORB-LINE-SLAM,
      showing strong robustness for facility inspection and mapping tasks.
    </p>

    <div class="kpi">
      <div class="card">
        <div class="big">Line-first</div>
        <div class="small">Lines are integrated into tracking, stereo matching, triangulation, BA, loop closure.</div>
      </div>
      <div class="card">
        <div class="big">Fully geometric</div>
        <div class="small">No learning modules, no GPU dependency; real-time on CPU-only platforms.</div>
      </div>
      <div class="card">
        <div class="big">StructScenes</div>
        <div class="small">9 real structured scenes with calibration + ground-truth poses for benchmarking.</div>
      </div>
    </div>
  </div>

  <!-- ================= Project Video ================= -->
  <div id="video" class="section">
    <h2>Project Video</h2>
    <div class="video">
      <!-- Replace with your YouTube embed -->
      <iframe src="https://www.youtube.com/embed/fToNWljt--Q" allowfullscreen></iframe>
    </div>
    <p class="caption">
      Placeholder video embed. Replace <code>REPLACE_WITH_PROJECT_VIDEO</code> with your YouTube ID (or switch to a local MP4 player).
    </p>
  </div>

  <!-- ================= Overview ================= -->
  <div id="overview" class="section">
    <h2>Overview</h2>
    <img src="teaser.png" class="teaser" alt="teaser image">
    <p class="caption">
      Replace <code>teaser.png</code> with a key figure (e.g., system + reconstruction). In the paper, example applications include a handheld stereo rig
      and structure-preserving mapping in photovoltaic/greenhouse/workshop scenes.
    </p>

    <div class="callout">
      <strong>Why lines?</strong> In structure-dominant, texture-sparse environments, point keypoints can be unreliable due to weak texture and repetitive patterns.
      Line segments provide stable geometric cues (larger spatial support and alignment with structural boundaries), enabling more robust tracking and cleaner maps.
    </div>
  </div>

  <!-- ================= Method ================= -->
  <div id="method" class="section">
    <h2>Method</h2>

    <img src="architecture.png" class="teaser" alt="system architecture figure">
    <p class="caption">
      Replace <code>architecture.png</code> with a pipeline figure (e.g., the system architecture diagram). In the paper, the design builds on a modular SLAM
      architecture and highlights line-specific modules integrated across tracking, mapping, and loop closing.
    </p>

    <h3 style="margin-top:22px;">Key Design Choices</h3>
    <ul>
      <li>
        <strong>Line extraction + preprocessing</strong>:
        line segments are detected with LSD and described by LBD; a fallback mechanism applies image sharpening when too few segments pass the threshold.
        A score combines response + length and penalizes boundary clipping; only the top-K lines per frame are kept for diversity.
      </li>
      <li>
        <strong>Direction-consistent stereo line matching</strong>:
        candidate stereo pairs must satisfy an angular consistency threshold in addition to descriptor similarity; tolerances adapt across pyramid levels.
      </li>
      <li>
        <strong>Endpoint-based triangulation for 3D lines</strong>:
        instead of midpoint triangulation, StrucLine-SLAM triangulates both endpoints from stereo correspondences to obtain a 3D segment, improving conditioning
        under perspective distortion, scale change, and narrow baselines.
      </li>
      <li>
        <strong>Joint point-line local mapping + bundle adjustment</strong>:
        introduces a <code>MapLine</code> landmark type; jointly minimizes point reprojection and line residuals (endpoint-to-segment distances) for stable optimization.
      </li>
      <li>
        <strong>Loop closure with line constraints</strong>:
        place recognition considers both point and line vocabularies; loop correction incorporates line endpoint residuals in Sim(3) estimation and merges overlapping lines.
      </li>
    </ul>

    <hr class="sep">

    <h3>Implementation Notes (Placeholders)</h3>
    <p>
      This project page is intentionally lightweight. Add your final implementation details here, e.g.,
      supported camera models, runtime (FPS), CPU specs, and how to reproduce results.
    </p>
    <pre>
# Example (placeholder) commands:
# git clone https://github.com/your_org/strucline-slam.git
# cd strucline-slam
# mkdir build && cd build
# cmake .. && make -j
# ./run_stereo --config configs/zed2i.yaml --dataset /path/to/sequence
    </pre>
  </div>

  <!-- ================= Dataset ================= -->
  <div id="dataset" class="section">
    <h2>StructScenes Dataset</h2>

    <img src="structscenes_examples.png" class="teaser" alt="StructScenes example scenes">
    <p class="caption">
      Replace <code>structscenes_examples.png</code> with a montage of the nine scenes (photovoltaic field, commercial/experimental greenhouse,
      workshops, entrance lobby, collaborative workspace). Ground-truth poses are obtained via COLMAP-based reconstruction with refinement.
    </p>

    <div class="callout">
      <strong>What’s included (as described in the paper):</strong>
      stereo sequences captured with a handheld rig; calibration files; and ground-truth poses. This dataset is designed to benchmark SLAM
      in structured, texture-sparse, repetitive environments where line geometry matters.
    </div>

    <div class="links" style="margin-top:14px;">
      <a class="disabled" title="Replace with dataset download link">Download StructScenes</a>
      <a class="disabled" title="Replace with dataset documentation link">Dataset Docs</a>
    </div>
  </div>

  <!-- ================= Results ================= -->
  <div id="results" class="section">
    <h2>Results</h2>

    <img src="results_overview.png" class="teaser" alt="quantitative results overview">
    <p class="caption">
      Replace <code>results_overview.png</code> with your key quantitative table/plot (e.g., ATE/WATE summary).
      In the paper, StrucLine-SLAM reports improved trajectory accuracy and structural map clarity on EuRoC, selected TartanAir sequences,
      and StructScenes, compared with ORB-SLAM3 and ORB-LINE-SLAM.
    </p>

    <h3 style="margin-top:22px;">Highlights (from the paper)</h3>
    <ul>
      <li><strong>EuRoC</strong>: lowest ATE on 7/11 stereo sequences; improved robustness under long-range motion and texture degradation.</li>
      <li><strong>TartanAir (structured sequences)</strong>: consistently lower trajectory error and cleaner reconstructions in corridor/factory/urban facade settings.</li>
      <li><strong>StructScenes</strong>: strongest performance across all sequences in both ATE and WATE, with more complete trajectories in challenging outdoor scenes.</li>
      <li><strong>Map quality</strong>: fewer spurious lines and more interpretable structure (e.g., frames, boundaries, beams) than hybrid baselines.</li>
    </ul>

    <!-- ===== Results video grid (placeholders) ===== -->
    <div class="section" style="margin-top:30px;">
      <h3>Qualitative Demos (Placeholders)</h3>
      <div class="yt-grid">

        <div class="yt-card">
          <div class="yt-wrap">
            <iframe src="https://www.youtube.com/embed/SYaSyBR9w3k?autoplay=1&mute=1&loop=1&playlist=SYaSyBR9w3k&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
          </div>
          <div class="yt-label">StructScenes: Greenhouse</div>
        </div>

        <div class="yt-card">
          <div class="yt-wrap">
            <iframe src="https://www.youtube.com/embed/H9RilUamtgU?autoplay=1&mute=1&loop=1&playlist=H9RilUamtgU&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
          </div>
          <div class="yt-label">StructScenes: Solar Farm</div>
        </div>

        <div class="yt-card">
          <div class="yt-wrap">
            <iframe src="https://www.youtube.com/embed/PIEjIHkYz9Y?autoplay=1&mute=1&loop=1&playlist=PIEjIHkYz9Y&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
          </div>
          <div class="yt-label">StructScenes: Indoor Workshop (low-texture)</div>
        </div>

        <div class="yt-card">
          <div class="yt-wrap">
            <iframe src="https://www.youtube.com/embed/MPm3F5_-X9w?autoplay=1&mute=1&loop=1&playlist=MPm3F5_-X9w&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
          </div>
          <div class="yt-label">StructScenes: EuRoC / TartanAir (structured)</div>
        </div>

      </div>

      <div class="section-caption">
        <strong>Tip:</strong> For silent looping demos, keep <code>autoplay=1&mute=1&loop=1&playlist=ID</code>.
        Replace each <code>REPLACE_ID_k</code> with your corresponding video ID.
      </div>
    </div>
  </div>

  <!-- ================= Ablations ================= -->
  <div id="ablation" class="section">
    <h2>Ablation Studies</h2>

    <img src="ablation_detector.png" class="teaser" alt="ablation figure">
    <p class="caption">
      Replace <code>ablation_detector.png</code> with the detector comparison (e.g., LSD vs EDLine).
      The paper reports that swapping in EDLine improves ATE/RPE on several EuRoC sequences, indicating the pipeline generalizes across detectors.
    </p>

    <div class="callout">
      <strong>What to show here:</strong>
      (1) detector comparison, (2) matching strategy comparison (direction consistency on/off),
      (3) triangulation strategy comparison (midpoint vs endpoint), (4) loop-closure variants (point-only vs point+line).
    </div>
  </div>

  <!-- ================= Citation ================= -->
  <div id="citation" class="section">
    <h2>Citation</h2>
    <pre>
@inproceedings{struclineslam2026,
  title     = {StrucLine-SLAM: A Lightweight and Fully Geometric SLAM System for Structure-Dominant Environments},
  author    = {Anonymous Authors},
  booktitle = {Submitted to IROS},
  year      = {2026}
}
    </pre>
    <p class="caption">
      Replace venue/year/authors when finalized.
    </p>
  </div>

  <div class="section">
    <h2>Acknowledgements</h2>
    <p>
      (Placeholder) Add funding, lab, and collaborator acknowledgements here.
    </p>
  </div>

  <div class="footer">
    Project page template for robotics/SLAM research papers • Replace placeholders (images/videos/links) with your final assets
  </div>

</div>
</body>
</html>
