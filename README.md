# ZTAP
<!-- link-hub.html
Single-file "link in bio" landing page you can edit and upload to any static host.
Instructions: replace the placeholder image, name, bio, and link URLs. Save as link-hub.html and open in a browser.
-->

<!doctype html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>QRZ — صفحة روابط</title>
  <meta name="description" content="صفحة روابط سريعة - link in bio">
  <style>
    :root{
      --bg1:#0f172a; /* dark blue */
      --bg2:#0b1220;
      --card:#0b1228;
      --accent1:#2563eb; /* blue */ /* purple */
      --accent2:#3b82f6; /* lighter blue */ /* teal */
      --muted:#94a3b8;
      --glass: rgba(255,255,255,0.04);
      font-family: 'Segoe UI', Tahoma, system-ui, -apple-system, 'Noto Naskh Arabic', 'Arial';
    }
    *{box-sizing:border-box}
    body{
      margin:0;min-height:100vh;display:flex;align-items:center;justify-content:center;
      background:radial-gradient(circle at 10% 10%, rgba(124,58,237,0.12), transparent 10%), linear-gradient(180deg,var(--bg1),var(--bg2));
      color:#fff;
    }
    .wrap{width:100%;max-width:480px;padding:28px}
    .card{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:18px;padding:28px;backdrop-filter: blur(6px);box-shadow: 0 8px 30px rgba(2,6,23,0.6);
      border:1px solid rgba(255,255,255,0.03);
    }
    .top{display:flex;flex-direction:column;align-items:center;text-align:center;gap:12px}
    .avatar{width:120px;height:120px;border-radius:50%;overflow:hidden;border:3px solid rgba(255,255,255,0.06)}
    .avatar img{width:100%;height:100%;object-fit:cover;display:block}
    h1{margin:0;font-size:20px}
    p.bio{margin:0;color:var(--muted);font-size:14px}

    .links{margin-top:18px;display:flex;flex-direction:column;gap:12px}
    .link-btn{
      display:flex;align-items:center;gap:12px;padding:12px 14px;border-radius:12px;text-decoration:none;color:#fff;font-weight:600;
      background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);
      transition: transform .15s ease, box-shadow .15s ease;
    }
    .link-btn:hover{transform:translateY(-4px);box-shadow:0 8px 20px rgba(2,6,23,0.5)}
    .link-left{display:inline-flex;align-items:center;justify-content:center;width:44px;height:44px;border-radius:10px;background:linear-gradient(135deg,var(--accent1),var(--accent2));flex-shrink:0}
    .link-left svg{width:20px;height:20px}
    .link-meta{display:flex;flex-direction:column;text-align:right}
    .link-title{font-size:15px}
    .link-sub{font-size:12px;color:var(--muted);margin-top:2px}

    .small{display:flex;justify-content:center;gap:10px;margin-top:14px}
    .pill{padding:6px 10px;border-radius:999px;border:1px solid rgba(255,255,255,0.04);font-size:13px;color:var(--muted)}

    /* responsive */
    @media (max-width:420px){.wrap{padding:18px}.card{padding:18px}.avatar{width:100px;height:100px}}
    /* Light/Dark mode variables */
    body.light{
      --bg1:#f1f5f9;
      --bg2:#e2e8f0;
      --card:#ffffff;
      --muted:#475569;
      color:#0f172a;
    }
    .mode-btn{
      margin-top:10px;padding:6px 14px;border-radius:999px;font-size:13px;cursor:pointer;
      background:var(--glass);border:1px solid rgba(255,255,255,0.15);color:inherit;
    }
    .fade-in{animation:fade .6s ease forwards;opacity:0}
    @keyframes fade{to{opacity:1}}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="card">
      <div class="top">
        <div class="avatar fade-in">
          <!-- Enhanced QRZ Logo -->
          <svg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:100%">
            <defs>
              <linearGradient id="g1" x1="0" x2="1" y1="0" y2="1">
                <stop offset="0%" stop-color="#2563eb"/>
                <stop offset="100%" stop-color="#3b82f6"/>
              </linearGradient>
            </defs>
            <circle cx="100" cy="100" r="90" fill="url(#g1)"/>
            <text x="50%" y="57%" text-anchor="middle" font-size="72" fill="white" font-family="Segoe UI, Arial" dy="10">QRZ</text>
          </svg>
        </div>
        <h1 id="name">QRZ</h1>
        <p class="bio" id="bio">نبذة قصيرة عنك — مثلاً: مصمم، مبرمج، أو صاحب محتوى</p>

        <div class="small fade-in">
          <div class="pill" id="location">القاهرة • مصر</div>
          <div class="pill" id="role">مطور ويب</div>
        </div>
        <button class="mode-btn" id="modeToggle">تغيير الثيم</button>
          <div class="pill" id="role">مطور ويب</div>
        </div>
      </div>

      <div class="links" id="links">
        <!-- Example link items. Replace href targets with your real URLs -->
        <a class="link-btn" href="https://instagram.com/" target="_blank" rel="noopener noreferrer">
          <span class="link-left" aria-hidden>
            <!-- Instagram SVG -->
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="24" height="24" rx="5" fill="white" fill-opacity="0"/><path d="M7 2h10a5 5 0 015 5v10a5 5 0 01-5 5H7a5 5 0 01-5-5V7a5 5 0 015-5z" stroke="white" stroke-opacity="0.95" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <span class="link-meta">
            <span class="link-title">Instagram</span>
            <span class="link-sub">تابعني على الإنستجرام</span>
          </span>
        </a>

        <a class="link-btn" href="https://wa.me/201234567890" target="_blank" rel="noopener noreferrer">
          <span class="link-left" aria-hidden>
            <!-- WhatsApp SVG -->
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><circle cx="12" cy="12" r="10" stroke="white" stroke-opacity="0.95" stroke-width="1.2"/><path d="M17 7a6 6 0 00-10 4c0 1.1.3 2.1.8 3L7 18l3.1-.8A5.9 5.9 0 0017 7z" stroke="white" stroke-opacity="0.95" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <span class="link-meta">
            <span class="link-title">واتساب</span>
            <span class="link-sub">ابدأ محادثة مباشرة</span>
          </span>
        </a>

        <a class="link-btn" href="https://youtube.com/" target="_blank" rel="noopener noreferrer">
          <span class="link-left" aria-hidden>
            <!-- YouTube SVG -->
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="24" height="24" rx="4" stroke="white" stroke-opacity="0.95" stroke-width="1.2"/><path d="M10 9l5 3-5 3V9z" stroke="white" stroke-opacity="0.95" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <span class="link-meta">
            <span class="link-title">قناتي على يوتيوب</span>
            <span class="link-sub">فيديوهات تعليمية ومحتوى جديد</span>
          </span>
        </a>

        <!-- Copy profile link button -->
        <button class="link-btn" id="copy-btn" title="انسخ رابط الصفحة">
          <span class="link-left" aria-hidden>
            <!-- Link icon -->
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M10 14a3 3 0 004.24 0l3.02-3.02a3 3 0 00-4.24-4.24L12 9.76" stroke="white" stroke-opacity="0.95" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/><path d="M14 10a3 3 0 00-4.24 0L6.74 13.02a3 3 0 004.24 4.24L12 14.24" stroke="white" stroke-opacity="0.95" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
          </span>
          <span class="link-meta">
            <span class="link-title">انسخ رابط صفحتي</span>
            <span class="link-sub" id="copy-sub">مشاركة سهلة</span>
          </span>
        </button>
      </div>

    </div>
  </div>

  <script>
    // Simple JS to make 'copy link' work and show temporary feedback
    (function(){
      const copyBtn = document.getElementById('copy-btn');
      const copySub = document.getElementById('copy-sub');
      copyBtn.addEventListener('click', async function(){
        try{
          const url = window.location.href;
          await navigator.clipboard.writeText(url);
          copySub.textContent = 'تم النسخ!';
          setTimeout(()=> copySub.textContent = 'مشاركة سهلة', 2500);
        }catch(e){
          // fallback
          const input = document.createElement('input');
          document.body.appendChild(input);
          input.value = window.location.href;
          input.select();
          try{document.execCommand('copy'); copySub.textContent = 'تم النسخ!'}catch(err){copySub.textContent = 'انسخ يدويًا'}
          document.body.removeChild(input);
          setTimeout(()=> copySub.textContent = 'مشاركة سهلة', 2500);
        }
      });

      // Optional: replace content dynamically if you want to prefill from JS
      // document.getElementById('name').textContent = 'Mahmoud Zine';
      // document.getElementById('bio').textContent = 'مطور ويب ومصمم واجهات';

    })();
    // Theme toggle
    const modeToggle=document.getElementById('modeToggle');
    modeToggle.addEventListener('click',()=>{
      document.body.classList.toggle('light');
    });

  </script>
</body>
</html>
