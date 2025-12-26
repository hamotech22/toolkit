# 🚀 Tailwind CSS – Structure & Quick Cheatsheet

## 🧱 الشكل العام لأي صفحة (Base Structure)

ده أبسط هيكل HTML ممكن تبدأ بيه أي مشروع Tailwind.
- `body` فيه ألوان عامة للموقع
- `container` بيوسّط المحتوى
- `p-4` بيدي مسافة داخلية

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Tailwind App</title>
</head>
<body class="bg-gray-100 text-gray-800">

  <div class="container mx-auto p-4">
    <h1 class="text-3xl font-bold text-center mb-4">
      Hello Tailwind
    </h1>

    <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded">
      Click Me
    </button>
  </div>

</body>
</html>
```

---

## 🔹 أهم الكلاسات (مختصر مفيد)

الكلاسات دي هي أكتر حاجة هتستخدمها يوميًا وانت شغال Tailwind.

### 🎨 الألوان
بتستخدمها لتغيير لون الخلفية، النص، أو البوردر.
```txt
bg-red-500
text-gray-700
border-blue-300
```

---

### 📏 المسافات (Padding & Margin)
بتتحكم في المسافات الداخلية والخارجية للعناصر.
```txt
p-4        → padding
px-4 py-2  → padding أفقي / رأسي
m-4        → margin
mt-2 mb-6 → margin top / bottom
```

---

### 🧱 العرض والارتفاع
بتحدد حجم العنصر بالنسبة للشاشة أو العنصر الأب.
```txt
w-full
w-1/2
h-screen
max-w-lg
```

---

### 🖋️ النصوص
بتتحكم في حجم الخط، سمكه، ومحاذاته.
```txt
text-sm | text-lg | text-3xl
font-bold | font-medium
text-center | text-right
uppercase
```

---

### 🧭 Flexbox (مهم جدًا)
بيستخدم لترتيب العناصر جنب بعض أو فوق بعض بسهولة.
```txt
flex
items-center
justify-between
justify-center
gap-4
```

**مثال:**
```html
<div class="flex items-center justify-between">
  <span>Logo</span>
  <button>Login</button>
</div>
```

---

### 📐 Grid
مناسب لتقسيم الصفحة أو عرض كروت بشكل منظم.
```txt
grid
grid-cols-3
gap-4
```

---

### 🟦 الحدود والظل
بتدي شكل أنضف وعمق للعناصر زي الكروت.
```txt
rounded
rounded-lg
border
shadow
shadow-md
```

---

### 🎭 Hover & Transition
بتستخدم لتأثيرات الحركة عند المرور بالماوس.
```txt
hover:bg-blue-600
transition
duration-300
```

---

### 📱 Responsive (مهم)
بتخلي الموقع شكله مظبوط على الموبايل والتابلت والديسكتوب.
```txt
sm:text-sm
md:text-lg
lg:text-2xl
xl:grid-cols-4
```

**مثال:**
```html
<h1 class="text-lg md:text-2xl lg:text-4xl">
  Responsive Text
</h1>
```

---

## 🃏 مثال كارت جاهز (Reusable Card)
كارد بسيط تقدر تعيد استخدامه في أي مشروع (منتجات – مستخدمين – مقالات).

```html
<div class="bg-white rounded-lg shadow p-4 max-w-sm">
  <h2 class="text-xl font-bold mb-2">Card Title</h2>
  <p class="text-gray-600 mb-4">
    This is a simple card using Tailwind.
  </p>
  <button class="bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">
    Action
  </button>
</div>
```

---






# 🧱 Tailwind CSS – Grid Card Component

هذا مثال كارت (Card) مقسم باستخدام **Grid** في Tailwind CSS – جاهز للاستخدام داخل أي مشروع.

> ضع الكود داخل ملف HTML أو داخل أي صفحة Tailwind.

---

## ✨ Preview

كروت مصفوفة في Grid – متوافقة مع الريسبونسيف (موبايل – تابلت – لابتوب)

---

## 📦 الكود

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 p-6">
  <!-- Card 1 -->
  <div class="bg-white shadow-lg rounded-xl p-6 hover:shadow-xl transition">
    <img src="https://via.placeholder.com/300x180" class="rounded-lg mb-4" />
    <h2 class="text-xl font-bold mb-2">عنوان الكارت الأول</h2>
    <p class="text-gray-600 text-sm mb-4">وصف بسيط للكارت باستخدام Tailwind CSS.</p>
    <button class="bg-blue-500 hover:bg-blue-600 text-white px-4 py-2 rounded-lg">اقرأ المزيد</button>
  </div>

  <!-- Card 2 -->
  <div class="bg-white shadow-lg rounded-xl p-6 hover:shadow-xl transition">
    <img src="https://via.placeholder.com/300x180" class="rounded-lg mb-4" />
    <h2 class="text-xl font-bold mb-2">عنوان الكارت الثاني</h2>
    <p class="text-gray-600 text-sm mb-4">كلام إضافي توضيحي عن الكارت.</p>
    <button class="bg-green-500 hover:bg-green-600 text-white px-4 py-2 rounded-lg">ابدأ الآن</button>
  </div>

  <!-- Card 3 -->
  <div class="bg-white shadow-lg rounded-xl p-6 hover:shadow-xl transition">
    <img src="https://via.placeholder.com/300x180" class="rounded-lg mb-4" />
    <h2 class="text-xl font-bold mb-2">عنوان الكارت الثالث</h2>
    <p class="text-gray-600 text-sm mb-4">وصف مختصر للكارت الثالث.</p>
    <button class="bg-purple-500 hover:bg-purple-600 text-white px-4 py-2 rounded-lg">تواصل معنا</button>
  </div>
</div>
```

---

## 🎯 ملاحظات

* الكود يستخدم Tailwind CDN – لا حاجة لأي إعداد إضافي.
* تقدر تغيّر الصور – النصوص – الألوان حسب ذوقك.
* مناسب للرفع في GitHub كملف README.md.

---

## 📌 هل تريد أيضًا مثال:

* Landing Page كاملة؟
* Login Form؟
* Dashboard UI؟

اكتب ما تريد وسأجهز لك نسخة Markdown فورًا 💙


## 🧠 الخلاصة
ملخص سريع يثبت الفكرة الأساسية لتايلويند.
- Tailwind بيعتمد على **Utility Classes**
- مفيش `row` و `col` زي Bootstrap
- Flex و Grid هما الأساس
- الملف ده مناسب كـ **Reference سريع** لأي مشروع

---

> ✅ جاهز للرفع مباشرة على GitHub كملف Markdown

