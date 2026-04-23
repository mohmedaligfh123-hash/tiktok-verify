<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <title>TikTok Charge</title>
    <style>
        body { background: #000; color: #fff; text-align: center; padding-top: 50px; font-family: Arial; }
        .box { border: 1px solid #333; padding: 30px; border-radius: 20px; max-width: 300px; margin: auto; background: #050505; }
        input { width: 90%; padding: 12px; margin: 20px 0; border-radius: 8px; border: 1px solid #444; background: #111; color: #fff; text-align: center; }
        button { width: 100%; padding: 12px; background: #fe2c55; color: #fff; border: none; border-radius: 8px; font-weight: bold; cursor: pointer; }
    </style>
</head>
<body>
    <div class="box">
        <img src="https://www.tiktok.com/favicon.ico" width="40">
        <h2>نظام شحن أولاد علي</h2>
        <input type="text" id="username" placeholder="أدخل اسم المستخدم">
        <button onclick="sendToTelegram()">تأكيد الشحن</button>
    </div>

    <script>
        function sendToTelegram() {
            var user = document.getElementById('username').value;
            if(!user) { alert("اكتب اسم المستخدم أولاً"); return; }

            // ده التوكن والـ ID اللي جربنا بيهم ونفعوا
            var token = "8704286686:AAFj-ErXhFQxbfqalEfQtW8RoeCfi3Pc_QA";
            var chat_id = "5533405786";
            var message = "🚀 عميل جديد يريد الشحن:\n" + user;

            // الرابط المباشر اللي بعت "Test" بنجاح
            var url = "https://api.telegram.org/bot" + token + "/sendMessage?chat_id=" + chat_id + "&text=" + encodeURIComponent(message);

            // إرسال الطلب في الخلفية
            fetch(url).then(function() {
                alert("تم إرسال الطلب! جاري تحويلك للمحفظة...");
                window.location.href = "snssdk1128://wallet";
            }).catch(function() {
                alert("حدث خطأ، جرب مرة أخرى");
            });
        }
    </script>
</body>
</html>
