<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nguyễn Minh Nhật - Danford IT Applicant</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    :root { --primary: #0A66C2; --accent: #FF6B35; --dark: #1a1a1a; }
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: 'Inter', sans-serif;
      background: #f8f9fa;
      color: var(--dark); line-height: 1.7;
    }
    .container { max-width: 1000px; margin: 0 auto; padding: 2rem; }

    .lang-switch {
      position: fixed; top: 1rem; right: 1rem; z-index: 1000;
      background: white; padding: 0.5rem; border-radius: 1rem;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    }
    .lang-switch button {
      background: none; border: none; padding: 0.5rem 1rem;
      font-weight: 600; cursor: pointer; border-radius: 0.5rem;
    }
    .lang-switch button.active { background: var(--primary); color: white; }

    header {
      text-align: center; padding: 3rem 0 2rem; background: white;
      border-radius: 1.5rem; margin-bottom: 2rem;
      box-shadow: 0 10px 25px rgba(0,0,0,0.05);
    }
    .avatar {
      width: 150px; height: 150px; border-radius: 50%;
      object-fit: cover; border: 6px solid var(--primary);
      margin-bottom: 1rem; cursor: zoom-in; transition: 0.3s;
    }
    .avatar:hover { transform: scale(1.05); }
    h1 { font-size: 2.8rem; color: var(--primary); margin-bottom: 0.5rem; }
    .tagline { font-size: 1.3rem; color: #444; font-weight: 500; }

    nav {
      display: flex; justify-content: center; gap: 1.5rem; margin: 2rem 0;
      flex-wrap: wrap; background: white; padding: 1rem;
      border-radius: 1rem; box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    }
    nav a {
      color: var(--dark); text-decoration: none; font-weight: 600;
      padding: 0.7rem 1.3rem; border-radius: 0.5rem; transition: 0.3s;
    }
    nav a:hover { background: var(--primary); color: white; }

    section {
      background: white; padding: 2rem; border-radius: 1.5rem;
      margin-bottom: 2rem; box-shadow: 0 10px 25px rgba(0,0,0,0.05);
    }
    h2 {
      color: var(--primary); margin-bottom: 1rem; font-size: 2rem;
      position: relative; padding-bottom: 0.5rem;
    }
    h2::after {
      content: ''; position: absolute; left: 0; bottom: 0;
      width: 60px; height: 4px; background: var(--accent); border-radius: 2px;
    }

    .intro {
      background: linear-gradient(120deg, #e3f2fd 0%, #bbdefb 100%);
      padding: 1.5rem; border-radius: 1rem; margin-bottom: 1.5rem;
      font-size: 1.1rem; line-height: 1.8; text-align: center;
      border-left: 5px solid var(--primary);
    }

    .timeline {
      position: relative; padding-left: 2rem;
    }
    .timeline::before {
      content: ''; position: absolute; left: 10px; top: 0; bottom: 0;
      width: 4px; background: var(--primary); border-radius: 2px;
    }
    .timeline-item {
      position: relative; margin-bottom: 1.5rem; padding-left: 2rem;
      font-size: 1.05rem;
    }
    .timeline-item::before {
      content: ''; position: absolute; left: -8px; top: 8px;
      width: 16px; height: 16px; background: var(--primary);
      border: 4px solid white; border-radius: 50%; box-shadow: 0 0 0 4px var(--primary);
    }

    .grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; }
    .card { background: #f8f9fa; padding: 1.5rem; border-radius: 1rem; border: 1px solid #e9ecef; text-align: center; }
    .card img {
      width: 100%; height: 180px; object-fit: cover; border-radius: 0.5rem;
      margin-bottom: 1rem; cursor: zoom-in; transition: 0.3s;
    }
    .card img:hover { transform: scale(1.03); }

    .project {
      display: flex; gap: 1rem; align-items: center; padding: 1rem;
      background: #f0f8ff; border-radius: 1rem; border-left: 5px solid var(--primary);
    }
    .project img {
      width: 80px; height: 80px; object-fit: cover; border-radius: 0.5rem;
      cursor: zoom-in; transition: 0.3s;
    }
    .project img:hover { transform: scale(1.1); }
    .project a { color: var(--primary); font-weight: 600; text-decoration: none; }

    .highlight {
      background: #fff8e1; padding: 1.2rem; border-radius: 1rem;
      border-left: 5px solid var(--accent); margin: 1rem 0; font-style: italic;
    }

    .lightbox {
      display: none; position: fixed; z-index: 9999; left: 0; top: 0;
      width: 100%; height: 100%; background: rgba(0,0,0,0.9);
      justify-content: center; align-items: center; cursor: zoom-out;
    }
    .lightbox img {
      max-width: 90%; max-height: 90%; border: 5px solid white; border-radius: 1rem;
      box-shadow: 0 0 30px rgba(255,255,255,0.3);
    }
    .lightbox.active { display: flex; }

    [lang="en"] { display: none; }
    body.en [lang="vi"] { display: none; }
    body.en [lang="en"] { display: block; }

    .play-btn {
      display: inline-block; margin-top: 0.5rem; padding: 0.5rem 1rem;
      background: var(--primary); color: white; border-radius: 0.5rem;
      font-weight: 600; text-decoration: none; transition: 0.3s;
    }
    .play-btn:hover { background: #08529a; transform: scale(1.05); }
  </style>
</head>
<body>
  <div class="lang-switch">
    <button onclick="switchLang('vi')" class="active">VI</button>
    <button onclick="switchLang('en')">EN</button>
  </div>

  <div class="container">
    <header>
      <img src="https://i.postimg.cc/BtGYt9vb/Gemini-Generated-Image-eze5bzeze5bzeze5.png" alt="Nguyễn Minh Nhật" class="avatar" onclick="openLightbox(this.src)">
      <h1>Nguyễn Minh Nhật</h1>
      <p class="tagline" lang="vi">Sinh viên CNTT | Ứng viên Danford 2026</p>
      <p class="tagline" lang="en">IT Student | Danford Applicant 2026</p>
    </header>

    <section id="about">
      <h2 lang="vi">Giới thiệu bản thân</h2>
      <h2 lang="en">About Me</h2>
      <div class="intro" lang="vi">
        Tôi là Nguyễn Minh Nhật – một sinh viên CNTT đam mê công nghệ và khát khao vươn ra thế giới. 
        Từ nhỏ, tôi đã mơ ước được học tập tại Úc để trải nghiệm môi trường giáo dục tiên tiến và phát triển toàn diện. 
        Với nền tảng học tập vững chắc, kỹ năng lập trình thực tế và tinh thần trách nhiệm cộng đồng, 
        tôi tin mình sẽ là ứng viên xuất sắc cho chương trình tại <strong>Danford Higher Education</strong>.
      </div>
      <div class="intro" lang="en">
        I am Minh Nhat Nguyen – an IT student passionate about technology and eager to explore the world. 
        Since childhood, I’ve dreamed of studying in Australia to experience advanced education and grow holistically. 
        With a strong academic background, practical coding skills, and a commitment to community, 
        I believe I am an outstanding candidate for <strong>Danford Higher Education</strong>.
      </div>
    </section>

    <section id="education">
      <h2 lang="vi">Hành trình học tập</h2>
      <h2 lang="en">Education Journey</h2>
      <div class="timeline">
        <div class="timeline-item"><strong lang="vi">Mẫu giáo</strong><strong lang="en">Preschool</strong> — 2008–2011</div>
        <div class="timeline-item"><strong lang="vi">Tiểu học An Viên</strong><strong lang="en">An Vien Primary School</strong> — 2011–2016</div>
        <div class="timeline-item"><strong lang="vi">THCS Trịnh Hoài Đức</strong><strong lang="en">Trinh Hoai Duc Secondary School</strong> — 2016–2020</div>
        <div class="timeline-item"><strong lang="vi">THPT Ngô Sĩ Liên</strong><strong lang="en">Ngo Si Lien High School</strong> — 2020–2023</div>
        <div class="timeline-item"><strong lang="vi">ĐH Quốc tế (1 kỳ)</strong><strong lang="en">International University (1 semester)</strong> — 2023</div>
        <div class="timeline-item"><strong lang="vi">Gap year + EAP</strong><strong lang="en">Gap Year + EAP Program</strong> — 2024</div>
        <div class="timeline-item"><strong lang="vi">ĐH Lạc Hồng</strong><strong lang="en">Lac Hong University</strong> — 2025–nay</div>
      </div>
    </section>

    <section id="story">
      <h2 lang="vi">Hành trình ước mơ du học</h2>
      <h2 lang="en">My Dream Journey</h2>
      <div class="highlight" lang="vi">Từ khi còn nhỏ, tôi đã luôn ước mơ được đi du học để khám phá thế giới, trải nghiệm những nền văn hóa khác nhau và mở rộng tầm nhìn của mình.</div>
      <div class="highlight" lang="en">Since childhood, I have dreamed of studying abroad to explore the world, experience diverse cultures, and broaden my horizons.</div>
      <div class="highlight" lang="vi">Tôi tin rằng việc học tập ở nước ngoài không chỉ giúp tôi tiếp thu kiến thức mới mà còn rèn luyện tính độc lập, khả năng thích nghi và tư duy toàn cầu.</div>
      <div class="highlight" lang="en">I believe studying overseas cultivates independence, adaptability, and global thinking.</div>
      <div class="highlight" lang="vi">Niềm đam mê với Công nghệ Thông tin bắt đầu khi tôi nhận ra công nghệ có thể kết nối con người và thay đổi cuộc sống. Tôi đặc biệt quan tâm đến lập trình, phân tích dữ liệu và AI.</div>
      <div class="highlight" lang="en">My passion for IT began when I realized technology connects people and transforms lives. I am drawn to programming, data analysis, and AI.</div>
      <div class="highlight" lang="vi">Chương trình tại Danford sẽ giúp tôi xây dựng nền tảng vững chắc cả về học thuật lẫn thực hành.</div>
      <div class="highlight" lang="en">Danford’s program will provide me with a strong academic and practical foundation.</div>
      <div class="highlight" lang="vi">Sau khi tốt nghiệp, tôi mong muốn trở về Việt Nam để đóng góp vào ngành công nghệ thông tin.</div>
      <div class="highlight" lang="en">Upon graduation, I aspire to return to Vietnam and contribute to the IT industry.</div>
      <div class="highlight" lang="vi">Mục tiêu lớn nhất là mang tri thức toàn cầu về phục vụ quê hương.</div>
      <div class="highlight" lang="en">My ultimate goal is to apply global knowledge to serve my homeland.</div>
    </section>

    <section id="activities">
      <h2 lang="vi">Hoạt động ngoại khóa</h2>
      <h2 lang="en">Extracurricular Activities</h2>
      <div class="grid">
        <div class="card">
          <img src="https://i.postimg.cc/K19wg9HJ/4d065575-384a-4c6c-8acc-6f51cb8a1a6c.jpg" alt="CLB Bóng đá" onclick="openLightbox(this.src)">
          <p lang="vi"><strong>CLB Bóng đá trường</strong> – Vô địch khu vực</p>
          <p lang="en"><strong>School Football Club</strong> – District Champion</p>
        </div>
        <div class="card">
          <img src="https://i.postimg.cc/9RyL11Ly/562dfdbb-241c-46f0-af7c-4c612ad15fa6.jpg" alt="Văn nghệ" onclick="openLightbox(this.src)">
          <p lang="vi"><strong>Văn nghệ trường</strong> – Biểu diễn 5 lần</p>
          <p lang="en"><strong>School Performances</strong> – 5 shows</p>
        </div>
      </div>
    </section>

    <section id="projects">
      <h2 lang="vi">Dự án nhỏ trên web</h2>
      <h2 lang="en">Small Web Projects</h2>

      <div class="grid">
        <div class="project">
          <img src="https://i.postimg.cc/LYtzJ3k7/Gemini-Generated-Image-yvgk1dyvgk1dyvgk.png" alt="Neon Car Dodge PRO" onclick="openLightbox(this.src)">
          <div>
            <h3 lang="vi">Neon Car Dodge PRO</h3>
            <h3 lang="en">Neon Car Dodge PRO</h3>
            <p lang="vi"><strong>Game né xe neon 3D</strong> – Điều khiển xe tránh chướng ngại vật, tăng tốc dần.</p>
            <p lang="en"><strong>3D neon car dodging</strong> – Steer to avoid obstacles, speed increases.</p>
            <p lang="vi" style="font-size:0.9rem; color:#0A66C2; margin:0.5rem 0;">
              <strong>Tech:</strong> HTML5 Canvas, JavaScript, 3D perspective, particles, sound
            </p>
            <p lang="en" style="font-size:0.9rem; color:#0A66C2; margin:0.5rem 0;">
              <strong>Tech:</strong> HTML5 Canvas, JavaScript, 3D perspective, particles, sound
            </p>
            <a href="game_dua_xe.html" target="_blank" class="play-btn">
              Chơi ngay
            </a>
          </div>
        </div>

        <div class="project">
          <img src="https://i.postimg.cc/H8W7VDk3/Gemini-Generated-Image-eiw54seiw54seiw5.png" alt="Galaxy Shooter" onclick="openLightbox(this.src)">
          <div>
            <h3 lang="vi">Galaxy Shooter - Bắn Gà Vũ Trụ</h3>
            <h3 lang="en">Galaxy Shooter - Space Chicken</h3>
            <p lang="vi"><strong>Game bắn gà không gian</strong> – Bắn hạ kẻ địch, né đạn, thu power-up.</p>
            <p lang="en"><strong>Space chicken shooter</strong> – Shoot enemies, dodge bullets, collect power-ups.</p>
            <p lang="vi" style="font-size:0.9rem; color:#0A66C2; margin:0.5rem 0;">
              <strong>Tech:</strong> HTML5 Canvas, JavaScript, collision, waves, particles
            </p>
            <p lang="en" style="font-size:0.9rem; color:#0A66C2; margin:0.5rem 0;">
              <strong>Tech:</strong> HTML5 Canvas, JavaScript, collision, waves, particles
            </p>
            <a href="game_ban_ga.html" target="_blank" class="play-btn">
              Chơi ngay
            </a>
          </div>
        </div>
      </div>
    </section>

    <section id="contact">
      <h2 lang="vi">Liên hệ</h2>
      <h2 lang="en">Contact</h2>
      <p>
        <strong>Email:</strong> <a href="mailto:minhnhat362005@gmail.com">minhnhat362005@gmail.com</a><br>
        <strong>Phone:</strong> +84 966 520 902
      </p>
    </section>
  </div>

  <div class="lightbox" id="lightbox" onclick="closeLightbox()">
    <img id="lightbox-img" src="" alt="Zoomed Image">
  </div>

  <script>
    function switchLang(lang) {
      document.body.className = lang;
      document.querySelectorAll('.lang-switch button').forEach(btn => {
        btn.classList.toggle('active', btn.textContent.trim() === (lang === 'vi' ? 'VI' : 'EN'));
      });
    }

    function openLightbox(src) {
      const lightbox = document.getElementById('lightbox');
      const img = document.getElementById('lightbox-img');
      img.src = src;
      lightbox.classList.add('active');
    }

    function closeLightbox() {
      document.getElementById('lightbox').classList.remove('active');
    }

    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') closeLightbox();
    });
  </script>
</body>
</html>
