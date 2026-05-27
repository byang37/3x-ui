# Fork 3X-UI: ضریب ترافیک

این مخزن یک fork شخصی از 3X-UI است. این fork با پروژه اصلی همگام می‌شود و این README فقط قابلیت‌های اصلی اضافه‌شده خارج از upstream را توضیح می‌دهد.

## قابلیت اصلی اضافه‌شده

### ضریب ترافیک برای inbound

این fork برای inbound node ها قابلیت ضریب ترافیک اضافه می‌کند.

- در فرم‌های Add Inbound و Edit Inbound فیلد Traffic Multiplier اضافه شده است.
- مقدار پیش‌فرض `1` است و رفتار اصلی شمارش ترافیک را حفظ می‌کند.
- اگر ضریب روی `2` تنظیم شود، upload و download inbound دو برابر مصرف واقعی محاسبه می‌شوند.
- upload و download هر client داخل inbound نیز با همین ضریب محاسبه می‌شود.
- ترافیک باقی‌مانده client و بررسی عبور از محدودیت ترافیک بر اساس مقدار وزن‌دهی‌شده انجام می‌شود.
- هنگام sync کردن inbound با remote node، مقدار ضریب هم ارسال می‌شود.
- subscription link ها تغییر نمی‌کنند. مقدار مصرف و ترافیک باقی‌مانده در subscription بر اساس آمار وزن‌دهی‌شده client محاسبه می‌شود.

## نصب این fork

```bash
bash <(curl -Ls https://raw.githubusercontent.com/byang37/3x-ui/master/install.sh)
```

## ارجاع به upstream

این fork بر پایه پروژه اصلی زیر ساخته شده است:

[MHSanaei/3x-ui](https://github.com/MHSanaei/3x-ui)
