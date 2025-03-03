# -
조랭의 모든 것
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
  <title>조랭을 소개한다</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }
    body {
      background-color: #f4f4f4;
      text-align: center;
    }
    .section {
      opacity: 0;
      transform: translateY(50px);
      transition: opacity 1s ease-out, transform 1s ease-out;
      padding: 100px 20px;
    }
    .section.visible {
      opacity: 1;
      transform: translateY(0);
    }
    .intro {
      background: #3498db;
      color: white;
      padding: 150px 20px;
      font-size: 24px;
    }
    .gallery img {
      width: 200px;
      margin: 10px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div class="section intro">
    <h1>조랭 is king</h1>
    <p>동희 엉덩이 동희</p>
  </div>
  
  <div class="section">
    <h2>조랭의 특징</h2>
    <p>조랭조랭함.</p>
  </div>
  
  <div class="section">
    <h2>조랭조랭.</h2>
    <p>하개찌따</p>
  </div>
  
  <div class="section gallery">
    <h2>사진 갤러리</h2>
    <img src="![image](https://github.com/user-attachments/assets/7694c5bd-b39a-410c-85bc-0e7380981e39)
" alt="친구 사진 1">
    <img src="![image](https://github.com/user-attachments/assets/f9617b48-0888-4b28-b98e-f3b80c4f006f)
" alt="친구 사진 2">
  </div>
  
  <div class="section">
    <h2>조랭이야기</h2>
    <p>통일초등학교 졸업</p>
  </div>
  
  <script>
    document.addEventListener("DOMContentLoaded", () => {
      const sections = document.querySelectorAll(".section");
      
      const observer = new IntersectionObserver((entries, observer) => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.classList.add("visible");
          }
        });
      }, { threshold: 0.3 });
      
      sections.forEach(section => {
        observer.observe(section);
      });
    });
  </script>
</body>
</html>
