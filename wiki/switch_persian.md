# [لینوکس] Bash switch استفاده: [تغییر بین گزینه‌ها]

## Overview
دستور `switch` در Bash برای تغییر بین گزینه‌ها یا حالت‌های مختلف در یک اسکریپت استفاده می‌شود. این دستور به شما اجازه می‌دهد تا بر اساس ورودی‌های مختلف، عملیات‌های متفاوتی را انجام دهید.

## Usage
سینتکس پایه دستور `switch` به صورت زیر است:

```bash
switch [options] [arguments]
```

## Common Options
- `-e`: بررسی می‌کند که آیا یک گزینه خاص وجود دارد یا خیر.
- `-d`: گزینه پیش‌فرض را مشخص می‌کند که در صورت عدم تطابق با هیچ‌یک از گزینه‌ها اجرا می‌شود.

## Common Examples
### مثال ۱: استفاده از switch برای بررسی ورودی
```bash
case $1 in
    start)
        echo "Starting the service..."
        ;;
    stop)
        echo "Stopping the service..."
        ;;
    restart)
        echo "Restarting the service..."
        ;;
    *)
        echo "Usage: $0 {start|stop|restart}"
        ;;
esac
```

### مثال ۲: گزینه پیش‌فرض
```bash
case $1 in
    hello)
        echo "Hello, World!"
        ;;
    goodbye)
        echo "Goodbye!"
        ;;
    *)
        echo "Please enter 'hello' or 'goodbye'."
        ;;
esac
```

## Tips
- همیشه از گزینه پیش‌فرض (`*`) استفاده کنید تا در صورت عدم تطابق با گزینه‌ها، کاربر را راهنمایی کنید.
- از تو رفتگی مناسب در کد استفاده کنید تا خوانایی آن افزایش یابد.
- می‌توانید از متغیرهای محیطی برای تعیین گزینه‌ها استفاده کنید تا انعطاف‌پذیری بیشتری داشته باشید.