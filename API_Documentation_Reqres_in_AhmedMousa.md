<div dir="rtl">
<div align="center">

# *توثيـق واجهـات برمجـة التطبيقات (API)*  

### ***مثال توضيحي لعمليات CRUD باستخدام واجهة Reqres.in***  



<p align="center">
  <img src="./media/image1.jpeg" alt="API Doc Cover" width="99%">
</p>
</div>
<p align="right"><strong>إعداد: أحمد موسى</strong></p>  
<p align="right"><strong>التاريخ: 2025/09/25</strong></p>  

---
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل استخدام Reqres.in API</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: #333;
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: #fff;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, #2980b9 0%, #2c3e50 100%);
            color: white;
            padding: 30px;
            text-align: center;
            border-bottom: 5px solid #3498db;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .content {
            display: flex;
            flex-wrap: wrap;
            padding: 0;
        }
        
        .toc {
            flex: 0 0 300px;
            background-color: #f8f9fa;
            padding: 25px;
            border-left: 1px solid #eaeaea;
            position: sticky;
            top: 0;
            align-self: flex-start;
            max-height: 100vh;
            overflow-y: auto;
        }
        
        .main-content {
            flex: 1;
            padding: 30px;
            min-width: 300px;
        }
        
        h2 {
            color: #2c3e50;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
            margin: 30px 0 20px;
            font-size: 1.8rem;
        }
        
        h3 {
            color: #2980b9;
            margin: 25px 0 15px;
            font-size: 1.4rem;
        }
        
        p {
            margin-bottom: 15px;
            font-size: 1.1rem;
            text-align: justify;
        }
        
        .toc h2 {
            text-align: center;
            color: #2c3e50;
            margin-top: 0;
        }
        
        .toc ul {
            list-style-type: none;
            padding-right: 0;
        }
        
        .toc li {
            margin-bottom: 10px;
            padding: 8px 15px;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .toc li:hover {
            background-color: #e3f2fd;
            transform: translateX(-5px);
        }
        
        .toc a {
            text-decoration: none;
            color: #2c3e50;
            display: block;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .toc a:hover {
            color: #2980b9;
        }
        
        .toc ul ul {
            margin-top: 5px;
            margin-right: 20px;
        }
        
        .toc ul ul li {
            margin-bottom: 5px;
            padding: 5px 10px;
            font-size: 0.95rem;
        }
        
        .code-block {
            background-color: #f1f1f1;
            border: 1px solid #ddd;
            border-radius: 5px;
            padding: 15px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            direction: ltr;
            text-align: left;
            overflow-x: auto;
        }
        
        .note {
            background-color: #e3f2fd;
            border-right: 4px solid #2196f3;
            padding: 15px;
            margin: 20px 0;
            border-radius: 5px;
        }
        
        .warning {
            background-color: #ffecb3;
            border-right: 4px solid #ffc107;
            padding: 15px;
            margin: 20px 0;
            border-radius: 5px;
        }
        
        .image-container {
            text-align: center;
            margin: 25px 0;
        }
        
        .image-container img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            background-color: #2c3e50;
            color: white;
            margin-top: 40px;
        }
        
        @media (max-width: 768px) {
            .content {
                flex-direction: column;
            }
            
            .toc {
                position: static;
                max-height: none;
                border-left: none;
                border-bottom: 1px solid #eaeaea;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>دليل استخدام Reqres.in API</h1>
            <p class="subtitle">دليل شامل لاختبار واجهات برمجة التطبيقات باستخدام Reqres.in</p>
        </header>
        
        <div class="content">
            <div class="main-content">
                <h2 id="المقدمة">1. المقدمة</h2>
                <p>يوفر هذا الدليل شرحًا مفصلاً لكيفية استخدام واجهة Reqres.in API التي تُعد منصة تجريبية مجانية لاختبار واجهات برمجة التطبيقات (APIs). تم تصميم هذه الواجهة خصيصًا للمطورين والمختبرين لممارسة وإتقان مهارات التعامل مع REST APIs دون الحاجة إلى قاعدة بيانات حقيقية.</p>
                
                <div class="image-container">
                    <img src="https://via.placeholder.com/800x400/2980b9/ffffff?text=Reqres.in+API+Diagram" alt="مخطط عمل Reqres.in API">
                </div>
                
                <h2 id="المتطلبات-الأساسية">2. المتطلبات الأساسية</h2>
                <p>قبل البدء في استخدام Reqres.in، يجب أن تكون على دراية بالمفاهيم الأساسية التالية:</p>
                <ul>
                    <li>مبادئ REST APIs</li>
                    <li>طرق HTTP (GET, POST, PUT, PATCH, DELETE)</li>
                    <li>رموز حالة HTTP</li>
                    <li>JSON (JavaScript Object Notation)</li>
                    <li>أدوات مثل Postman أو curl</li>
                </ul>
                
                <h2 id="نظرة-عامة-وطبيعة-الواجهة-reqresin">3. نظرة عامة وطبيعة الواجهة (Reqres.in)</h2>
                <p>Reqres.in هي واجهة API تجريبية توفر نقاط نهاية (endpoints) وهمية لمحاكاة سيناريوهات العالم الحقيقي. البيانات المخزنة ليست حقيقية ولا يتم الاحتفاظ بها بعد إجراء العمليات.</p>
                
                <h3 id="31-طبيعة-الواجهة-التجريبية">3.1 طبيعة الواجهة التجريبية</h3>
                <p>تم تصميم Reqres.in لتكون بيئة آمنة للتعلم والاختبار. جميع العمليات التي تقوم بها تكون مؤقتة ولا تؤثر على أي بيانات حقيقية.</p>
                
                <h3 id="32-أفضل-ممارسات-الاختبار">3.2 أفضل ممارسات الاختبار</h3>
                <p>عند اختبار API، يُنصح باتباع هذه الممارسات:</p>
                <ul>
                    <li>اختبار جميع حالات النجاح والفشل المتوقعة</li>
                    <li>التحقق من صحة هياكل البيانات المرسلة والمستلمة</li>
                    <li>اختبار أداء API تحت أحمال مختلفة</li>
                    <li>التأكد من معالجة الأخطاء بشكل صحيح</li>
                </ul>
                
                <h2 id="المصادقة-authentication--login">4. المصادقة (Authentication / Login)</h2>
                <p>تستخدم Reqres.in نظامًا مبسطًا للمصادقة يعتمد على البريد الإلكتروني وكلمة المرور.</p>
                
                <h3 id="41-الهدف-من-المصادقة">4.1 الهدف من المصادقة</h3>
                <p>الهدف من عملية المصادقة هو التحقق من هوية المستخدم ومنحه رمزًا (Token) يستخدمه للوصول إلى الموارد المحمية.</p>
                
                <h3 id="42-إرسال-طلب-تسجيل-الدخول">4.2 إرسال طلب تسجيل الدخول</h3>
                <div class="code-block">
                    POST /api/login<br>
                    Content-Type: application/json<br><br>
                    {<br>
                    &nbsp;&nbsp;"email": "eve.holt@reqres.in",<br>
                    &nbsp;&nbsp;"password": "cityslicka"<br>
                    }
                </div>
                
                <h3 id="43-الاستجابة-المتوقعة">4.3 الاستجابة المتوقعة</h3>
                <div class="code-block">
                    HTTP/1.1 200 OK<br>
                    Content-Type: application/json<br><br>
                    {<br>
                    &nbsp;&nbsp;"token": "QpwL5tke4Pnpja7X4"<br>
                    }
                </div>
                
                <h3 id="44-استخدام-الـ-token">4.4 استخدام الـ Token</h3>
                <p>بعد الحصول على الـ Token، يمكن استخدامه في رؤوس طلبات HTTP اللاحقة للوصول إلى الموارد المحمية:</p>
                <div class="code-block">
                    Authorization: Bearer QpwL5tke4Pnpja7X4
                </div>
                
                <h3 id="45-ملاحظات-مهمة">4.5 ملاحظات مهمة</h3>
                <div class="note">
                    <p>يجب استخدام البريد الإلكتروني وكلمة المرور المحددين في الوثائق الرسمية لـ Reqres.in للحصول على استجابة ناجحة.</p>
                </div>
                
                <!-- سيتم إضافة الأقسام المتبقية هنا -->
                
                <h2 id="العمليات-الأساسية-crud-باستخدام-postman">5. العمليات الأساسية (CRUD) باستخدام Postman</h2>
                <p>يشرح هذا القسم كيفية تنفيذ عمليات CRUD الأساسية باستخدام أداة Postman.</p>
                
                <h2 id="العمليات-الأساسية-على-resources">6. العمليات الأساسية على Resources</h2>
                <p>يغطي هذا القسم العمليات المختلفة التي يمكن تنفيذها على الموارد المتاحة في Reqres.in.</p>
                
                <h2 id="أمثلة-باستخدام-أمر-curl">7. أمثلة باستخدام أمر curl</h2>
                <p>يقدم هذا القبد أمثلة عملية لاستخدام أمر curl للتفاعل مع Reqres.in API.</p>
                
                <h2 id="معالجة-الأخطاء-error-handling">8. معالجة الأخطاء (Error Handling)</h2>
                <p>يشرح هذا القسم كيفية التعامل مع الأخطاء المختلفة التي قد تواجهها عند استخدام API.</p>
                
                <h2 id="التصفّح-pagination">9. التصفّح (Pagination)</h2>
                <p>يغطي هذا القسم كيفية التعامل مع التصفّح عند الحصول على قوائم كبيرة من البيانات.</p>
                
                <h2 id="الملاحق">10. الملاحق</h2>
                <p>يحتوي هذا القسم على معلومات إضافية ومصطلحات مفيدة.</p>
                
                <div class="image-container">
                    <img src="https://via.placeholder.com/800x400/27ae60/ffffff?text=API+Workflow+Example" alt="مثال سير عمل API">
                </div>
            </div>
            
            <div class="toc">
                <h2>فهرس المحتويات</h2>
                <ul>
                    <li><a href="#المقدمة">1. المقدمة</a></li>
                    <li><a href="#المتطلبات-الأساسية">2. المتطلبات الأساسية</a></li>
                    <li><a href="#نظرة-عامة-وطبيعة-الواجهة-reqresin">3. نظرة عامة وطبيعة الواجهة (Reqres.in)</a>
                        <ul>
                            <li><a href="#31-طبيعة-الواجهة-التجريبية">3.1 طبيعة الواجهة التجريبية</a></li>
                            <li><a href="#32-أفضل-ممارسات-الاختبار">3.2 أفضل ممارسات الاختبار</a></li>
                        </ul>
                    </li>
                    <li><a href="#المصادقة-authentication--login">4. المصادقة (Authentication / Login)</a>
                        <ul>
                            <li><a href="#41-الهدف-من-المصادقة">4.1 الهدف من المصادقة</a></li>
                            <li><a href="#42-إرسال-طلب-تسجيل-الدخول">4.2 إرسال طلب تسجيل الدخول</a></li>
                            <li><a href="#43-الاستجابة-المتوقعة">4.3 الاستجابة المتوقعة</a></li>
                            <li><a href="#44-استخدام-الـ-token">4.4 استخدام الـ Token</a></li>
                            <li><a href="#45-ملاحظات-مهمة">4.5 ملاحظات مهمة</a></li>
                        </ul>
                    </li>
                    <li><a href="#العمليات-الأساسية-crud-باستخدام-postman">5. العمليات الأساسية (CRUD) باستخدام Postman</a>
                        <ul>
                            <li><a href="#51-get--جلب-البيانات">5.1 GET – جلب البيانات</a></li>
                            <li><a href="#52-post--إنشاء-بيانات-جديدة">5.2 POST – إنشاء بيانات جديدة</a></li>
                            <li><a href="#53-put--تعديل-كامل-للبيانات">5.3 PUT – تعديل كامل للبيانات</a></li>
                            <li><a href="#54-patch--تعديل-جزئي-للبيانات">5.4 PATCH – تعديل جزئي للبيانات</a></li>
                            <li><a href="#55-delete--حذف-البيانات">5.5 DELETE – حذف البيانات</a></li>
                        </ul>
                    </li>
                    <li><a href="#العمليات-الأساسية-على-resources">6. العمليات الأساسية على Resources</a>
                        <ul>
                            <li><a href="#61-get--جلب-قائمة-الموارد">6.1 GET – جلب قائمة الموارد</a></li>
                            <li><a href="#62-get--جلب-مورد-واحد">6.2 GET – جلب مورد واحد</a></li>
                        </ul>
                    </li>
                    <li><a href="#أمثلة-باستخدام-أمر-curl">7. أمثلة باستخدام أمر curl</a>
                        <ul>
                            <li><a href="#71-المصادقة-authentication--login">7.1 المصادقة (Authentication / Login)</a></li>
                            <li><a href="#72-get--جلب-مستخدم">7.2 GET – جلب مستخدم</a></li>
                            <li><a href="#73-post--إنشاء-مستخدم">7.3 POST – إنشاء مستخدم</a></li>
                            <li><a href="#74-put--تعديل-كامل">7.4 PUT – تعديل كامل</a></li>
                            <li><a href="#75-patch--تعديل-جزئي">7.5 PATCH – تعديل جزئي</a></li>
                            <li><a href="#76-delete--حذف">7.6 DELETE – حذف</a></li>
                        </ul>
                    </li>
                    <li><a href="#معالجة-الأخطاء-error-handling">8. معالجة الأخطاء (Error Handling)</a>
                        <ul>
                            <li><a href="#81-مبادئ-عامة">8.1 مبادئ عامة</a></li>
                            <li><a href="#82-رموز-الحالة-الشائعة">8.2 رموز الحالة الشائعة</a></li>
                            <li><a href="#83-مسار-تشخيص-سريع-troubleshooting">8.3 مسار تشخيص سريع (Troubleshooting)</a></li>
                            <li><a href="#84-أفضل-ممارسات-التعامل-مع-الأخطاء-في-العميل">8.4 أفضل ممارسات التعامل مع الأخطاء في العميل</a></li>
                        </ul>
                    </li>
                    <li><a href="#التصفّح-pagination">9. التصفّح (Pagination)</a></li>
                    <li><a href="#الملاحق">10. الملاحق</a>
                        <ul>
                            <li><a href="#101-مصطلحات-موحّدة">10.1 مصطلحات موحّدة</a></li>
                            <li><a href="#102-روابط-مفيدة">10.2 روابط مفيدة</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
        </div>
        
        <footer>
            <p>دليل استخدام Reqres.in API &copy; 2023. جميع الحقوق محفوظة.</p>
        </footer>
    </div>

    <script>
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 20,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Highlight current section in TOC
        window.addEventListener('scroll', function() {
            const sections = document.querySelectorAll('.main-content h2, .main-content h3');
            const scrollPos = window.scrollY || document.documentElement.scrollTop;
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop - 100;
                const sectionBottom = sectionTop + section.offsetHeight;
                const sectionId = section.getAttribute('id');
                
                if (scrollPos >= sectionTop && scrollPos < sectionBottom) {
                    document.querySelectorAll('.toc a').forEach(link => {
                        link.parentElement.classList.remove('active');
                    });
                    
                    const activeLink = document.querySelector(`.toc a[href="#${sectionId}"]`);
                    if (activeLink) {
                        activeLink.parentElement.classList.add('active');
                    }
                }
            });
        });
    </script>
</body>
</html>

<div dir="rtl">

## 1. المقدمة

يُقدّم هذا الدليل شرحًا عمليًا لاستخدام واجهة برمجة التطبيقات التجريبية Reqres.in.  

يٌركّز الدليل على توضيح كيفية تنفيذ العمليات الأساسية (CRUD) وآلية المصادقة (Authentication) بالإضافة إلى معالجة الأخطاء (Error Handling) وتنظيم النتائج عبر التصفّح (Pagination).  

الهدف من هذا الدليل هو تزويد المطوّر بخطوات واضحة وأمثلة عملية يمكن الاعتماد عليها لاختبار واجهات برمجة التطبيقات وفهم كيفية عملها.  

**الفئات المستهدفة:**  

- المطوّرون المبتدئون الراغبون في تعلّم مبادئ REST APIs، وكذلك المطوّرون المتقدمون الذين يحتاجون إلى مرجع سريع أو أمثلة عملية.  
- فرق العمل التي تحتاج إلى مرجع تدريبي لتجربة وبناء طلبات واجهة برمجة التطبيقات.  

---

## 2. المتطلبات الأساسية

قبل البدء في استخدام واجهة Reqres.in، ينبغي التأكد من توافر مجموعة من المتطلبات التي تُمكّن المطوّر من تنفيذ الطلبات (Requests) ومعالجة الاستجابات (Responses) بكفاءة:  

- اتصال إنترنت مستقر لضمان تنفيذ جميع العمليات دون انقطاع.  
- أداة لاختبار واجهات برمجة التطبيقات (API Testing Tool) مثل Postman أو أي بديل مكافئ يتيح إنشاء الطلبات، إضافة الرؤوس (Headers)، إرسال البيانات عبر الجسم (Body)، واستعراض الاستجابات.  

> يمكن تحميل البرنامج من هنا: [Postman](https://www.postman.com/downloads/)  

- يمكن الاستعانة بأداة سطر أوامر (Command Line Tool) مثل cURL لاختبار الطلبات من خلال الطرفية (Terminal)، بينما يكفي للمبتدئين الاعتماد على أداة رسومية مثل Postman في المراحل الأولى.  
- يُفضل الإلمام بأساسيات REST APIs، بما في ذلك طرق HTTP Methods (GET، POST، PUT، PATCH، DELETE) والبنية العامة للطلبات والاستجابات.  
- معرفة برموز حالة (HTTP Status Codes) مثل:  
  - 200 (تم التنفيذ بنجاح)  
  - 201 (تم إنشاء مورد جديد)  
  - 400 (طلب غير صالح)  
  - 401 (غير مصرح)  
  - 404 (المورد غير موجود)  
- إلمام بكيفية التعامل مع JSON (JavaScript Object Notation)، باعتبارها الصيغة الأساسية لتبادل البيانات بين العميل والخادم.  

---

## 3. نظرة عامة وطبيعة الواجهة (Reqres.in)

<p dir="rtl">
Reqres.in هي واجهة برمجة تطبيقات تجريبية (Mock API) تتيح للمطوّرين اختبار مفاهيم REST APIs في بيئة آمنة ومجانية. صُمِّمت هذه الواجهة لمحاكاة سلوك أنظمة حقيقية دون الحاجة إلى إعداد خوادم أو قواعد بيانات.
</p>

---

</div>


**<span dir="rtl">المزايا الرئيسية:</span>**

- <span dir="rtl">مجانية بالكامل ولا تتطلّب إنشاء حساب</span>.

- <span dir="rtl">تدعم العمليات الأساسية</span> (CRUD)
  <span dir="rtl">عبر طرق</span> HTTP Methods<span dir="rtl">.</span>

- <span dir="rtl">تُوفّر بيانات جاهزة للتعامل مع كيانات مثل</span> Users
  <span dir="rtl">و</span> Resources<span dir="rtl">.</span>

- <span dir="rtl">تدعم التصفّح</span> (Pagination) <span dir="rtl">وإرجاع
  رموز الحالة القياسية</span> (HTTP Status
  Codes)<span dir="rtl">.</span>

- <span dir="rtl">سهلة الاستخدام عبر أدوات رسومية مثل</span> Postman
  <span dir="rtl">أو عبر الطرفية باستخدام</span>
  cURL<span dir="rtl">.</span>

<span dir="rtl">**الموقع الرسمي**:</span> <https://reqres.in>

<span id="طبيعةوجهة" class="anchor"></span>**<span dir="rtl">3.1</span>
<span dir="rtl">طبيعة الواجهة التجريبية</span>**

- Reqres.in <span dir="rtl">ليست قاعدة بيانات فعلية؛ الغرض منها التدريب
  والعرض فقط</span>.

- <span dir="rtl">بعد تنفيذ</span> POST <span dir="rtl">وإنشاء
  معرّف</span> (id)<span dir="rtl">، قد لا تتمكّن من جلب نفس العنصر لاحقًا
  عبر</span> GET <span dir="rtl">قد تعود الاستجابة (404</span> Not
  Found<span dir="rtl">).</span>

- <span dir="rtl">هذا السلوك متعمّد للتجارب وليس خللًا</span>.

**<span dir="rtl">حدود الاستخدام</span> (Rate Limits)**

- <span dir="rtl">قد تُحاكي الواجهة قيودًا على المعدّل (429</span>Too Many
  Requests <span dir="rtl">).</span>

- <span dir="rtl">عند ظهور 429، يُنصح بالانتظار فترة قصيرة ثم إعادة
  المحاولة</span>.

<span id="افضلممارسات"
class="anchor"></span>**<span dir="rtl">3.2</span> <span dir="rtl">أفضل
ممارسات الاختبار</span>**

- <span dir="rtl">استخدم معرّفات ثابتة في أمثلة القراءة مثل:</span> GET
  /api/users/2)<span dir="rtl">).</span>

- <span dir="rtl">افصل بين اختبارات القراءة</span> (GET)
  <span dir="rtl">والكتابة</span> (POST/PUT/PATCH/DELETE)
  <span dir="rtl">لتتبّع النتائج بسهولة</span>.

- <span dir="rtl">احتفظ بقوالب جاهزة للطلبات</span> (Postman Collection)
  <span dir="rtl">لتسريع الاختبارات المتكررة</span>.

4.  <span id="المصادقة" class="anchor"></span>**<span dir="rtl">المصادقة
    (</span>Authentication / Login<span dir="rtl">)</span>**

**4**<span id="هدفمصادقة" class="anchor"></span>**.1
<span dir="rtl">الهدف من المصادقة</span>**  
<span dir="rtl">التحقّق من هوية المستخدم والحصول على رمز أمني</span>
(Token) <span dir="rtl">لاستخدامه في تفويض الطلبات اللاحقة</span>.

<span id="ارسالطلبتس" class="anchor"></span>**4.2 <span dir="rtl">إرسال
طلب تسجيل الدخول</span>**

- <span dir="rtl">الطريقة (</span>Method<span dir="rtl">):</span> POST

- <span dir="rtl">المسار</span> /api/login :(Endpoint)
  <span dir="rtl"></span>

- <span dir="rtl">الرؤوس</span> Content-Type: application/json
  :(Headers)

- <span dir="rtl">الجسم</span>
  <span dir="rtl"></span>(Body)<span dir="rtl">:</span>JSON

{

"email": "eve.holt@reqres.in",

"password": "Ahmed1-Viper@1stPass"

}

![](./media/image2.png)

<span id="استجابةمتوقع" class="anchor"></span>**4.3
<span dir="rtl">الاستجابة المتوقعة</span>**

- **<span dir="rtl">عند النجاح</span> :(OK) <span dir="rtl"></span>200
  <span dir="rtl"></span>**

![](./media/image3.png)

- **<span dir="rtl">في حال الفشل</span>:**

  - <span dir="rtl">(بيانات ناقصة أو غير صحيحة)</span> 400 Bad Request

  - <span dir="rtl">(غير مصرح) 401</span> Unauthorized

<span id="استخدامتوكن" class="anchor"></span>**4.4
<span dir="rtl">استخدام الـ</span> Token <span dir="rtl">في الطلبات
اللاحقة</span>**

- <span dir="rtl">الطريقة العامة (إضافة يدويا فى الـ</span>
  Headers<span dir="rtl">)</span>

  - Authorization: Bearer \<token\>

<img src="./media/image4.png" style="width:4.76852in;height:1.53704in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-24 220352.png" />

- <span dir="rtl">الطريقة البديلة فى</span> Postman
  <span dir="rtl">(اختر طريقة واحدة اى تضع القيمه فى</span> Headers
  <span dir="rtl">أو من</span> Auth Type<span dir="rtl">)</span>

  - <span dir="rtl">عبر تبويب</span> Headers:

> Authorization: Bearer \<token\> <span dir="rtl"></span>

- <span dir="rtl">أو عبر تبويب</span> Auth:

> Type: Bearer Token <span dir="rtl"></span>
>
> <span dir="rtl">ثم إدخال قيمة الـ</span> Token
> <span dir="rtl">المستلمة</span>.

![](./media/image5.png)

<span id="ملاحظاتمهمه" class="anchor"></span>**4.5
<span dir="rtl">ملاحظات مهمة</span>**

- <span dir="rtl">بما أنّ</span> Reqres.in <span dir="rtl">واجهة تجريبية،
  بعض الطلبات قد تعمل دون الحاجة إلى</span>
  Token<span dir="rtl">.</span>

- <span dir="rtl">يبقى الـ</span> Token <span dir="rtl">صالحًا ما لم
  يتغيّر</span>.

- <span dir="rtl">لا حاجة لإرسال</span> Body <span dir="rtl">مع
  طلبات</span> Get<span dir="rtl">.</span>

- **<span dir="rtl">الطلبات تتطلّب إضافة</span> API Key
  <span dir="rtl">في الهيدر</span>:  
  x-api-key: reqres-free-v1**

![](./media/image6.png)

5.  <span id="عملياتاساسى"
    class="anchor"></span>**<span dir="rtl">العمليات الأساسية</span>
    (CRUD)<span dir="rtl">باستخدام برنامج</span> Postman**

<span dir="rtl">يوضّح هذا القسم كيفية تنفيذ العمليات الأساسية على الموارد
(المستخدمين والمصادر) باستخدام واجهة</span> Reqres.in.  
<span dir="rtl">كل عملية مرفقة بخطوات التنفيذ، مقتطف</span> JSON
<span dir="rtl">مبسّط، وصورة</span> Postman <span dir="rtl">توضّح الطلب
والاستجابة</span>.

<span id="جلببيانات1"
class="anchor"></span>**<span dir="rtl">5.1</span>GET
<span dir="rtl"></span>– <span dir="rtl">جلب البيانات</span>**

<span dir="rtl">**الهدف:** استدعاء بيانات من الخادم: إمّا قائمة
المستخدمين أو مستخدم واحد</span>.

**5.1.2 <span dir="rtl">جلب قائمة المستخدمين</span>**

- Method: GET

- Endpoint: /api/users?page=2

- Headers: Content-Type: application/json

- <span dir="rtl">غير مطلوب</span>Body:

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image7.png)

**5.1.3 <span dir="rtl">جلب مستخدم واحد</span>**

- Method: GET

- Endpoint: /api/users/2

- Headers: Content-Type: application/json

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image8.png)

- <span dir="rtl">في حال لم يُعثر على المستخدم</span> 404 Not
  Found<span dir="rtl">.</span>

<span id="انشاءبيانان2" class="anchor"></span>**5.2
<span dir="rtl"></span>POST <span dir="rtl"></span>–
<span dir="rtl">إنشاء بيانات جديدة</span>**

<span dir="rtl">الهدف: إرسال بيانات جديدة إلى الخادم لإنشاء
مستخدم</span>.

- Method: POST

- Endpoint: /api/users

- Headers: Content-Type: application/json

{

"name": "Ahmed Mousa",

"job": "Tech Writer"

}

**<span dir="rtl">استجابة متوقعة</span> :(Created)
<span dir="rtl">201</span>**

![](./media/image9.png)

<span id="تعديلبيان3" class="anchor"></span>**5.3
<span dir="rtl"></span> – PUT<span dir="rtl">تعديل كامل
للبيانات</span>**

<span dir="rtl">الهدف: تحديث بيانات مستخدم بشكل كامل (استبدال القيم
القديمة بقيم جديدة</span>).

- Method: PUT

- Endpoint: /api/users/2

{

"name": "Ahmed Hamdy",

"job": "Tech Writer Lead"

}

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image10.png)

<span id="تعديلجزئي4" class="anchor"></span>**5.4
<span dir="rtl"></span>– PATCH <span dir="rtl">تعديل جزئي
للبيانات</span>**

<span dir="rtl">الهدف: تحديث جزء محدد من بيانات المستخدم</span>.

- Method: PATCH

- Endpoint: /api/users/2

{

"job": "Principal Technical Writer"

}

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image11.png)

<span id="حذفبيانات5" class="anchor"></span>**5.5
<span dir="rtl"></span>DELETE <span dir="rtl"></span>–
<span dir="rtl">حذف البيانات</span>**

<span dir="rtl">الهدف: حذف مستخدم بشكل نهائي</span>.

- Method: DELETE

- Endpoint: /api/users/2

- <span dir="rtl">غير مطلوب</span>Headers / Body:

**<span dir="rtl">استجابة متوقعة</span> No Content
<span dir="rtl">204</span>**

<img src="./media/image12.png" style="width:4.79408in;height:2.81345in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 202115.png" />

<span id="عاساسيةعريسورس"
class="anchor"></span>**<span dir="rtl">6.</span>
<span dir="rtl">العمليات الأساسية على</span> (Resources)**

<span id="جلب61" class="anchor"></span>**6.1 <span dir="rtl"></span>
GET<span dir="rtl">جلب قائمة الموارد</span>**

<span dir="rtl">الهدف: جلب قائمة</span> Resources <span dir="rtl">مع دعم
التصفّح</span> (Pagination)<span dir="rtl">.</span>

<span dir="rtl">تفاصيل الطلب</span>

- Method: GET

- Endpoint: /api/unknown?page=1

- <span dir="rtl">غير مطلوبين</span> Headers & Body:

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image13.png)

**<span dir="rtl">ملاحظات مهمة</span>**

- <span dir="rtl">مفاتيح التصفّح:</span> page, per_page, total,
  total_pages

- <span dir="rtl">يمكن تغيير الصفحة باستخدام معاملات الاستعلام</span>
  (Query Parameters) <span dir="rtl">مثل</span> ?page=2

<span id="جلب62" class="anchor"></span>**6.2 <span dir="rtl"></span>GET
<span dir="rtl"></span>– <span dir="rtl">جلب مورد واحد</span>**

<span dir="rtl">الهدف: جلب</span> Resource <span dir="rtl">واحد باستخدام
المعرّف</span> (ID).

<span dir="rtl">تفاصيل الطلب</span>

- Method: GET

- Endpoint: /api/unknown/2

- <span dir="rtl">غير مطلوبين</span> Headers & Body:

**<span dir="rtl">استجابة متوقعة</span> :(OK)
<span dir="rtl">200</span>**

![](./media/image14.png)

**<span dir="rtl">في حال عدم العثور</span>**

- **404 Not Found** <span dir="rtl">عند استخدام معرّف غير موجود</span>.

![](./media/image15.png)

<span id="امثلة7" class="anchor"></span>**<span dir="rtl">7.</span>
<span dir="rtl">أمثلة باستخدام أمر</span> curl**

<span dir="rtl">يمكن نسخ الأمر ثم لصقة فى سطر الأوامر</span>
CMD<span dir="rtl">.</span>

<span id="مصاد71" class="anchor"></span>**<span dir="rtl">7.1</span>
<span dir="rtl">المصادقة</span> (Authentication / Login)**

**cURL:**

curl -X POST "https://reqres.in/api/login" -H "Content-Type:
application/json" -H "x-api-key: reqres-free-v1" -d
"{\\email\\:\\eve.holt@reqres.in\\,\\password\\:\\AhmedTheBest\\}"

<img src="./media/image16.png" style="width:6.5in;height:1.05556in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 203950.png" />**<span dir="rtl">استجابة
متوقعة</span> 200 :(OK)**

<span id="مصا72" class="anchor"></span>**<span dir="rtl">7.2</span>GET
<span dir="rtl"></span>– <span dir="rtl">جلب مستخدم</span>**

> **cURL:**
>
> <img src="./media/image17.png" style="width:6.49097in;height:0.96319in"
> alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 210044.png" />curl
> "https://reqres.in/api/users/2" -H "x-api-key: reqres-free-v1"

**<span dir="rtl">جلب المستخدمين</span>**

**cURL:**

curl "https://reqres.in/api/users?page=2" -H "x-api-key: reqres-free-v1"

<img src="./media/image18.png" style="width:6.5in;height:1.76875in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 205809.png" />

<span id="مصا73" class="anchor"></span>**<span dir="rtl">7.3</span>POST
<span dir="rtl"></span>– <span dir="rtl">إنشاء مستخدم</span>**

**cURL:**

curl -X POST "https://reqres.in/api/users" -H "Content-Type:
application/json" -H "x-api-key: reqres-free-v1" -d
"{\\name\\:\\Ahmed\\,\\job\\:\\Developer\\}"

<img src="./media/image19.png" style="width:6.49097in;height:0.83333in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 204807.png" />

<span id="مصا74" class="anchor"></span>**<span dir="rtl">7.4</span>PUT
<span dir="rtl"></span>– <span dir="rtl">تعديل كامل</span>**

**cURL:**

curl -X PUT "https://reqres.in/api/users/2" -H "Content-Type:
application/json" -H "x-api-key: reqres-free-v1" -d
"{\\name\\:\\Ahmed\\,\\job\\:\\Senior Dev\\}"

<img src="./media/image20.png" style="width:6.49097in;height:0.81458in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 205018.png" />

<span id="مصا75" class="anchor"></span>**<span dir="rtl">7.5</span>PATCH
<span dir="rtl"></span>– <span dir="rtl">تعديل جزئي</span>**

**cURL:**

curl -X PATCH "https://reqres.in/api/users/2" -H "Content-Type:
application/json" -H "x-api-key: reqres-free-v1" -d "{\\job\\:\\Tech
Lead\\}"

<img src="./media/image21.png" style="width:6.5in;height:0.79653in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 205337.png" />

<span id="مصا76"
class="anchor"></span>**<span dir="rtl">7.6</span>DELETE
<span dir="rtl"></span>– <span dir="rtl">حذف</span>**

**cURL:**

curl -X DELETE "https://reqres.in/api/users/2" -H "x-api-key:
reqres-free-v1"

**<span dir="rtl">استجابة متوقعة:</span>204 No Content**
<img src="./media/image22.png" style="width:6.49097in;height:0.69444in"
alt="C:\Users\engra\AppData\Local\Microsoft\Windows\INetCache\Content.Word\Screenshot 2025-09-25 205604.png" />

**<span dir="rtl">التفكيك والشرح</span>:**

1.  **curl**

    - <span dir="rtl">هذا البرنامج هو أداة لعمل طلبات</span> HTTP (GET /
      POST / PUT / PATCH / DELETE) <span dir="rtl"></span>

2.  **-X POST**

    - -X <span dir="rtl">معناها: نوع الطريقة اللي هتستخدمه</span> (HTTP
      Method) <span dir="rtl"></span>

    - <span dir="rtl">هنا اخترنا</span> POST

    - <span dir="rtl">يمكن أن يكون</span>:

      - GET <span dir="rtl">جلب بيانات</span>

      - POST <span dir="rtl">إرسال بيانات جديدة</span>

      - PUT <span dir="rtl">تحديث كامل</span>

      - PATCH <span dir="rtl">تحديث جزئي</span>

      - DELETE <span dir="rtl">حذف</span>

3.  **"https://reqres.in/api/login"**

    - <span dir="rtl">ده الـمسار
      (</span>Endpoint<span dir="rtl">)</span> <span dir="rtl">اللي
      هيتبعتله الطلب</span>.

    - <span dir="rtl">في المثال</span> /api/login
      <span dir="rtl"></span>

4.  **-H "Content-Type: application/json"**

    - -H <span dir="rtl">معناها</span> Header <span dir="rtl"></span>

    - <span dir="rtl">الـ</span> Header <span dir="rtl">بيتكتب كـ</span>
      Name: Value

    - <span dir="rtl">هنا معناه إن جسم الطلب</span> (Body)
      <span dir="rtl">مكتوب بصيغة</span> JSON

    - <span dir="rtl">مكان</span> Value <span dir="rtl">ممكن تحط أي قيمة
      لازمة زي</span> application/xml <span dir="rtl">لو</span> XML

5.  **-H "x-api-key: reqres-free-v1"**

    - <span dir="rtl">مثال على هيدر تاني</span>.

    - <span dir="rtl">هنا اسمه</span> x-api-key<span dir="rtl">،
      وقيمته</span> reqres-free-v1

    - <span dir="rtl">أنت تغيّر الجزء ده لو عندك</span> API Key
      <span dir="rtl">مختلف</span>.

6.  **-d
    "{\\email\\:\\your_email@example.com\\,\\password\\:\\your_password\\}"**

    - -d <span dir="rtl">معناها</span>: <span dir="rtl">بيانات الجسم
      اللي هيتبعت في الطلب.</span>

    - <span dir="rtl">لازم يكون مكتوب بصيغة</span> JSON
      <span dir="rtl">لو الـ</span> API <span dir="rtl">بيطلب
      كده.</span>

    - <span dir="rtl">في المثال</span>:

      - email: <span dir="rtl">هنا تكتب إيميلك</span>.

      - password: <span dir="rtl">هنا تكتب الباسورد</span>.

    - <span dir="rtl">لو الطلب ما يحتاجش</span> Body
      <span dir="rtl">مثل</span> GET <span dir="rtl">لا تكتب</span> -d

**<span dir="rtl">الخلاصة العملية</span>:**

- **-X** <span dir="rtl">هو نوع العملية</span> .(GET/POST/PUT/DELETE)
  <span dir="rtl"></span>

- **-H** <span dir="rtl">هو بيانات</span> Header <span dir="rtl">دايما
  اسم:قيمة</span>Name: Value <span dir="rtl">مثل</span> Content-Type
  <span dir="rtl">أو</span> .Authorization <span dir="rtl"></span>

- **-d** <span dir="rtl">هو بيانات</span> Body <span dir="rtl">تبعتها في
  شكل</span> .JSON

<span id="معالجه8" class="anchor"></span>**<span dir="rtl">8. معالجة
الأخطاء</span> (Error Handling)**

<span id="معال81" class="anchor"></span>**<span dir="rtl">8.1 مبادئ
عامة</span>**

- <span dir="rtl">تُرجِع الواجهة رموز حالة</span> (HTTP Status Codes)
  <span dir="rtl">قياسية توضّح نتيجة الطلب</span>.

- <span dir="rtl">تُعرَض تفاصيل الخطأ –عند توفّرها– في الاستجابة</span>
  (Response) <span dir="rtl">بصيغة</span> JSON <span dir="rtl">ليسهل
  قراءتها ومعالجتها برمجيًا</span>.

- <span dir="rtl">يجب دائمًا قراءة الرمز والنص المصاحب له لتحديد الإجراء
  المناسب (تصحيح الطلب، إعادة المحاولة، المصادقة… إلخ).</span>

<span id="معا82" class="anchor"></span>**<span dir="rtl">8.2 رموز الحالة
الشائعة</span>**

- 200 OK <span dir="rtl">: نجاح الطلب</span> (GET / PUT / PATCH)

- 201 Created<span dir="rtl">: تم إنشاء مورد جديد</span> (POST)
  <span dir="rtl"></span>

- 204 No Content<span dir="rtl">: نجاح بدون جسم استجابة</span> (DELETE)

- 400 Bad Request <span dir="rtl">: جسم أو صيغة طلب غير صحيحة</span>.

- 401 Unauthorized <span dir="rtl">: نقص المصادقة أو</span> Token
  <span dir="rtl">غير صالح</span>.

- 404 Not Found <span dir="rtl">: المورد غير موجود مثل</span> (GET
  /api/users/23) <span dir="rtl"></span>

- 429 Too Many Requests <span dir="rtl">: تجاوز حدّ المعدّل</span> (Rate
  Limit) – <span dir="rtl">إن وُجد</span>.

- 500 Internal Server Error<span dir="rtl">: خطأ عام في الخادم</span>.

<span id="معا83" class="anchor"></span>**<span dir="rtl">8.3 مسار تشخيص
سريع</span> (Troubleshooting)**

- <span dir="rtl">تحقّق من</span> Method <span dir="rtl">و</span>Endpoint
  <span dir="rtl">ومن الأخطاء الشائعة: كتابة</span> GET
  <span dir="rtl">في شريط العنوان بدل اختياره من القائمة.</span>

- <span dir="rtl">راجع</span> Headers <span dir="rtl">المطلوبة
  (مثل</span> Content-Type: application/json <span dir="rtl">و</span>
  Authorization: Bearer \<token\> <span dir="rtl">عند الحاجة)</span>

- <span dir="rtl">تأكّد من أن</span> Body <span dir="rtl">مكتوب
  بصيغة</span> JSON <span dir="rtl">صحيحة، و وجود الحقول الإلزامية (مثل
  البريد الإلكتروني/كلمة المرور في تسجيل الدخول</span>(

- <span dir="rtl">جرّب بمعرّفات صحيحة: بعض المعرّفات في</span> Reqres.in
  <span dir="rtl">ثابتة (مثل المستخدم 2)، بينما المعرّفات المُنشأة تجريبيًا
  قد لا تبقى محفوظة</span>.

- <span dir="rtl">راقب أولًا</span> Status Code <span dir="rtl">ثم نصّ
  الخطأ لتحديد الإجراء المناسب (إعادة الإرسال، تعديل المدخلات،
  إضافة</span> (Token

<span id="افض84" class="anchor"></span>**<span dir="rtl">8.4</span>
<span dir="rtl">أفضل ممارسات التعامل مع الأخطاء في العميل</span>
(Client)**

- <span dir="rtl">أظهر رسالة واضحة للمستخدم النهائي مشتقّة من</span>
  Status Code<span dir="rtl">.</span>

- <span dir="rtl">لا تفترض نجاح الطلب؛ افحص الرمز دائمًا قبل استخدام
  البيانات</span>.

- <span dir="rtl">أعد المحاولة تلقائيًا فقط في الحالات المناسبة (مثل
  مشاكل الشبكة، وليس عند</span> 400 Bad Request<span dir="rtl">)</span>

- <span dir="rtl">سجّل تفاصيل الخطأ</span> (Logging)
  <span dir="rtl">لأغراض التشخيص والمتابعة</span>.

<span id="تص9" class="anchor"></span>**<span dir="rtl">9.</span>
<span dir="rtl">التصفّح</span> (Pagination)**

<span dir="rtl">الهدف**:** تنظيم النتائج على صفحات متتالية لتقليل حجم
الاستجابة وتسهيل العرض والتنقّل</span>.

<span dir="rtl">طريقة الاستخدام (قائمة المستخدمين مثالًا)</span>

- (Method): GET

- (Endpoint): /api/users?page=2

- (Query Parameters):

  - page <span dir="rtl">لتحديد الصفحة المطلوبة</span>.

**<span dir="rtl">الاستجابة المتوقّعة</span> 200 :(OK)**

{

"page": 2,

"per_page": 6,

"total": 12,

"total_pages": 2,

"data": \[ /\* <span dir="rtl">عناصر الصفحة</span> \*/ \]

}

**<span dir="rtl">ملاحظات مهمة</span>**

- <span dir="rtl">يمكن الانتقال بين الصفحات بتغيير قيمة</span>page
  <span dir="rtl">مثل</span> ?page=1, ?page=2

- <span dir="rtl">عدد العناصر في الصفحة</span> (per_page)
  <span dir="rtl">ثابت في</span>Reqres.in <span dir="rtl">لأغراض العرض،
  لكنه قد يختلف في واجهات حقيقية</span>.

- <span dir="rtl">في نهاية الصفحات، قد تعود الاستجابة بحقل</span>data
  <span dir="rtl">فارغ دون أن يكون ذلك خطأ</span>.

<span id="ملاح10" class="anchor"></span>**<span dir="rtl">10.
الملاحق</span>**

<span id="مصطلح101" class="anchor"></span>**<span dir="rtl">10.1 مصطلحات
موحّدة</span>**

- :Token <span dir="rtl">رمز أمني يُستخدم لتفويض الطلبات</span>.

- HTTP Methods: GET, POST, PUT, PATCH, DELETE.

- HTTP Status Codes: 200, 201, 204, 400, 401, 404, 429, 500.

- Requests / Responses <span dir="rtl">طلبات / استجابات</span>.

- JSON (JavaScript Object Notation) <span dir="rtl">صيغة لتبادل البيانات
  بين العميل والخادم</span>.

<span id="روابط102" class="anchor"></span>**<span dir="rtl">10.2 روابط
مفيدة</span>**

- **<span dir="rtl">الموقع الرسمي:</span> <https://reqres.in>**

- **<span dir="rtl">تحميل</span>:Postman <span dir="rtl"></span>
  <https://www.postman.com/downloads/>**

- **<span dir="rtl">شرح فلسفة</span> RESTful API
  <span dir="rtl">بالعربية من حسوب:</span> [Hsoub in
  Arabic](https://academy.hsoub.com/programming/general/شرح-فلسفة-restful-تعلم-كيف-تبني-واجهات-rest-البرمجية-r635/)**

- **<span dir="rtl">تعلم اساسيات</span> :RESTful API
  <span dir="rtl"></span>[https://restfulapi.net<span dir="rtl">/</span>](https://restfulapi.net/)**
























