<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#130622">
<title>FARJ_8 | My Universe</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:radial-gradient(ellipse at top,#6322a4,#130622 55%,#080411);color:white;font-family:Arial,sans-serif;min-height:100vh}
.wrap{width:92%;max-width:950px;margin:auto}
header{padding:22px 0;border-bottom:1px solid #a855f755;display:flex;justify-content:space-between;flex-wrap:wrap;gap:15px}
.logo{font-size:25px;font-weight:bold;color:#e8c5ff}
nav{display:flex;gap:15px;flex-wrap:wrap}
a{color:#e8c5ff;text-decoration:none}
.hero{text-align:center;padding:75px 10px 45px}
.hero h1{font-size:clamp(55px,12vw,100px);margin:18px 0;text-shadow:0 0 35px #b35cff}
.hero p{color:#d7c5ee;line-height:2}
.btn{display:inline-block;padding:13px 20px;background:linear-gradient(135deg,#a855f7,#6d28d9);border:0;border-radius:12px;color:white;cursor:pointer;font-size:15px}
section{padding:25px 0 35px}
h2{color:#e8c5ff}
.card{background:#ffffff0d;border:1px solid #b86bff55;border-radius:18px;padding:20px;margin:12px 0}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
input,select{width:100%;padding:13px;margin:8px 0 15px;border-radius:10px;border:1px solid #a855f7;background:#10071e;color:white}
label{color:#e8c5ff;font-size:14px}
.muted{color:#cbb8e2;line-height:1.8}
.social a{display:block;padding:15px;border:1px solid #a855f766;border-radius:12px;margin:10px 0;background:#ffffff0a}
footer{text-align:center;padding:30px;color:#bba4d4;border-top:1px solid #a855f744}
</style>
</head>
<body>
<div class="wrap">
<header>
<div class="logo">✦ FARJ_8</div>
<nav>
<a href="#home">الرئيسية</a>
<a href="#links">روابطي</a>
<a href="#downloader">تنزيل الفيديو</a>
<a href="#about">حولي</a>
</nav>
</header>

<main>
<section class="hero" id="home">
<p>✦ MY FANTASY UNIVERSE ✦</p>
<h1>FARJ_8</h1>
<p>عالمي الخاص… حيث يلتقي الخيال بالواقع</p>
<a class="btn" href="#links">اكتشف عالمي ↓</a>
</section>

<section id="links">
<h2>✧ حساباتي الرسمية</h2>
<div class="grid social">
<div class="card">
<h3>👻 Snapchat</h3>
<a href="https://www.snapchat.com/add/f_trwy2018?share_id=yHyJ5a4HThU&locale=ar-EG" target="_blank" rel="noopener">افتح حساب سناب شات ↗</a>
</div>
<div class="card">
<h3>♪ TikTok</h3>
<a href="https://www.tiktok.com/@f8m__11" target="_blank" rel="noopener">افتح حساب تيك توك ↗</a>
</div>
<div class="card">
<h3>◎ Instagram</h3>
<a href="https://www.instagram.com/f8m__11.tk" target="_blank" rel="noopener">افتح حساب إنستغرام ↗</a>
</div>
</div>
</section>

<section id="downloader">
<h2>✦ FARJ Downloader</h2>
<div class="card">
<p class="muted">الصق رابط فيديو تملكه أو لديك إذن بتنزيله. سنحدد المنصة ونفتح الفيديو حتى تستخدم خيارات التنزيل المتاحة.</p>
<form id="downloadForm">
<label for="videoUrl">رابط الفيديو</label>
<input id="videoUrl" type="url" required placeholder="https://...">
<button class="btn" type="submit">تحليل الرابط</button>
</form>
<p id="result" class="muted" aria-live="polite">يدعم TikTok وInstagram وSnapchat.</p>
</div>
</section>

<section id="about">
<h2>✧ أهلاً بك في عالمي</h2>
<div class="card">
<p class="muted">FARJ_8 — مساحة شخصية تجمع الذكريات والروابط والخيال 💜</p>
</div>
</section>
</main>

<footer>✦ FARJ_8 · MY FANTASY UNIVERSE ✦</footer>
</div>

<script>
document.getElementById('downloadForm').addEventListener('submit',function(e){
e.preventDefault();
const input=document.getElementById('videoUrl').value.trim();
const result=document.getElementById('result');
let url;
try{url=new URL(input)}catch(error){
result.textContent='الرابط غير صحيح، حاول مرة ثانية.';
return;
}
if(!['https:','http:'].includes(url.protocol)){
result.textContent='استخدم رابط يبدأ بـ https://';
return;
}
const host=url.hostname.toLowerCase();
let platform='';
if(host.includes('tiktok.com'))platform='TikTok';
else if(host.includes('instagram.com'))platform='Instagram';
else if(host.includes('snapchat.com'))platform='Snapchat';
else{
result.textContent='الرابط ليس من المنصات المدعومة.';
return;
}
result.textContent='تم التعرف على '+platform+'. افتح الفيديو واستخدم خيار التنزيل الرسمي إذا كان متاحاً. لا يمكن ضمان تنزيل كل فيديو أو إزالة العلامة المائية.';
window.open(url.href,'_blank','noopener,noreferrer');
});
</script>
</body>
</html>
