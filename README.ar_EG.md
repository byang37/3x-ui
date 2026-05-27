[English](/README.md) | [فارسی](/README.fa_IR.md) | [العربية](/README.ar_EG.md) | [中文](/README.zh_CN.md) | [Español](/README.es_ES.md) | [Русский](/README.ru_RU.md)

# 3X-UI Fork: مضاعف الترافيك

هذا المستودع هو fork شخصي من 3X-UI. يتابع المشروع الأصلي، وهذا README يشرح فقط الوظيفة الأساسية المضافة خارج upstream.

## الوظيفة الأساسية المضافة

### مضاعف الترافيك للـ inbound

هذا fork يضيف مضاعف ترافيك لعقد inbound.

- نماذج Add Inbound و Edit Inbound تحتوي على حقل Traffic Multiplier.
- القيمة الافتراضية هي `1`، وهذا يحافظ على سلوك حساب الترافيك الأصلي.
- عند ضبط المضاعف على `2`، يتم حساب upload و download للـ inbound بضعف الاستخدام الفعلي.
- يتم حساب upload و download لكل client داخل inbound بنفس المضاعف.
- الترافيك المتبقي للـ client وفحص تجاوز الحد يستخدمان القيم الموزونة.
- مزامنة inbound مع remote nodes ترسل قيمة المضاعف أيضًا.
- subscription links لا تتغير. استخدام الترافيك والمتبقي في subscription يعتمدان على عدادات client الموزونة.

## تثبيت هذا fork

```bash
bash <(curl -Ls https://raw.githubusercontent.com/byang37/3x-ui/master/install.sh)
```

## مرجع upstream

هذا fork مبني على المشروع الأصلي:

[MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)
