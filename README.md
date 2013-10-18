מסמך איפיון לפרוייקט במגשימים (Magshimim): סוס טרויאני לאנדרואיד
==================================

צד שרת
=======
תיאור כללי:
----------
המערכת משמשת לשליטה, בקרה ואיסוף מידע על מכשירים הפועלים על מערכת ההפעלה Android.

תיחום המערכת:
-------------
המערכת תפעל על מערכת ההפעלה Android.
תוכנת השרת שולחת את המידע לתוכנת הלקוח כל x זמן, או בכל פעם שיש גישה לאינטרנט- TBD
תוכנת השרת אוגרת את המידע עד לשליחתו אל הלקוח, ואז מוחקת אותו.

אילוצים:
-------
- פיתוח בAPI Levels 9-18.

תהליכים מרכזיים:
---------------


איסוף מידע:
----------
- אודות הטלפון (מספר גרסה, מספר טלפון ועוד)
- אנשי קשר 
- היסטוריית שיחות
- אסמסים
- אימיילים
- רשימת אפליקציות
- רשימת קבצים ותיקיות
- היסטוריית גלישה
- האזנה למיקרופון (כל x דקות קח דגימת קול של y דקות, או הקלט בתאריכים ... בשעות ...)
- האזנה למצלמה (כל x דקות קח y תמונות, או קח סרטון ווידיאו בתאריכים ... בשעות ...)
- האזנה לשבב NFC (האזנה אקטיבית- כל הזמן)
- מיקום GPS (כל x דקות קח מידע מהGPS, או הקלט את מסלול המשתמש בתאריכים ... בשעות ...)

שינוי מידע:
---------
- מחיקת והוספת קבצים
- הסתרת אסמסים ע"י מחיקתם

הפצה:
-----
שלב ראשון: הדבקת המכשיר ע"י התחזות לאפליקציה תמימה, ושכנוע המשתמש להתקין אותה, או התקנתה מבלי ידעתו.
שלב שני: הפצה למכשירים אחרים ע"י שליחת אימיילים ואסאמסים עם לינק לאפליקציה הנגועה אל רשימת אנשי הקשר של המכשיר המודבק.

שימור:
------
- ללא ROOT: התחזות לאפליקציה תמימה, לדוגמא- משחק, live wallpaper, ווידג'ט וכו'
- עם ROOT: במידה והשגנו גישת ROOT, ניתן להסתיר לגמרי את התוכנה מהמשתמש ומכל התהליכים והאפליקציות הרצות ברקע

פירוט תהליכים מרכזיים:
--------------------

צד לקוח
=======
תיאור כללי:
---------
- המערכת מופקדת על איסוף הנתונים מהשרת והצגתם למשתמש בממשק Web
- המערכת תאפשר למשתמש לשלוח פקודות לביצוע אצל השרת דרך ממשק הWeb

תיחום המערכת:
-------------
- המשתמש יתקשר עם תוכנת הלקוח ע"י כניסה לכתובת מסויימת דרך דפדפן אינטרנט.
- תוכנת הלקוח אחראית לשמירת המידע והצגתו למשתמש בממשק נוח.

אילוצים:
-------

תהליכים מרכזיים:
---------------

פקודות משתמש:
--------------
- הצגת מידע אודות הטלפון (מספר גרסה, מספר טלפון ועוד)
- הצגת רשימת אנשי קשר 
- הצגת היסטוריית שיחות
- הצגת אסמסים
- הצגת אימיילים
- הצגת רשימת האפליקציות המותקנות
- הצגת רשימת הקבצים והתיקיות
- הצגת היסטוריית הגלישה
- שמיעה לקבצי הקול שהתקבלו מהשרת, והצגת מידע לגביהם
- ניגון קבצי הווידיאו שהתקבלו מהרשת, והצגת מידע לגביהם
- הצגת הstrings שהתקבלו מהאזנה לשבב הNFC
- הצגת המיקומים שהמשתמש היה בהם עפ"י תאריכים ושעות ע"ג המפה
- אם השרת עוזב איזור מסויים או נכנס אל תוך אזור מסויים- הצגת התרעה TBD


פירוט תהליכים מרכזיים:
--------------------
