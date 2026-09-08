منصة الأستاذ التعليمية V7

هذه النسخة تحافظ على واجهة V4 تقريبًا، مع ربط Supabase فعليًا.

1) ارفع الملفات إلى GitHub Pages:
- index.html
- admin.html
- config.js

2) افتح Supabase > SQL Editor.
3) الصق كل محتوى supabase.sql واضغط Run.
4) افتح الموقع.
5) أنشئ حساب طالب من تسجيل الدخول.
6) لإنشاء حساب المدرس: أنشئ الحساب أولًا من نفس شاشة التسجيل، ثم نفّذ في SQL Editor:
   update public.profiles set role='teacher' where id=(select id from auth.users where email='TEACHER_EMAIL');
7) سجّل دخول المدرس ثم اضغط 👨‍🏫 المدرس لفتح لوحة التحكم.

مهم:
- المفتاح الموجود في config.js هو Publishable Key فقط.
- لا تضع Secret/Service Role Key في GitHub أو داخل JavaScript.
- Team ظاهر للعامة لأن V4 كان يعرضه في الصفحة الرئيسية.
