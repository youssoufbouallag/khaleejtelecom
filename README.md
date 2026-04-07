<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khaleej Telecom</title>
    <link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cdefs%3E%3ClinearGradient id='g' x1='0%25' y1='0%25' x2='100%25' y2='100%25'%3E%3Cstop offset='0%25' style='stop-color:%23ff9500'/%3E%3Cstop offset='100%25' style='stop-color:%23ff6b00'/%3E%3C/linearGradient%3E%3C/defs%3E%3Ccircle cx='256' cy='256' r='240' fill='url(%23g)' stroke='%23fff' stroke-width='20'/%3E%3Ccircle cx='256' cy='256' r='180' fill='none' stroke='%23fff' stroke-width='15'/%3E%3Cellipse cx='256' cy='256' rx='180' ry='80' fill='none' stroke='%23fff' stroke-width='12'/%3E%3Cellipse cx='256' cy='256' rx='80' ry='180' fill='none' stroke='%23fff' stroke-width='12'/%3E%3Cline x1='76' y1='256' x2='436' y2='256' stroke='%23fff' stroke-width='12'/%3E%3Cline x1='256' y1='76' x2='256' y2='436' stroke='%23fff' stroke-width='12'/%3E%3Cpath d='M 150 150 Q 256 256 362 150' stroke='%23fff' stroke-width='12' fill='none'/%3E%3Cpath d='M 150 362 Q 256 256 362 362' stroke='%23fff' stroke-width='12' fill='none'/%3E%3C/svg%3E" type="image/svg+xml">
    <style>
        /* سأضع هنا التنسيقات التي أرسلتها أنت */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background: #000; overflow-x: hidden; color: white; }
        .main-container { position: relative; width: 100%; height: 100vh; overflow: hidden; }
        .bg-slider { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; }
        .bg-slide { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-size: cover; background-position: center center; opacity: 0; transition: opacity 1.5s ease-in-out; }
        .bg-slide.active { opacity: 1; }
        .overlay { position: absolute; top: 0; left: 0; width: 100%; height: 100%; background: radial-gradient(ellipse at center, rgba(0,10,40,0.2) 0%, rgba(0,5,20,0.7) 100%); z-index: 2; }
        .content { position: relative; z-index: 10; width: 100%; height: 100%; display: flex; flex-direction: column; align-items: center; padding-top: 10vh; text-align: center; }
        .brand-text { font-size: 3.5rem; font-weight: 600; text-shadow: 0 4px 15px rgba(0,0,0,0.5); }
        .brand-orange { color: #ff9500; }
        .whatsapp-float { position: fixed; bottom: 30px; left: 30px; z-index: 1000; background: #25D366; color: white; width: 60px; height: 60px; border-radius: 50%; display: flex; align-items: center; justify-content: center; text-decoration: none; box-shadow: 0 4px 20px rgba(0,0,0,0.3); }
        
        /* أضف بقية الـ CSS الخاص بك هنا ليعمل التصميم بالكامل */
    </style>
</head>
<body>

<div class="main-container">
    <div class="bg-slider">
        <div class="bg-slide active" style="background-image: url('https://images.unsplash.com/photo-1461664054097-e319867377a0?q=80&w=2000');"></div>
    </div>
    <div class="overlay"></div>
    <div class="content">
        <div class="brand-text">
            <span>khaleej</span><span class="brand-orange">telecom</span><span>.com</span>
        </div>
        <h2 style="margin-top:20px;">رائد في مجال التحول الرقمي</h2>
    </div>
</div>

<a href="https://wa.me/213665817023" class="whatsapp-float" target="_blank">
    <svg viewBox="0 0 24 24" width="35" height="35" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413Z"/></svg>
</a>

</body>
</html>
