# RetinaXPart2
#A simulator that calculates  functions inside each cell of the graph and gives accurate result


פרויקט זה עוסק בבניה ושדרוג של סימולטור תוכנה ייעודי למבנה של רשתית העין. פרויקט זה נועד לשמש חוקרים של הרשתית במהלך מחקרם.
כיום לא קיים ממשק נוח שמשמש ככלי לבנית רשתות של מאות אלפי תאים ברשתית העין וחישוב מעבר אותות ברשת כזו. משמע שחוקרים אינם מסוגלים לבצע סימולציות בסדר גודל שמתאים לפיצוח
הבנת פעולות תאי הרשתית. פרויקט זה בא לתת מענה לבעיה זו על ידי יצירת ממשק וסביבת עבודה נוחה ואינטואיטיבית לחוקרי רשתית העין לביצוע סימולציות המתרחשות בתאים של רשתית העין.
פרויקט זה מתבסס על פרויקט גמר קיים של הסטודנטים שבנו מערכת שמבצעת סימולציה של תאי רשתית בודדים, הקשרים ביניהם ודרכי הפעולה ביניהם.
מטרת הפרויקט שלהם הייתה לבנות סימולטור תוכנה ייעודי למבנה העצבי של רשתית העין, שישמש את חוקרי הרשתית ככלי מחקר. בעזרתו החוקרים יוכלו לבנות מודלים לרשתות תאים המדמות תאי עצב ברשתית,
ולהשוואת בין תוצאות הניסויים השונות. הפרויקט אפשר סימולציה על 20 תאים לכל היותר. 
המערכת הזו מייצגת ממשק שמתבסס על הליבה הקיימת של חלק א', שמאפשרת סימולציה תקינה על מאות תאים.
הסימולטור יאפשר לקלוט ערכים ממשיים שמייצגים אותות אור המתקבלים בתאי הרשתית, יאפשר לשנות את הרכב התאים, דרכי הפעולה שלהם, לראות את ההשפעה על הרשתית, ולראות את זרימת מעבר האות ברשתית. 
קבוצת תאי רשתית מוצגת כגרף, והסימולטור גם מאפשר לבנות רשתות גדולות יותר על ידי חיבור כמה גרפים לרשת מורכבת יותר.

המערכת שלנו מבצעת ויזואליזציה על גרף/קבוצת גרפים/חיבור בין גרפים המייצגים חלקי רשת דו מימדית של תאים ברשתית העין, כלומר ממשק זה מאפשר לייצג מערכת גרפים גדולה של תאים ובכך מאפשר הסתכלות
ברמת המיקרו והמאקרו על הקשרים בכל חלקי המערכת. 
המערכת כוללת ממשק שמאפשר למשתמש לבצע את הפעולות הבאות :
1.	בניית גרף שממדל רשת דו ממדית של תאי רשתית
2.	חיבור בין גרפים 
3.	שכפול גרפים 
4.	שליפת נתוני הגרפים לקובץ
5.	מחיקת גרפים
6.	ייצוג ויזואלי של הגרף/קבוצת גרפים/חיבורים
7.	הרצת סימולציית חישוב אותות על רשתות נרחבות

.

להלן תיאור הפרויקט-


--------------------------------------------------------------------------------------------------------------------------------------------------------
יצירת תאים מסוג קלט
ראשית תיווצר לנו תכונה מסוג קלט , ניתן לראות ששמה היא InputCell (כתום) באיור.
אליה מחוברת פונקציה , היא תהיה מחוברת בהכרח לישות של פונקציה ספציפית x (ירוק)כפי שניתן לראות באיור.
ישות פונקציה ספציפית תהיה בהכרח מחוברת למשתנה ,במקרה הזה x (צהוב) , כפי שניתן לראות באיור.
נציין שעדיין לא נוצר תא אמיתי, כדי לייצר תא אמיתי, נצטרך לחברו לטיפוס שיתאר אותו (CellType) שבדוגמא זו הוא ה-InputCell, לא ניתן לייצר תא בלי טיפוס, כיוון שתא חייב להיות מטיפוס כלשהו.
לשם כך, נלחץ על הכפתור      בכדי לחבר ל- CellType תא CellInstance.

![תמונה1](https://github.com/vera962/RetinaXPart2/assets/78477792/faf07bef-d312-4154-9e4d-2dc0ef153484)


--------------------------------------------------------------------------------------------------------------------------------------------------------

כעת נייצר תאים "אמיתיים" (המסומנים בצבע אדום כאן). נייצר אותם ע"י לחיצה על כפתור ה+ הירוק שממד שמאל. נזכור שכל CellType הוא מסוג מסויים. ובמקרה שכאן הוא מסוג InputCell, וכל סוג תא מורכב מ
ממשתנים ופונקציה שמתארת את התפקיד של הסוג תא.(בדוגמא שכאן המשתנה בצבע צהוב פונקציה היא ירוקה.) אז כאן מייצרים CellInstances לסוג התא.
אפשר לייצר כמה תאים אמיתיים כאלה שנרצה. מה שיעבור בהם בסוף יהיו הערכים ההתחלתים שהוזנו ע"י המשתמש מקובץ אקסל.

![תמונה2](https://github.com/vera962/RetinaXPart2/assets/78477792/a95b60e1-bfa0-4c88-bcef-604028e6fb59)


---------------------------------------------------------------------------------------------------------------------------------------------------------

ייצור תא מסוג פונקציית חיבור
ראשית נלחץ על הכפתור Add Cell Type ונייצר תכונה מסוג חיבור , ניתן לראות ששמה היא Add.
הפונקציה שתחובר אליה תהיה x+y, ומשתניה יהיו x,y.
בנוסף, נבחר TransformType,במקרה זה נבחר ב - Analog to Analog.
לבסוף נלחץ על Create Cell Type כדי לייצרו. נציין שעדיין לא נוצר תא אמיתי, כדי לייצר תא אמיתי,
נצטרך לחברו לטיפוס שיתאר אותו (CellType) שבדוגמא זו הוא ה-Add, לא ניתן לייצר תא בלי טיפוס, כיוון שתא חייב להיות מטיפוס כלשהו.


![תמונה3](https://github.com/vera962/RetinaXPart2/assets/78477792/758c351f-07bc-46dc-9b4a-373e75739916)


--------------------------------------------------------------------------------------------------------------------------------------------------------

כך נראת יצירה של תאים מסוג קלט ותא מסוג חיבור (התאים האדומים מייצגים את התאים האמיתיי)



![תמונה4](https://github.com/vera962/RetinaXPart2/assets/78477792/6fbde1f7-0d7a-4144-8a7e-6df5f5349a2b)


--------------------------------------------------------------------------------------------------------------------------------------------------------

כעת נחבר בין התאים שיצרנו (CellIsntaces) דרך משתנה שקיים בתא היעד,על ידי לחיצה על Connect Cells.
נרחף מעל התאים שאנו רוצים לקשר)נזכיר שניתן לקשר רק בין CellInstances) ונבדוק את ה-ID שלהם , לאחר מכן נזין את המידע בחלון,בחלון ה-Delay  נבחר 0 או 1, ה-Delay שולט בזמן הכניסה של ערך לתא , ז"א האם להכניסו ישירות כאשר המידע מתקבל או לחכות פעימה אחת, לתוך שדה Input מזינים את התא שאליו מועב


![תמונה5](https://github.com/vera962/RetinaXPart2/assets/78477792/29189617-ffda-4359-9454-012d5b296a18)

יצירת קשר חדש בין תאים – חיבור תאי קלט לתא פונקציה


--------------------------------------------------------------------------------------------------------------------------------------------------------
תצוגה לאחר החיבור בין התאים, ניתן לראות שחיברנו בין שני התאים השמאליים(אדומים) שהם מסוג קלט ומהם עובר מידע הלאה דרך המשתנים(צהובים) אל התא הימני(אדום) שמסוג פונקציית חיבור 



![תמונה6](https://github.com/vera962/RetinaXPart2/assets/78477792/67a29450-f4dd-4518-9c43-9a2ea17b9e79)


--------------------------------------------------------------------------------------------------------------------------------------------------------

נייצר תת-גרף בעזרת חיבור יישות SubGraphInstance לתאי הקלט על מנת לאגד את הרשת לתת תת-גרף. נלחץ על הכפתור Create SubGraph,
נזין את השם הרצוי ונבדוק את את ה-ID של תאי הקלט (CellInstances) על ידי ריחוף עליהם עם העכבר.


![תמונה7](https://github.com/vera962/RetinaXPart2/assets/78477792/d4a7b991-ffb2-4800-9500-10ed74daa07f)

חיבור ישות SubGraphInstance לתאי הקלט של הגרף


--------------------------------------------------------------------------------------------------------------------------------------------------------

תת הגרף שנוצר , בעיגול מסומנת היישות SubGraphInstance 

![תמונה8](https://github.com/vera962/RetinaXPart2/assets/78477792/00de5678-fba6-472d-94ba-e72cd32c4944)


--------------------------------------------------------------------------------------------------------------------------------------------------------

הגרף הרצוי לשכפול

![תמונה9](https://github.com/vera962/RetinaXPart2/assets/78477792/90e0a082-1184-447d-825d-d8e94f873603)


--------------------------------------------------------------------------------------------------------------------------------------------------------


תוצאת שכפול הגרף הקיים 4 פעמים נוספות


![תמונה10](https://github.com/vera962/RetinaXPart2/assets/78477792/f9bb7a4d-6de2-4b09-a423-47fd7618f3cd)


--------------------------------------------------------------------------------------------------------------------------------------------------------
תוצאת המחיקה של תת הגרף

![תמונה11](https://github.com/vera962/RetinaXPart2/assets/78477792/281d9faf-0a53-46de-82d2-7b0a4896a6f9)


--------------------------------------------------------------------------------------------------------------------------------------------------------

שליפת מידע-
ניתן לשלוף את הנתונים של הגרף לקובץ חיצוני על ידי לחיצה על הכפתור Download Graph Json ולהזין את ה- ID של הגרף הרצוי, ולאחר מכן ניתן יהיה לראות את המידע מופיע בקובץ json
הנתונים יכתבו לקובץ  jsonשירד אוטומטית בעת לחיצה על כפתור ה Download

![תמונה12](https://github.com/vera962/RetinaXPart2/assets/78477792/671c71d2-ade7-419e-8e33-8e5a94005f2a)
![תמונה13](https://github.com/vera962/RetinaXPart2/assets/78477792/1dc97ffe-6580-4fb4-9d0d-2b02de94ee5a)


--------------------------------------------------------------------------------------------------------------------------------------------------------

סימולציה-
ביצוע סימולציה על הגרף הרצוי או הגרפים הרצויים יתבצע על ידי לחיצה על הכפתור Simulate, תופיע רשימת ID’s של כל תאי הקלט ועל המשתמש להזין את הנתונים הרצויים אל תאי הקלט המתאימים לגרפים שעליהם הוא רוצה להריץ את הסימולציה.
יש לשים לב שאורך הנתונים המוזנים צריך להיות אחיד בכל שדה, לדוגמא : 1,2,3,4 , משמע לכל תא קלט שנבחר, על המשתמש יהיה להזין נתונים באורך 4 שמופרדים על ידי פסיק.לבסוף על המשתמש יהיה להזין
את ה-ID’s של תאי הפלט בהם הוא ירצה לראות את תוצאות הסימולציה בנקודות זמן שונות, עם הפרדה של פסיק, לדוגמא: 169,89,63,4


![תמונה15](https://github.com/vera962/RetinaXPart2/assets/78477792/22cb6885-8f5b-4aed-80f6-63ae1f945d47)
![תמונה14](https://github.com/vera962/RetinaXPart2/assets/78477792/4cad9d37-f73d-4141-8f68-352e2e9f140b)


--------------------------------------------------------------------------------------------------------------------------------------------------------
תוצאת החישוב לאחר הרצת הסימולציה על פי הנתונים שהוזנו 

![תמונה16](https://github.com/vera962/RetinaXPart2/assets/78477792/5f5cdc1e-43b6-445f-abd3-32db9e58b927)


--------------------------------------------------------------------------------------------------------------------------------------------------------