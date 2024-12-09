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
        <option value="11">هود</option>
        <option value="12">يوسف</option>
        <option value="13">الرعد</option>
        <option value="14">إبراهيم</option>
        <option value="15">الحجر</option>
        <option value="16">النحل</option>
        <option value="17">الإسراء</option>
        <option value="18">الكهف</option>
        <option value="19">مريم</option>
        <option value="20">طه</option>
        <option value="21">الأنبياء</option>
        <option value="22">الحج</option>
        <option value="23">المؤمنون</option>
        <option value="24">النور</option>
        <option value="25">الفرقان</option>
        <option value="26">الشعراء</option>
        <option value="27">النمل</option>
        <option value="28">القصص</option>
        <option value="29">العنكبوت</option>
        <option value="30">الروم</option>
        <option value="31">لقمان</option>
        <option value="32">السجدة</option>
        <option value="33">الأحزاب</option>
        <option value="34">سبأ</option>
        <option value="35">فاطر</option>
        <option value="36">يس</option>
        <option value="37">الصافات</option>
        <option value="38">ص</option>
        <option value="39">الزمر</option>
        <option value="40">غافر</option>
        <option value="41">فصلت</option>
        <option value="42">الشورى</option>
        <option value="43">الزخرف</option>
        <option value="44">الدخان</option>
        <option value="45">الجاثية</option>
        <option value="46">الأحقاف</option>
        <option value="47">محمد</option>
        <option value="48">الفتح</option>
        <option value="49">الحجرات</option>
        <option value="50">ق</option>
        <option value="51">الذاريات</option>
        <option value="52">الطور</option>
        <option value="53">النجم</option>
        <option value="54">القمر</option>
        <option value="55">الرحمن</option>
        <option value="56">الواقعة</option>
        <option value="57">الحديد</option>
        <option value="58">المجادلة</option>
        <option value="59">الحشر</option>
        <option value="60">الممتحنة</option>
        <option value="61">الصف</option>
        <option value="62">الجمعة</option>
        <option value="63">المنافقون</option>
        <option value="64">التغابن</option>
        <option value="65">الطلاق</option>
        <option value="66">التحريم</option>
        <option value="67">الملك</option>
        <option value="68">القلم</option>
        <option value="69">الحاقة</option>
        <option value="70">المعارج</option>
        <option value="71">نوح</option>
        <option value="72">الجن</option>
        <option value="73">المزمل</option>
        <option value="74">المدثر</option>
        <option value="75">القيامة</option>
        <option value="76">الإنسان</option>
        <option value="77">المرسلات</option>
        <option value="78">النبأ</option>
        <option value="79">النازعات</option>
        <option value="80">عبس</option>
        <option value="81">التكوير</option>
        <option value="82">الإنفطار</option>
        <option value="83">المطففين</option>
        <option value="84">الإنشقاق</option>
        <option value="85">البروج</option>
        <option value="86">الطارق</option>
        <option value="87">الأعلى</option>
        <option value="88">الغاشية</option>
        <option value="89">الفجر</option>
        <option value="90">البلد</option>
        <option value="91">الشمس</option>
        <option value="92">الليل</option>
        <option value="93">الضحى</option>
        <option value="94">الشرح</option>
        <option value="95">التين</option>
        <option value="96">العلق</option>
        <option value="97">القدر</option>
        <option value="98">البينة</option>
        <option value="99">الزلزلة</option>
        <option value="100">العاديات</option>
        <option value="101">القارعة</option>
        <option value="102">التكاثر</option>
        <option value="103">العصر</option>
        <option value="104">الهمزة</option>
        <option value="105">الفيل</option>
        <option value="106">قريش</option>
        <option value="107">الماعون</option>
        <option value="108">الكوثر</option>
        <option value="109">الكافرون</option>
        <option value="110">النصر</option>
        <option value="111">المسد</option>
        <option value="112">الإخلاص</option>
        <option value="113">الفلق</option>
        <option value="114">الناس</option>
    </select>

    <label for="reciter">اختر القارئ:</label>
    <select id="reciter">
        <option value="Alafasy">مشاري العفاسي</option>
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
            const reciter = document.getElementById('reciter').value;
            const audioPlayer = document.getElementById('quranPlayer');

            // استخدام مصدر موثوق لتشغيل القرآن
            const baseUrls = {
                'Alafasy': 'https://server8.mp3quran.net/afs/',
                'Ajmy': 'https://server10.mp3quran.net/ajm/'
            };

            const audioSrc = `${baseUrls[reciter]}${surah}.mp3`;

            audioPlayer.src = audioSrc;
            audioPlayer.play();
        }
    </script>
</body>
</html>
