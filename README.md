
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>FARJ_8 | عالم الخيال</title>
<style>
*{box-sizing:border-box}
body{margin:0;background:radial-gradient(ellipse at top,#5720a8,#160b30 50%,#080610);color:white;font-family:Arial,sans-serif;min-height:100vh}
header{text-align:center;padding:55px 15px 30px}
h1{font-size:clamp(48px,12vw,90px);margin:20px 0;color:#fff;text-shadow:0 0 15px #c084fc,0 0 45px #9333ea}
header p{color:#dfc7ff;line-height:1.9}
nav{display:flex;justify-content:center;gap:10px;flex-wrap:wrap}
a,button{color:white;text-decoration:none;background:#ffffff10;border:1px solid #b67aff70;border-radius:12px;padding:12px 18px;cursor:pointer}
a:hover,button:hover{background:#9333ea}
main{max-width:900px;margin:auto;padding:15px}
section{margin:25px 0;padding:24px;background:#ffffff09;border:1px solid #b67aff45;border-radius:22px;box-shadow:0 0 30px #781bba12}
h2{color:#d8b4fe}
p{line-height:1.8;color:#e6d9ff}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(200px,1fr));gap:12px}
.item{padding:20px;background:#6d28d922;border:1px solid #c084fc50;border-radius:15px;overflow-wrap:anywhere}
input{width:100%;margin:7px 0 12px;padding:12px;border-radius:10px;background:#10091f;color:white;border:1px solid #a855f7}
footer{text-align:center;padding:30px;color:#bda4dd}
</style>
</head>
<body>
<header>
<div>✦ WELCOME TO MY UNIVERSE ✦</div>
<h1>FARJ_8</h1>
<p>عالمي الخاص، حيث يلتقي الخيال بالفخامة 💜<br>صور • فيديوهات • روابط • ذكرياتي</p>
<nav>
<a href="#about">عن عالمي</a>
<a href="#gallery">المعرض</a>
<a href="#links">روابطي</a>
</nav>
</header>
<main>
<section id="about">
<h2>✧ أهلاً بك في عالمي</h2>
<p>مكان خاص يجمع الأشياء التي أحبها، بتصميم بنفسجي مستقبلي ولمسة من الخيال.</p>
</section>
<section id="gallery">
<h2>✧ معرض الصور والفيديوهات</h2>
<p>أضف رابط صورة أو فيديو عام حتى تعرضه هنا.</p>
<form id="mediaForm">
<input id="mediaTitle" placeholder="اسم الصورة أو الفيديو" required>
<input id="mediaUrl" type="url" placeholder="رابط الصورة أو الفيديو" required>
<button>＋ إضافة إلى المعرض</button>
</form>
<div class="grid" id="galleryItems"></div>
</section>
<section id="links">
<h2>✧ بواباتي إلى العالم</h2>
<form id="linkForm">
<input id="linkTitle" placeholder="اسم الموقع أو الحساب" required>
<input id="linkUrl" type="url" placeholder="رابط الموقع الكامل https://..." required>
<button>＋ إضافة رابط</button>
</form>
<div class="grid" id="linkItems"></div>
</section>
</main>
<footer>✦ FARJ_8 · MY FANTASY UNIVERSE ✦</footer>
<script>
const g=document.getElementById('galleryItems'),l=document.getElementById('linkItems');
function valid(v){try{return ['http:','https:'].includes(new URL(v).protocol)}catch(e){return false}}
document.getElementById('mediaForm').onsubmit=e=>{
e.preventDefault();let t=document.getElementById('mediaTitle').value,u=document.getElementById('mediaUrl').value;
if(!valid(u))return alert('تأكد من صحة الرابط');
let d=document.createElement('div');d.className='item';
if(/\.(mp4|webm|ogg)(\?.*)?$/i.test(u)){let v=document.createElement('video');v.src=u;v.controls=true;v.style.width='100%';d.append(v)}
else{let im=document.createElement('img');im.src=u;im.alt=t;im.style.width='100%';d.append(im)}
let p=document.createElement('p');p.textContent=t;d.append(p);g.prepend(d);e.target.reset()};
document.getElementById('linkForm').onsubmit=e=>{
e.preventDefault();let t=document.getElementById('linkTitle').value,u=document.getElementById('linkUrl').value;
if(!valid(u))return alert('تأكد من صحة الرابط');
let d=document.createElement('div');d.className='item';let a=document.createElement('a');a.href=u;a.target='_blank';a.rel='noopener noreferrer';a.textContent='✧ '+t+' ↗';d.append(a);l.prepend(d);e.target.reset()};
</script>
</body>
</html>
# farj_8
