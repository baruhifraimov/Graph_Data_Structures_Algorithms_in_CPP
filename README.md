<div dir="rtl">

# מטלה מספר 1 - מימוש גרף על ידי רשימת שכנויות

### יושרה אקדמית

במהלך העבודה על המטלות, מותר להתייעץ עם סטודנטים אחרים ולחפש מידע באינטרנט. עם זאת, חל איסור להעתיק קטעי קוד שלמים ממקורות חיצוניים, כולל סטודנטים אחרים, אתרי אינטרנט ומודלי בינה מלאכותית (כגון ChatGPT).

יש לדווח על כל עזרה שקיבלתם, בין אם מדובר בהתייעצות עם סטודנטים אחרים או במידע שנמצא באינטרנט, בהתאם ל[תקנון היושר של המחלקה](https://www.ariel.ac.il/wp/cs/wp-content/uploads/sites/88/2020/08/Guidelines-for-Academic-Integrity.pdf).
**במקרה של שימוש בכלי בינה מלאכותית (AI), יש לצרף את הפרומפטים שהוזנו ואת התשובות שהתקבלו**.

-----
* **מטרת המטלה:** הבנת החומר הנלמד בהרצאות הראשונות, כגון: ניהול זיכרון ב ++C, מחלקות, עצמים, מרחבי שמות, העברת פרמטרים לפונקציות, החזרת אובייקטים.
* **שימו לב!** במטלה **אסור** להשתמש בספרייה הסטנדרטית; ניתן להשתמש במערך. **יתכן שתצטרכו לממש מבנה/י נתונים המתאים לצרכי המטלה**..
* **ההגשה ביחידים**.

---

## הוראות הגשה ב Moodle:

במערכת Moodle יש להגיש **קובץ טקסט למשל (`submission.txt`)** המכיל 3 שורות בפורמט הבא:

1. **תעודת זהות** – מספר תעודת הזהות של הסטודנט.
2. **קישור להגשה** – קישור למאגר ה-GitHub שבו נמצא הפרויקט.
3. **פרטי ה-commit האחרון** – המחרוזת המזהה של ה-commit האחרון (`commit hash`) 

 - דוגמה לקובץ הגשה תקין:
```
123456789
https://github.com/example-user/graph-assignment
e3f1c1a 
```

---

גרפים הם חלק בלתי נפרד ממדעי המחשב. במהלך הלימודים נחשפתם לדרכים שונות לייצוג של גרפים (מטריצת שכנויות, רשימת שכנויות ועוד).

במטלה זו תממשו גרף באמצעות **רשימת שכנויות** – [Adjacency List](https://en.wikipedia.org/wiki/Adjacency_list).

---

## דרישות המטלה:

### מימוש המחלקות הבאות:
הוסיפו את המחלקות במרחב שמות (namespace) חדש ( קראו לו ```graph```).

#### מחלקה בשם `Graph`:
הגרף יאותחל עם מספר קודקודים מסוים ולא ניתן יהיה לשנות את מספר הקודקודים בגרף. 
המחלקה תכיל את רשימת השכנויות וכן את הפונקציות הבאות:
1. פונקציה  `addEdge`  מקבלת שלושה מספרים שלמים: מקור, יעד ומשקל (ברירת המחדל למשקל היא 1). הפונקציה תוסיף צלע (לא מכוונת) לגרף.
2. פונקציה  `removeEdge` מקבלת שני מספרים שלמים המייצגים צלע ומוחקת אותה מהגרף. אם הצלע לא קיימת, הפונקציה תזרוק חריגה.
3. פונקציה  `print_graph` מדפיסה את הגרף בצורה כלשהי הגיונית לבחירתכם.
4. במידת הצורך, יש להוסיף בנאים\פונקציות עזר רלונטיות למחלקה.

#### מחלקה בשם `Algorithms`:
מחלקה זו תממש אלגוריתמים שונים על גרף (הכי קרוב שאפשר לאלו שלמדתם בקורס אלגוריתמים 1) מכוון ותכיל את:
1. פונקציה `bfs` – מקבלת גרף וקודקוד מקור ומחזירה גרף שהוא עץ מושרש (שהשורש הוא קודקוד המקור כמובן) שהתקבל מסריקת BFS .  
2. פונקציה `dfs` – מקבלת גרף וקודקוד ממנו תתחיל הסריקה ומחזירה גרף (עץ או יער) המתקבל לפי סריקת DFS. (עץ זה יכיל קודקודים מקוריים ורק צלעות מסוג tree edges).
3. פונקציה `dijkstra` – מקבלת גרף וקודקוד התחלה ומחזירה עץ ממושקל של מסלולים קצרים ביותר.
4. פונקציה `prim` – מקבלת גרף, מחשבת את העץ הפורש המינימלי ומחזירה אותו (כלומר מחזירה גרף המייצג את העץ).
5. פונקציה `kruskal` - כמו סעיף הקודם.
-  מכיוון ש-STL אינה זמינה במטלה זו, לצורך מימוש אלגוריתמים אלו תצטרכו לממש באופן בסיסי מבני נתונים נוספים: תור ו\או תור עדיפויות ו-union find. מימוש בסיסי אומר כי מספיק לממש מבנים אלו רק פונקציאונלית, אין דרישה מיוחדת לסיבוכיות. 
   
 
---

#### דרישות נוספות:

- חשוב לוודא שה-repository ציבורי.
- כתבו בתחילת **כל** קובץ את כתובת המייל שלכם.
- כתבו קוד נקי, מסודר, מחולק לקבצים, מודולרי, מתועד בצורה מספקת וכמובן בדיקות יחידה עבור כל הפונקציות.
- בדקו את תקינות הקלט ולזרוק חריגות מתאימות במידת הצורך
- מצורף קובץ קצר בשם `Test.cpp` להדגמת מימוש הבדיקות יחידה בעזרת ספריית `doctest`.
- לשימושכם הקישור הבא [doctest](https://github.com/doctest/doctest) בו תוכלו לראות דוגמאות נוספות לשימוש בסיפריה זו.
- מצורף קובץ בשם `Demo.cpp` המדגים את השימוש בקוד. שימו לב שקובץ זה אינו מחייב! להיפך, עליכם לשנות אותו.
- יש לבדוק שאין זליגת זיכרון באמצעות `valgrind`.
- צרפו גם קובץ `README` עם הסבר על פרויקט, על חלוקה למחלקות וקבצים וכל מידע אחר רלוונטי.


#### קובץ `Makefile`:
הוסיפו לפרויקט קובץ `Makefile` הכולל את הפקודות הבאות:
- הפקודה `make Main` – להרצת קובץ ההדגמה.
- הפקודה `make test` – להרצת בדיקות היחידה.
- הפקודה `make valgrind` – בדיקת זליגת זיכרון באמצעות valgrind.


בהצלחה!

</div>

