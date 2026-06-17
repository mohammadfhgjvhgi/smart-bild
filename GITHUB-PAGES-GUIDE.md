# 📦 دليل رفع موقع SmartBuild Palestine على GitHub Pages

> **⚠️ تحذير أمني مهم:** قبل أي شيء، احذف أي توكن سبق ونشرته من GitHub Settings → Tokens. لا تنشر توكنات في أي مكان أبداً.

---

## 🎯 المتطلبات

- ملف `company-website.html` (موجود في `/home/z/my-project/download/`)
- حساب GitHub (مجاني — سجل على https://github.com)
- 5 دقائق من وقتك

---

## 📝 الخطوة 1: إنشاء Repository جديد

1. افتح https://github.com/new
2. املأ التفاصيل:
   - **Repository name:** `smartbuild-palestine`
   - **Description:** `SmartBuild Palestine — Smart Building Systems & Automation`
   - **Visibility:** ✅ Public (مهم ليكون GitHub Pages مجاني)
   - **Initialize this repository with:** ✅ Add a README file
3. اضغط **Create repository**

---

## 📤 الخطوة 2: رفع ملف HTML

### الطريقة الأسهل (Drag & Drop):

1. في صفحة الـ repository الجديد، اضغط على **Add file → Upload files**
2. اسحب ملف `company-website.html` إلى المنطقة
3. **مهم:** أعد تسمية الملف إلى `index.html` (اكتب في حقل الاسم: `index.html`)
4. اكتب رسالة commit: `Add company website`
5. اضغط **Commit changes**

---

## ⚙️ الخطوة 3: تفعيل GitHub Pages

1. في صفحة الـ repository، اضغط على **Settings** (آخر tab بالأعلى)
2. من القائمة الجانبية اليسرى، اضغط على **Pages**
3. في قسم **Source**:
   - اختر **Deploy from a branch**
   - Branch: `main` (أو `master`)
   - Folder: `/ (root)`
4. اضغط **Save**

---

## 🌐 الخطوة 4: انتظر الدقائق وافتح موقعك

- GitHub Pages يأخذ **1-5 دقائق** ليصبح جاهزاً
- تحديث الصفحة (F5) — ستظهر رسالة: "Your site is live at..."
- **رابط موقعك سيكون:**
  ```
  https://YOUR-USERNAME.github.io/smartbuild-palestine/
  ```

مثال: لو اسم مستخدمك `mohammed-aqeeli`، الرابط سيكون:
```
https://mohammed-aqeeli.github.io/smartbuild-palestine/
```

---

## ✏️ الخطوة 5: تخصيص الموقع (مهم!)

افتح ملف `index.html` على GitHub (اضغط على اسم الملف) ثم اضغط ✏️ **Edit**، وعدّل التالي:

### 1. رابط WhatsApp (مهم جداً):
ابحث عن `wa.me/9705XXXXXXXX` واستبدله برقمك:
```bash
# ابحث عن (3 مواضع):
href="https://wa.me/9705XXXXXXXX"

# استبدلها برقمك (مع رمز الدولة 970):
href="https://wa.me/970599123456"
```

### 2. البريد الإلكتروني لاستقبال رسائل العملاء:
ابحث عن `your-email@example.com` واستبدله بإيميلك:
```html
<form ... action="https://formsubmit.co/your-email@example.com" ...>
# استبدلها بـ:
<form ... action="https://formsubmit.co/mohammed.aqeeli@gmail.com" ...>
```

> 💡 **FormSubmit.co** خدمة مجانية: أول مرة يصلك إيميل تفعيل، اضغط عليه وتصلك رسائل العملاء مباشرة على إيميلك.

### 3. رقم الهاتف:
ابحث عن `+970 5XX XXX XXX` واستبدله برقمك (موضعين).

### 4. روابط التواصل الاجتماعي:
ابحث عن `href="#"` في قسم social-links وأضف روابطك (فيسبوك، انستغرام، لينكدإن).

### 5. البريد الإلكتروني في قسم Contact:
ابحث عن `info@smartbuild.ps` واستبدله بإيميلك الحقيقي.

---

## 🎨 الخطوة 6 (اختيارية): نطاق مخصص

لو تريد موقعاً مثل `smartbuild.ps`:

1. اشترِ نطاقاً من Namecheap / GoDaddy / الاسم في جوجل (~10-15$ سنوياً)
2. في GitHub Settings → Pages → Custom domain
3. اكتب نطاقك (مثل `smartbuild.ps`)
4. في لوحة تحكم النطاق، أضف DNS records:
   ```
   A record: @ → 185.199.108.153
   A record: @ → 185.199.109.153
   A record: @ → 185.199.110.153
   A record: @ → 185.199.111.153
   CNAME: www → YOUR-USERNAME.github.io
   ```

---

## 🔧 صيانة الموقع لاحقاً

### تحديث المحتوى:
- افتح الـ repository على GitHub
- اضغط على `index.html`
- اضغط ✏️ Edit
- عدّل واحفظ

### إضافة صور المشاريع:
1. ارفع الصور للـ repository (Add file → Upload files)
2. في `index.html`، استبدل أيقونات `<i class="fas fa-...">` بـ:
   ```html
   <img src="project1.jpg" alt="SBMS Project" style="width:100%;height:100%;object-fit:cover;">
   ```

---

## 🆘 استكشاف الأخطاء

### الموقع لا يفتح؟
1. تأكد أن الـ repository **Public** (وليس Private)
2. تأكد أن اسم الملف `index.html` (وليس company-website.html)
3. انتظر 5 دقائق ثم أعد المحاولة
4. تحقق من Status في Settings → Pages

### الصفحة فارغة؟
- افتح Developer Tools (F12) → Console — اقرأ الأخطاء
- غالباً المشكلة من خطأ في HTML — انسخ الكود الصحيح من جديد

### نموذج التواصل لا يعمل؟
- تأكد أنك استبدلت `your-email@example.com` بإيميلك
- أول مرة تضغط Submit، يصلك إيميل تفعيل من FormSubmit
- اضغط رابط التفعيل — وبعدها كل الرسائل تصلك مباشرة

---

## 📊 ما يحتويه الموقع

| القسم | المحتوى |
|---|---|
| Hero | عنوان رئيسي + 4 إحصائيات + CTA |
| About | قصة الشركة + قيم + إحصائيات |
| Services | 6 خدمات (حريق + سرقة + كاميرات + أتمتة + شمسية + صيانة) |
| Projects | 6 مشاريع فعلية من إنجازاتك |
| Why Us | 6 ميزات تنافسية |
| Process | 5 خطوات عمل |
| Pricing | 3 باقات (Basic + Pro + Enterprise) |
| Testimonials | 3 آراء عملاء (من ضمنها لجنة الوزارية) |
| Team | محمد + عمار |
| FAQ | 5 أسئلة شائعة |
| Contact | معلومات + نموذج تواصل + WhatsApp |
| Footer | روابط + سوشيال |

**التصميم:** Dark Blue (#0a1628) + Orange (#ff6b35) — مطابق لبوربوينتك
**الخطوط:** Cairo + Tajawal — مطابقة لبوربوينتك
**اللغة:** عربي RTL كامل
**الاستجابة:** Mobile + Tablet + Desktop
**التفاعلية:** Animations + Hover + Scroll Reveal + FAQ Accordion

---

## 🚀 بعد النشر

### شارك الموقع على:
- فيسبوك (صفحة الشركة + مجموعات الخليل)
- واتساب (للعملاء المحتملين)
- انستغرام (Bio link)
- البطاقات الشخصية (QR code يوجه للموقع)

### تابع الزوار:
- أضف Google Analytics (مجاني) لمعرفة عدد الزوار
- أو استخدم GitHub Insights (موجود في تبويب Insights)

---

**🎉 مبروك! شركتك صار لها وجود رقمي رسمي.**

لو واجهت أي مشكلة، أخبرني — أنا هنا للمساعدة.
