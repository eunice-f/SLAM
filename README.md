<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<title>OpenClaw Project Page</title>
<meta name="viewport" content="width=device-width, initial-scale=1">

<style>

/* ---------- global ---------- */
*,
*::before,
*::after{
  box-sizing:border-box;
}

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
  font-size:3em;
  margin-bottom:15px;
  line-height:1.25;
  font-weight:600;
}

.main-title{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:9px;
}

.main-title img{ height:2.5em; }

.authors{
  text-align:center;
  font-size:1.15em;
}

.affiliation{
  text-align:center;
  color:#666;
  margin-bottom:28px;
}

/* ---------- buttons ---------- */
.links{
  text-align:center;
  margin:30px 0 20px 0;
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

.links a.disabled{
  pointer-events:none;
  cursor:default;
  opacity:.45;
}

/* ---------- sections ---------- */
.section{ margin-top:55px; }

h2{
  border-bottom:2px solid #eee;
  padding-bottom:6px;
  font-weight:600;
}

p{ font-size:17px; }

/* ---------- KPI cards (FIXED) ---------- */
.kpi{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:14px;
  margin-top:22px;
}

.kpi .card{
  border:1px solid #eee;
  border-radius:12px;
  padding:16px;
  background:#fff;
  box-shadow:0 4px 18px rgba(0,0,0,.05);
}

.kpi .big{
  font-size:20px;
  font-weight:700;
}

.kpi .small{
  font-size:13px;
  color:#666;
  margin-top:6px;
}

/* ---------- video ---------- */
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
  inset:0;
  width:100%;
  height:100%;
  border:0;
}

/* ---------- images ---------- */
.teaser{
  width:100%;
  border-radius:12px;
  box-shadow:0 4px 18px rgba(0,0,0,.08);
}

/* ---------- video grid ---------- */
.yt-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:28px;
}

.yt-card{text-align:center;}

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
  margin-top:14px;
  font-size:15px;
  color:#444;
  line-height:1.55;
}

/* ---------- footer ---------- */
.footer{
  text-align:center;
  margin-top:70px;
  font-size:.9em;
  color:#888;
}

.resource-note{
  text-align:center;
  font-size:14px;
  color:#777;
  margin-top:10px;
  font-style:italic;
}


/* ---------- responsive ---------- */
@media (max-width:700px){
  .yt-grid{ grid-template-columns:1fr; }
  h1{ font-size:2.2em; }
}

</style>
</head>

<body>
<div class="container">

<h1 class="main-title">
<img src="icon.png">
StrucLine-SLAM: A Lightweight and Fully Geometric SLAM System for Structure-Dominant Environments
</h1>

<div class="authors">Anonymous Authors</div>
<div class="affiliation">Affiliation withheld for double-blind review</div>

  <div class="badges">
    <span>Stereo SLAM</span>
    <span>Line-first Geometry</span>
    <span>CPU-only / No Learning</span>
    <span>Structured & Texture-sparse Scenes</span>
    <span>New Dataset: StructScenes</span>
  </div>

<div class="links">
<a href="https://www.youtube.com/watch?v=MN1LQOo9EvI" target="_blank">Video</a>
<a class="disabled">Code</a>
<a class="disabled">Dataset</a>
<a class="disabled">Hardware</a>
<a class="disabled">Paper</a>
</div>

<div class="resource-note">
Code, dataset, and hardware files will be released upon publication.
</div>


<!-- ABSTRACT -->
<div class="section">
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


</div>
</div>

<!-- VIDEO -->
<div id="video" class="section">
<h2>Project Video</h2>
<div class="video">
<iframe src="https://www.youtube.com/embed/MN1LQOo9EvI" allowfullscreen></iframe>
</div>
</div>


<!-- ===== 3x3 YouTube hover grid1 ===== -->
<div class="section">
<h2>Results Highlights</h2>
<div class="yt-grid">

<div class="yt-card"><div class="yt-wrap">
<iframe src="https://www.youtube.com/embed/SYaSyBR9w3k?autoplay=1&mute=1&loop=1&playlist=SYaSyBR9w3k&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
</div><div class="yt-label">StructScenes: Greenhouse</div></div>

<div class="yt-card"><div class="yt-wrap">
<iframe src="https://www.youtube.com/embed/H9RilUamtgU?autoplay=1&mute=1&loop=1&playlist=H9RilUamtgU&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
</div><div class="yt-label">StructScenes: Solar Farm</div></div>

<div class="yt-card"><div class="yt-wrap">
<iframe src="https://www.youtube.com/embed/PIEjIHkYz9Y?autoplay=1&mute=1&loop=1&playlist=PIEjIHkYz9Y&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
</div><div class="yt-label">StructScenes: Indoor Workshop (low-texture)</div></div>

<div class="yt-card"><div class="yt-wrap">
<iframe src="https://www.youtube.com/embed/MPm3F5_-X9w?autoplay=1&mute=1&loop=1&playlist=MPm3F5_-X9w&controls=0&rel=0&modestbranding=1" allow="autoplay"></iframe>
</div><div class="yt-label">StructScenes: EuRoC / TartanAir (structured)</div></div>


<div class="section-caption">
  <strong>Results Highlights.</strong>
  Representative executions across the nine-task removal suite under held-out real-robot conditions with synchronized multi-view observations and fingertip force traces.
</div>

</div>
</div>



<div class="section">
  <h2>Citation</h2>
  <pre>
@inproceedings{struclineslam2026,
  title     = {StrucLine-SLAM: A Lightweight and Fully Geometric SLAM System for Structure-Dominant Environments},
  author    = {Anonymous Authors},
  booktitle = {Submitted to IROS},
  year      = {2026}
}
  </pre>
</div>

<div class="footer">
  Project page template for robotics research papers
</div>

</div>

</body>
</html>


</div>

<!-- FOOTER -->
<div class="footer">
Project page for robotics research papers
</div>

</div>
</body>
</html>
