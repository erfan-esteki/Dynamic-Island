# Dynamic Island Persian (Android · Jetpack Compose)

نسخه نهایی و یکپارچه پروژه بومی اندروید جزیره پویا با **Kotlin + Jetpack Compose + Material 3**:
- موتور رندر سه‌لایه Gooey: شیدر **AGSL SDF** با درخشش لبه (اندروید ۱۳+)، **RenderEffect** (اندروید ۱۲) و **متابال بزیه مکعبی دقیق (`metaballNeck`)** روی Canvas (اندروید ۸ تا ۱۱)
- تعامل لمسی (Long Press برای کارت گسترده)، بازخورد لرزشی (Haptic Feedback)، پشته فعالیت‌های همزمان (Live Stack) و اتصال زنده به `BatteryManager` و `AudioManager`
- دانلود خودکار فونت **Vazirmatn** هنگام Build همراه با بازگشت امن به فونت پیش‌فرض در صورت نبود اینترنت
- آزمون‌های واحد (JUnit + Coroutines Test) و آزمون‌های رابط کاربری (Compose UI Test)

## اجرا در Android Studio
1. پوشه پروژه را در Android Studio (Ladybug یا جدیدتر) با JDK 17 باز کنید.
2. روی **Sync Project with Gradle Files** بزنید؛ تسک `downloadVazirmatn` فونت‌ها را خودکار در `app/src/main/res/font/` دریافت می‌کند (در صورت قطع اینترنت، اپ بدون خطا با فونت پیش‌فرض اجرا می‌شود).
3. برای اجرای تست‌ها:
   - `./gradlew testDebugUnitTest`
   - `./gradlew connectedDebugAndroidTest`
