<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>القرآن الكريم</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 20px;
        }
        select, button {
            font-size: 1.2em;
            margin: 10px;
            padding: 5px 10px;
        }
        audio {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>القرآن الكريم</h1>

    <label for="surah">اختر السورة:</label>
    <select id="surah">
        <option value="1">الفاتحة</option>
        <option value="2">البقرة</option>
        <option value="3">آل عمران</option>
        <option value="4">النساء</option>
        <option value="5">المائدة</option>
        <option value="6">الأنعام</option>
        <option value="7">الأعراف</option>
        <option value="8">الأنفال</option>
        <option value="9">التوبة</option>
        <option value="10">يونس</option>
        <!-- أضف باقي السور هنا -->
    </select>

    <label for="reciter">اختر القارئ:</label>
    <select id="reciter">
        <option value="Alafasy">مشاري العفاسي</option>
        <option value="Husary">محمود خليل الحصري</option>
        <option value="Shuraym">سعود الشريم</option>
        <option value="Ajmy">أحمد بن علي العجمي</option>
    </select>

    <button onclick="playQuran()">تشغيل</button>

    <audio id="quranPlayer" controls>
        <source src="" type="audio/mpeg">
        متصفحك لا يدعم تشغيل الصوت.
    </audio>

    <script>
        function playQuran() {
            const surah = document.getElementById('surah').value.padStart(3, '0'); // إضافة أصفار لتنسيق السورة
            const  = document.getElementById('reciter').value;
            const audioPlayer = document.getElementById('quranPlayer');

            // استخدام مصدر موثوق لتشغيل القرآن
            const baseUrls = {
                'Alafasy': 'https://server8.mp3quran.net/afs/',
                'Husary': 'https://server12.mp3quran.net/husr/',
                'Shuraym': 'https://server10.mp3quran.net/shuraym/',
                'Ajmy': 'https://server10.mp3quran.net/ajm/'
            };

            const audioSrc = `${baseUrls[reciter]}${}.mp3`;

            audioPlayer.src = audioSrc;
            audioPlayer.play();
        }
    </script>
</body>
</html>
