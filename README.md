<!-- markdownlint-disable MD034 -->
# GFWProxyProtector

به کمک این اسکریپت میتوانید ماژول xt_geoip را برای هسته ی لینوکس نصب و فعال کنید. این ماژول سیستم عامل را قادر به کنترل اتصالات شبکه بر اساس خصوصیات جغرافیایی می‌کند. با این روش دیگر اهمیتی ندارد از چه نرم افزار پروکسی یا وی پی ان بر روی سرور استفاده می‌کنید چون نهایتا تمام اتصالات توسط هسته ی سیستم عامل لینوکس و iptables بررسی خواهند شد.

برای مثال این اسکریپت پس از فعالسازی ماژول به کمک دستور زیر مانع اتصالات خروجی به سمت آی‌پی های ایرانی و چینی می‌شود:

```
iptables -A OUTPUT -m geoip --dst-cc IR,CN -j DROP
```

## نحوه اجرا

```
git clone https://github.com/0xLem0nade/GFIProxyProtector.git
cd GFIProxyProtector
chmod +x run.sh
./run.sh
```

## منابع

- [صفحه ی اصلی ماژول](https://inai.de/projects/xtables-addons/geoip.php)
