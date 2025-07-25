# SmartAnswerBot

SmartAnswerBot هو بوت تيليجرام متعدد الخدمات يعتمد على مكتبة [aiogram](https://docs.aiogram.dev/) و[Flask](https://flask.palletsprojects.com/) ويدعم عدة لغات (العربية، الإنجليزية، الروسية). يوفر البوت خدمات متنوعة مثل الترجمة، كتابة السيرة الذاتية، تصميم الإعلانات، المساعدة الأكاديمية، وغيرها.

## الميزات الرئيسية
- دعم متعدد اللغات (عربي، إنجليزي، روسي)
- خدمات متنوعة (ترجمة نصوص، كتابة سيرة ذاتية، تصميم، استشارات، إلخ)
- نظام FSM لإدارة تدفق الطلبات
- التحقق من الاشتراك في قناة تيليجرام قبل استخدام البوت
- تكامل مع Google Translate
- دعم استقبال الملفات والنصوص والصور
- نظام تواصل مع المسؤول وإشعارات إدارية
- نظام دفع وإثبات دفع وتقييم نهائي
- واجهة ويب بسيطة (Flask) للحفاظ على نشاط البوت

## المتطلبات
- Python 3.8+
- aiogram
- Flask
- googletrans==4.0.0-rc1

## الإعداد
1. قم بتثبيت المتطلبات:
   ```bash
   pip install -r requirements.txt
   ```
2. أنشئ ملف متغيرات البيئة أو عيّن المتغيرات التالية:
   - `BOT_TOKEN`: توكن البوت من BotFather
   - `CHANNEL_ID`: معرف أو اسم قناة التحقق من الاشتراك
   - `ADMIN_CHAT_ID`: معرف المسؤول
   - (اختياري) `PAYMENT_NOTIFICATION_CHAT_ID`, `SUPPORT_CONTACT_INFO`, `NEWS_CHANNEL_LINK`, `SBP_QR_CODE_FILE_ID`, `PORT`

3. شغّل البوت:
   ```bash
   python main.py
   ```

## الملفات
- `main.py`: الكود الرئيسي للبوت
- `requirements.txt`: متطلبات التشغيل
- `Procfile`: دعم التشغيل على منصات مثل Heroku
- `pyproject.toml`, `uv.lock`: إدارة الحزم (اختياري)

## ملاحظات
- تأكد من ضبط متغيرات البيئة بشكل صحيح قبل التشغيل.
- يوصى باستخدام Redis للتخزين في الإنتاج بدلاً من الذاكرة المؤقتة.
- يمكن تخصيص الخدمات والأسعار من خلال قاموس `services` في الكود.

## الدعم
للدعم أو الاستفسارات، تواصل مع المسؤول المحدد في متغير البيئة `SUPPORT_CONTACT_INFO`.
