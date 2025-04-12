<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Urban Infrastructure Dashboard</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/three@0.150.1/build/three.min.js"></script>
  <style>
    body { 
      font-family: 'Segoe UI', sans-serif;
          margin: 0;
          background-color: #f0f4f8;
          color: #333;
         }
    header
    { 
      background-color: #2a5298;
      color: white;
      padding: 20px;
      text-align: center; 
    }
    nav 
    { 
      display: flex;
      justify-content: center;
      background-color: #ddd; 
    }
    nav button 
    { 
      background-color: #eee;
      border: none;
      padding: 15px 20px;
      cursor: pointer; 
      font-size: 16px;
    }
    nav button:hover, nav button.active
    { 
      background-color: #2a5298; 
      color: white;
    }
    .container
    { 
      padding: 20px; 
      max-width: 1000px;
      margin: auto;
    }
    .section 
    { display: none; 
     padding: 20px; 
     background: white;
     border-radius: 10px;
     box-shadow: 0 2px 8px rgba(0,0,0,0.1); 
     margin-bottom: 20px;
    }
    .section.active 
    { 
      display: block; 
    }
    .btn-effect6
    { 
      position: relative;
      display: inline-block;
      padding: 12px 30px; 
      font-size: 16px; 
      font-weight: bold;
      color: #fff; 
      background: #031809;
      cursor: pointer;
      margin-right: 10px;
    }
    .btn-effect6::before 
    { content: "";
     position: absolute;
     top:0;
     left:-100%;
     width:100%;
     height:100%;
     background:#2980b9;
     transition: all 0.4s ease;
     z-index:1; 
    }
    .btn-effect6:hover::before 
    {
      left:0; 
    }
    .btn-effect6 span
    {
      position: relative;
      z-index:2;
    }
    .alert
    {
      background:#ffdddd;
      color:#d8000c;
      padding:10px;
      margin-top:10px;
      border-left:6px solid #d8000c;
    }
    .chart-container
    {
      position: relative;
      width:100%;
      height:400px;
      margin-top:20px;
    }
    #pieChart 
    {
      width:100%;
      height:400px;
    }
    #threeContainer
    {
      width:100%;
      height:300px;
      margin-top:20px;
    }
    input 
    { padding:8px;
     margin:5px 0;
     width:100%;
     box-sizing:border-box; 
    }
  </style>
</head>
<body>
  <header>
    <h1>Urban Infrastructure Monitoring Dashboard</h1>
    <p>Comprehensive real-time insights with interactive 3D visuals and animated charts.</p>
  </header>
  <nav>
    <button class="tab active" onclick="showSection('overview')">Overview</button>
    <button class="tab" onclick="showSection('dataInput')">Data Input</button>
    <button class="tab" onclick="showSection('insights')">Maintenance Insights</button>
    <button class="tab" onclick="showSection('reports')">Report Generation</button>
  </nav>
  <div class="container">
    <div id="overview" class="section active">
      <h2>Overview</h2>
      <p>Welcome to the Urban Infrastructure Dashboard, designed to provide city planners and engineers with real-time monitoring, predictive maintenance insights, and dynamic reporting tools. Utilize interactive charts and 3D visualizations to stay ahead of structural risks and optimize resource allocation.</p>
      <div id="threeContainer"></div>
    </div>
    <div id="dataInput" class="section">
      <h2>Data Input</h2>
      <p>Enter current sensor readings to visualize infrastructure health metrics. Data updates animate the charts instantly for immediate feedback.</p>
      <label>Stress Level (%):</label><input type="number" id="stressInput" placeholder="e.g. 75">
      <label>Water Level (cm):</label><input type="number" id="waterInput" placeholder="e.g. 120">
      <label>Traffic Density (veh/hr):</label><input type="number" id="trafficInput" placeholder="e.g. 450">
      <div id="alertsContainer"></div>
      <div class="chart-container"><canvas id="pieChart"></canvas></div>
    </div>
    <div id="insights" class="section">
      <h2>Maintenance Insights</h2>
      <p>Generate actionable recommendations based on historical trends and real-time anomalies to ensure timely interventions and cost-effective maintenance.</p>
      <button class="btn-effect6" onclick="generateInsights()"><span>Generate Insights</span></button>
      <div id="insightsContainer"></div>
    </div>
    <div id="reports" class="section">
      <h2>Report Generation</h2>
      <p>Export comprehensive reports in PDF or Excel formats, including interactive snapshots of charts and 3D models.</p>
      <input type="file" id="file"><button class="btn-effect6"><span>Upload</span></button>
    </div>
  </div>
  <footer>&copy; 2025 Urban Infrastructure Dashboard</footer>
  <script>
    let pieChart;
    function showSection(id){
      document.querySelectorAll('.section').forEach(s=>s.classList.remove('active'));
      document.querySelectorAll('.tab').forEach(t=>t.classList.remove('active'));
      document.getElementById(id).classList.add('active');event.target.classList.add('active');
    }
    function updateChart(){
      const s=+document.getElementById('stressInput').value||0;
      const w=+document.getElementById('waterInput').value||0;
      const t=+document.getElementById('trafficInput').value||0;
      document.getElementById('alertsContainer').innerHTML = (s>80?'<div class="alert">⚠️ Stress high!</div>':'')+(w>100?'<div class="alert">⚠️ Water high!</div>':'')+(t>500?'<div class="alert">⚠️ Traffic high!</div>':'')||'<div class="alert" style="background:#ddffdd;color:green;border-color:green;">✅ All safe.</div>';pieChart.data.datasets[0].data=[s,w,t];pieChart.update({duration:800, easing:'easeOutBounce'});
    }
    function generateInsights(){const ins=["Bridge A exceeded stress threshold","Drainage surges post-rain","Road X peak congestion"];const rec=["Inspect within 48h","Upgrade drainage","Plan alternate routes"];const c=document.getElementById('insightsContainer');c.innerHTML='';ins.forEach((i,idx)=>c.innerHTML+=`<div class='insight'><strong>${i}</strong><br>Recommendation: ${rec[idx]}</div>`);}    
    function init3D(){const scene=new THREE.Scene(),cam=new THREE.PerspectiveCamera(75,window.innerWidth/300,0.1,1000),rnd=new THREE.WebGLRenderer({antialias:true});rnd.setSize(window.innerWidth,300);document.getElementById('threeContainer').appendChild(rnd.domElement);const geom=new THREE.BoxGeometry(),mat=new THREE.MeshNormalMaterial();const cube=new THREE.Mesh(geom,mat);scene.add(cube);cam.position.z=3;function ani(){requestAnimationFrame(ani);cube.rotation.x+=0.01;cube.rotation.y+=0.01;rnd.render(scene,cam);}ani();}
    window.addEventListener('DOMContentLoaded',()=>{const ctx=document.getElementById('pieChart').getContext('2d');pieChart=new Chart(ctx,{type:'pie',data:{labels:['Stress','Water','Traffic'],datasets:[{data:[0,0,0],backgroundColor:['#FF6384','#36A2EB','#FFCE56']}]},options:{animation:{animateScale:true,animateRotate:true}}});['stressInput','waterInput','trafficInput'].forEach(id=>document.getElementById(id).addEventListener('input',updateChart));init3D();});
  </script>
</body>
</html>
