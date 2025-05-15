<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vels University - Home</title>

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&display=swap" rel="stylesheet">

  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: #000000;
      color: #ffffff;
      font-size: 16px;
      line-height: 1.6;
    }

    .header {
      background-color: #111111;
      padding: 20px;
      text-align: center;
      box-shadow: 0 2px 5px rgba(255, 165, 0, 0.2);
    }

    .logo {
      max-width: 200px;
      height: auto;
      margin-bottom: 20px;
    }

    @keyframes fadeInSlideUp {
      0% {
        opacity: 0;
        transform: translateY(30px);
      }

      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .welcome-message {
      background-color: #ff6600;
      padding: 50px 20px;
      text-align: center;
      opacity: 0;
      animation: fadeInSlideUp 2s ease-out forwards;
    }

    .aws-title {
      font-family: 'Cinzel', serif;
      font-weight: 700;
      letter-spacing: 1px;
      font-size: 2.8em;
      text-transform: uppercase;
      margin-bottom: 20px;
      color: #000000;
    }

    .nav-bar {
      background-color: #222222;
      padding: 15px;
      text-align: center;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .nav-bar a {
      color: #ffffff;
      background-color: #ff6600;
      padding: 10px 20px;
      text-decoration: none;
      border-radius: 5px;
      font-weight: 600;
      font-size: 1em;
      transition: background-color 0.3s, color 0.3s;
      display: inline-block;
      cursor: pointer;
    }

    .nav-bar a:hover {
      background-color: #ffa347;
      color: #000;
    }

    .content {
      display: none;
      padding: 30px;
      background-color: #111111;
      border-top: 2px solid #ff6600;
    }

    .content.active {
      display: block;
      animation: slideFade 1s ease;
    }

    @keyframes slideFade {
      0% {
        opacity: 0;
        transform: translateY(20px);
      }

      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .section {
      margin-bottom: 20px;
    }

    .section h2 {
      color: #ff6600;
      margin-bottom: 10px;
    }

    ul {
      padding-left: 20px;
    }

    li {
      margin-bottom: 5px;
    }

    pre {
      background-color: #222222;
      padding: 10px;
      border-left: 4px solid #ff6600;
      overflow-x: auto;
    }

    .architecture-image {
      width: 100%;
      max-width: 800px;
      height: auto;
      border: 2px solid #ff6600;
      margin-top: 20px;
    }

    .tool-icons {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      margin-top: 20px;
    }

    .tool-icons img {
      height: 100px;
      transition: transform 0.3s ease;
    }

    .tool-icons img:hover {
      transform: scale(1.1);
    }
  </style>
</head>

<body>
  <div class="header">
    <img src="Linux.png" alt="Linux" class="logo" />
    <img src="ec2.png" alt="ec2" class="logo" />
    <img src="HTML5.png" alt="HTML5" class="logo" />
    
  </div>

  <div class="welcome-message">
    <h1 class="aws-title">HOSTING A STATIC WEBPAGE USING AWS</h1>
    <p>PROJECT</p>
  </div>

  <div class="nav-bar">
    <a onclick="showContent('home')">Overview</a>
    <a onclick="showContent('about')">About The Project</a>
    <a onclick="showContent('services')">Services</a>
    <a onclick="showContent('architecture')">Architecture</a>
  </div>

  <div id="home" class="content">
    <div class="section">
      <h2>Project Overview</h2>
      <p>This project demonstrates hosting a static website using Amazon Web Services (AWS). It involves setting up an EC2 instance with Amazon Linux, installing Apache HTTP Server, and using WinSCP to transfer HTML files for hosting and configuring Private Domain Using AWS Route53.</p>
    </div>
    <div class="section">
      <h2>Technologies Used</h2>
      <ul>
        <li>Amazon EC2</li>
        <li>Amazon Linux</li>
        <li>Apache HTTP Server</li>
        <li>WinSCP</li>
        <li>Route 53</li>
        <li>Hostinger</li>
        <li>HTML</li>
      </ul>
    </div>
    <div class="section">
      <h2>Installation Commands</h2>
      <pre>
sudo -i
cd / 
yum install httpd -y
systemctl start httpd
systemctl status httpd
touch index.html
chmod 777 /var/www/html
      </pre>
    </div>
  </div>

  <div id="about" class="content">
    <div class="section">
      <h2>About The Project</h2>
      <p>This project was developed by a dedicated team of students:</p>
      <ul>
        <li>Gowtham</li>
        <li>Rugin Vishal</li>
        <li>Niyas</li>
        <li>Dev Anand</li>
      </ul>
    </div>
    <div class="section">
      <h2>Purpose of the Project</h2>
      <p>The aim is to gain hands-on AWS experience by building and hosting a static website using EC2, Apache, and Route 53, with a custom domain from Hostinger.</p>
    </div>
    <div class="section">
      <h2>Learning Outcomes</h2>
      <ul>
        <li>Understanding EC2 and Linux configuration</li>
        <li>Hosting with Apache</li>
        <li>Domain routing via Route 53</li>
        <li>Secure file transfer with WinSCP</li>
        <li>Real-world cloud deployment</li>
      </ul>
    </div>
  </div>

  <div id="services" class="content">
    <div class="section">
      <h2>Services / Tools Used</h2>
      <p>The following tools were used to build and deploy the static website:</p>
      <div class="tool-icons">
        <img src="PuTTY.png" alt="PuTTY" />
        <img src="Linux.png" alt="Linux" />
        <img src="HTML5.png" alt="HTML5" />
        <img src="WinSCP.png" alt="WinSCP" />
        <img src="ec2.png" alt="ec2" />
        <img src="Hostinger.png" alt="Hostinger" />
         <img src="route53.png" alt="route53" />
      </div>
    </div>
  </div>

  <div id="architecture" class="content">
    <div class="section">
      <h2>Architecture</h2>
      <p>The architecture includes using Amazon EC2 with Linux OS, Apache for web hosting, domain purchase via Hostinger, and domain routing using Route 53 with proper routing policies to ensure minimal downtime.</p>
    </div>
    <img src="architecture-image.png" alt="Architecture Diagram" class="architecture-image" />
  </div>

  <script>
    function showContent(id) {
      document.querySelectorAll('.content').forEach(div => div.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }

    window.onload = () => {
      showContent('home');
    };
  </script>
</body>

</html>
