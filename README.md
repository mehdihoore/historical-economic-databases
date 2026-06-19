<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>دیتابیس‌های مرجع تاریخ اقتصادی، نهادها و سنجش کمی</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: 'Segoe UI', Tahoma, 'Noto Sans Arabic', sans-serif;
      background: #0d1117;
      color: #c9d1d9;
      direction: rtl;
      text-align: right;
      line-height: 1.9;
      font-size: 15px;
      padding: 0 0 60px 0;
    }

    .page-header {
      background: linear-gradient(135deg, #161b22 0%, #1a2332 100%);
      border-bottom: 1px solid #30363d;
      padding: 40px 48px 32px 48px;
      margin-bottom: 40px;
    }

    h1 {
      font-size: 1.75rem;
      font-weight: 700;
      color: #e6edf3;
      margin-bottom: 14px;
    }

    .intro-text {
      color: #8b949e;
      max-width: 820px;
      font-size: 14px;
      line-height: 1.8;
    }

    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* ── بخش‌بندی ── */
    .section {
      margin-bottom: 48px;
    }

    h2 {
      font-size: 1.15rem;
      font-weight: 700;
      color: #e6edf3;
      border-bottom: 2px solid #21262d;
      padding-bottom: 10px;
      margin-bottom: 24px;
    }

    /* ── کارت هر دیتابیس ── */
    .db-card {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 8px;
      padding: 22px 26px;
      margin-bottom: 16px;
      transition: border-color .2s;
    }

    .db-card:hover {
      border-color: #58a6ff;
    }

    .db-title {
      font-size: 1.05rem;
      font-weight: 700;
      color: #e6edf3;
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      flex-direction: row-reverse;
      justify-content: flex-end;
    }

    .db-num {
      background: #21262d;
      color: #8b949e;
      font-size: 12px;
      font-weight: 600;
      padding: 2px 8px;
      border-radius: 12px;
      flex-shrink: 0;
    }

    /* ── ردیف‌های داخلی ── */
    .db-row {
      display: flex;
      gap: 0;
      margin-bottom: 10px;
      direction: rtl;
    }

    .db-label {
      font-weight: 700;
      color: #79c0ff;
      white-space: nowrap;
      flex-shrink: 0;
      min-width: 110px;
      font-size: 13.5px;
    }

    .db-content {
      color: #c9d1d9;
      font-size: 14px;
      line-height: 1.75;
      flex: 1;
    }

    /* ── لیست متغیرها ── */
    .var-list {
      list-style: none;
      padding: 0;
      margin: 4px 0 0 0;
      direction: rtl;
    }

    .var-list li {
      padding: 4px 0;
      font-size: 13.5px;
      color: #c9d1d9;
      display: flex;
      align-items: flex-start;
      gap: 8px;
      direction: rtl;
    }

    .var-list li::before {
      content: "◂";
      color: #58a6ff;
      flex-shrink: 0;
      margin-top: 2px;
      font-size: 11px;
    }

    code {
      background: #1c2129;
      border: 1px solid #30363d;
      border-radius: 4px;
      padding: 1px 6px;
      font-family: 'Consolas', 'Courier New', monospace;
      font-size: 12.5px;
      color: #f0883e;
      direction: ltr;
      display: inline-block;
    }

    /* ── لینک ── */
    .db-link {
      margin-top: 10px;
    }

    .db-link a {
      color: #58a6ff;
      text-decoration: none;
      font-size: 13px;
    }

    .db-link a:hover {
      text-decoration: underline;
    }

    /* ── نکته ── */
    .db-note {
      background: #1a2332;
      border-right: 3px solid #f0883e;
      border-radius: 0 4px 4px 0;
      padding: 8px 12px;
      font-size: 13px;
      color: #c9d1d9;
      margin-top: 8px;
    }

    /* ── بخش مشارکت ── */
    .contribution {
      background: #161b22;
      border: 1px solid #30363d;
      border-radius: 8px;
      padding: 24px 28px;
      margin-top: 40px;
    }

    .contribution h2 {
      border: none;
      margin-bottom: 14px;
    }

    .contrib-list {
      list-style: none;
      padding: 0;
      counter-reset: step;
    }

    .contrib-list li {
      counter-increment: step;
      display: flex;
      gap: 12px;
      align-items: flex-start;
      padding: 8px 0;
      font-size: 14px;
      color: #c9d1d9;
      direction: rtl;
    }

    .contrib-list li::before {
      content: counter(step);
      background: #21262d;
      color: #58a6ff;
      font-weight: 700;
      border-radius: 50%;
      width: 22px;
      height: 22px;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
      font-size: 12px;
      margin-top: 2px;
    }

    hr {
      border: none;
      border-top: 1px solid #21262d;
      margin: 32px 0;
    }

    strong { color: #e6edf3; }
  </style>
</head>
<body>

<div class="page-header">
  <div class="container">
    <h1>📚 دیتابیس‌های مرجع تاریخ اقتصادی، نهادها و سنجش کمی (Cliometrics)</h1>
    <p class="intro-text">
      این مخزن یک راهنمای کاربردی و طبقه‌بندی‌شده به زبان فارسی است که پایگاه‌های داده آنلاین و کلان‌داده‌های تاریخی را معرفی می‌کند. این دیتابیس‌ها ابزارهای اصلی اقتصاددانان سیاسی، مورخان محاسباتی و پژوهشگران (از جمله فیلیپ تی. هافمن در تحلیل‌هایش پیرامون ریشه‌های رشد اقتصادی و تکنولوژی نظامی) برای سنجش فرضیات تاریخی هستند. در این راهنما، علاوه بر معرفی هر پایگاه، متغیرهای کلیدی درون فایل‌های داده و روش‌شناسی کاربردی آن‌ها تشریح شده است.
    </p>
  </div>
</div>

<div class="container">

  <!-- ═══ بخش ۱ ═══ -->
  <div class="section">
    <h2>📊 دیتابیس‌های کلان‌اقتصادی، معیشت و توزیع ثروت</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱</span> پروژه مدیسون (Maddison Project Database)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">معتبرترین پروژه آکادمیک جهان برای بازسازی و تخمین جمعیت، GDP و تولید ناخالص داخلی سرانه کشورها از دوران باستان تا به امروز.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">این پروژه از شاخص «برابری قدرت خرید با مبنای دلاری ثابت» (PPP) استفاده می‌کند تا تفاوت‌های نرخ ارز را خنثی کند. در دوره‌های پیش از قرن بیستم، داده‌ها بر اساس برآوردهای مورخان محلی زنجیره‌سازی (Interpolate) شده‌اند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>countrycode</code>: کد ۳ حرفی استاندارد ایزو برای کشورها (مثلاً <code>IRN</code> برای ایران).</li>
          <li><code>year</code>: سال مورد بررسی (از سال ۱ میلادی تا کنون).</li>
          <li><code>gdppc</code>: تولید ناخالص داخلی سرانه بر اساس دلار ثابت سال ۲۰۱۱ (مبنای سنجش رفاه تاریخی).</li>
          <li><code>pop</code>: جمعیت کشور به هزار نفر.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای تحلیل‌های مقایسه‌ای بلندمدت و بررسی پدیده «واگرایی بزرگ» (Great Divergence) میان شرق و غرب از متغیر <code>gdppc</code> استفاده می‌شود.</span></div>
      <div class="db-link">🔗 <a href="https://www.rug.nl/ggdc/historicaldevelopment/maddison/" target="_blank">Maddison Project Database</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۲</span> گروه تاریخچه قیمت‌ها و درآمدهای جهانی (GPIH)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">این پایگاه داده حاوی قیمت‌های تاریخی کالاها، نرخ تبدیل دستمزدها به نقره و قدرت خرید روزمره مردم از قرون وسطی تا قرن بیستم در شهرهای بزرگ جهان است.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">برای رفع مشکل تنوع بی‌پایان ارزها و واحدهای اندازه‌گیری قدیمی (مانند پوند، من، خروار، رئال)، تمام قیمت‌ها بر اساس وزن نقره به کار رفته در سکه‌های محلی در آن سال به «گرم نقره» تبدیل شده‌اند تا قابلیت مقایسه جهانی داشته باشند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>City</code>: شهری که داده‌ها از آن استخراج شده است.</li>
          <li><code>Commodity</code>: نوع کالا (مانند گندم، برنج، زغال‌سنگ، دستمزد نیروی کار).</li>
          <li><code>Price in local currency</code>: قیمت به ارز محلی در همان دوره.</li>
          <li><code>Price in silver (grams)</code>: معادل قیمت کالا به گرم نقره خالص.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">با تقسیم دستمزد اسمی یک کارگر (به گرم نقره) بر قیمت سبد مصرفی او (شامل غلات، سوخت و منسوجات)، می‌توانید «شاخص رفاه» (Welfare Ratio) را برای سنجش فقر تاریخی محاسبه کنید.</span></div>
      <div class="db-link">🔗 <a href="https://gpih.ucdavis.edu/" target="_blank">Global Price and Income History Group</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۳</span> دیتابیس کلان‌تاریخ ژوردا-شولاریک-تیلور (JST Macrohistory Database)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">یکی از غنی‌ترین منابع برای بررسی تحولات کلان اقتصادی، بانکی و مالی بلندمدت در ۱۷ اقتصاد پیشرفته جهان از سال ۱۸۷۰ به بعد. این دیتابیس شامل ۴۵ متغیر اسمی و واقعی است و بیش از ۹۰ درصد از خروجی کشورهای پیشرفته را پوشش می‌دهد.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">این پروژه داده‌های سالانه کلان اقتصادی را که پیش از این به صورت پراکنده در آرشیو بانک‌های مرکزی پنهان بود، همگن‌سازی کرده است.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>gdp</code>: تولید ناخالص داخلی اسمی.</li>
          <li><code>loans</code>: کل اعتبارات و وام‌های بانکی اعطاشده به بخش خصوصی غیرمالی (سنجش اهرم مالی جامعه).</li>
          <li><code>hp</code>: شاخص قیمت مسکن (برای بررسی حباب‌های ملکی تاریخی).</li>
          <li><code>bill_rate</code>: نرخ بهره کوتاه‌مدت.</li>
          <li><code>rrequity</code> / <code>rrhousin</code>: نرخ بازده واقعی بلندمدت سهام و مسکن (افزوده شده در نسخه‌های اخیر).</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">اقتصاددانان سیاسی از نسبت متغیر <code>loans</code> به <code>gdp</code> برای ارزیابی اینکه آیا رشد سریع اعتبارات بانکی پیش‌بینی‌کننده بحران‌های مالی بزرگ (مانند رکود بزرگ ۱۹۲۹ یا بحران ۲۰۰۸) بوده است یا خیر، استفاده می‌کنند.</span></div>
      <div class="db-note">⚠️ <strong>نکته ارجاع:</strong> هنگام استفاده از داده‌های نرخ بازده، باید علاوه بر مقاله اصلی JST، مقاله ژوردا، نول، کووسینوف، شولاریک و تیلور (2019) در QJE را نیز ارجاع دهید.</div>
      <div class="db-link">🔗 <a href="https://www.macrohistory.net/" target="_blank">JST Macrohistory Database</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۴</span> پایگاه داده قیمت‌ها و دستمزدهای تاریخی مؤسسه بین‌المللی تاریخ اجتماعی (IISH)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">پروژه‌ای متعلق به مؤسسه بین‌المللی تاریخ اجتماعی هلند که روی قیمت‌ها و دستمزدهای دوره پیش از آمارهای رسمی مدرن (به‌ویژه پیش از سال ۱۹۱۴) در اروپا و آسیا تمرکز دارد.</span></div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">این دیتابیس مکمل بسیار خوبی برای داده‌های GPIH است و اطلاعات بسیار جزئی از بازارهای کار محلی، خیریه‌ها، اسناد صنفی و نوانخانه‌های قرون گذشته ارائه می‌دهد.</span></div>
      <div class="db-link">🔗 <a href="https://iisg.amsterdam/en/data/data-collections/historical-prices-and-wages" target="_blank">IISH Historical Prices and Wages</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۵</span> پایگاه داده ماکرو-تاریخی NBER (NBER Macrohistory Database)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">یکی از قدیمی‌ترین و جامع‌ترین مخازن داده‌های اقتصادی تاریخی که در دهه‌های اولیه فعالیت دفتر ملی تحقیقات اقتصادی آمریکا (NBER) گردآوری شده است. این دیتابیس بیش از ۳۰۰۰ سری زمانی تاریخی دارد که جنبه‌های مختلف اقتصادهای پیش از جنگ جهانی اول و دوران بین دو جنگ را پوشش می‌دهد.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">داده‌ها از اسناد آرشیوی دولتی، گزارش‌های بانک‌های مرکزی و سرشماری‌های صنعتی دوران پیش از مدرنیزاسیون آماری جمع‌آوری شده‌اند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li>تولید (Production): شاخص‌های تولید صنعتی بخش‌بندی‌شده.</li>
          <li>قیمت‌ها (Prices): شاخص‌های قیمت کالاهای مصرفی و صنعتی.</li>
          <li>دستمزدها (Wages): دستمزد روزانه و هفتگی بخش‌های مختلف.</li>
          <li>تجارت خارجی (Foreign Trade): واردات و صادرات کشورهای اصلی.</li>
          <li>فعالیت بانکی و پولی (Money): ذخایر طلا، انتشار اسکناس و وام‌های بانکی.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">پوشش جغرافیایی:</span><span class="db-content">عمدتاً آمریکا، انگلستان، فرانسه و آلمان، با برخی داده‌های ماهانه و فصلی.</span></div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای بازسازی چرخه‌های تجاری (Business Cycles) پیش از جنگ جهانی دوم و آزمون مدل‌های اقتصاد کلاسیک با داده‌های واقعی تاریخی.</span></div>
      <div class="db-link">🔗 <a href="https://www.nber.org/research/data/nber-macrohistory-database" target="_blank">NBER Macrohistory Database</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ بخش ۲ ═══ -->
  <div class="section">
    <h2>🏛️ دیتابیس‌های نهادهای سیاسی، قوانین اساسی و ظرفیت دولت‌ها</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۶</span> پروژه انواع دموکراسی (Varieties of Democracy — V-Dem)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">بزرگترین و دقیق‌ترین دیتابیس توصیفی و تحلیلی در مورد نهادهای سیاسی، دموکراسی و حاکمیت قانون در جهان که بازه زمانی ۱۷۸۹ تا کنون را با بیش از ۲۶۰ شاخص پوشش می‌دهد.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">V-Dem دموکراسی را به ۵ بعد اصلی (انتخاباتی، لیبرال، مشارکتی، مشورتی و برابرخواهانه) تقسیم می‌کند و از روش مدل‌سازی ارزیابی کارشناسان (Bayesian Item Response Theory) برای به حداقل رساندن خطای انسانی در ارزیابی‌ها استفاده می‌کند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>v2x_polyarchy</code>: شاخص دموکراسی انتخاباتی (پولی‌آرشی).</li>
          <li><code>v2x_libdem</code>: شاخص دموکراسی لیبرال (میزان محدودیت‌های قانون اساسی بر اکثریت و حفظ حقوق اقلیت).</li>
          <li><code>v2x_partip</code>: شاخص دموکراسی مشارکتی.</li>
          <li><code>v2x_egaldem</code>: شاخص دموکراسی برابرخواهانه.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">به دلیل حجم بسیار بالا (بیش از ۳۱ میلیون نقطه داده)، این دیتابیس برای تحلیل‌های رگرسیونی پنل (Panel Data Regression) در نرم‌افزارهای R یا Stata بسیار ایده‌آل است.</span></div>
      <div class="db-link">🔗 <a href="https://www.v-dem.net/" target="_blank">V-Dem Database</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۷</span> پروژه مقایسه قانون اساسی (Comparative Constitutions Project — CCP)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">این پروژه تمام قوانین اساسی نوشته شده در جهان را از سال ۱۷۸۹ میلادی تا کنون بر اساس معیارهای ساختار قدرت، حقوق شهروندی و نهادهای قانونی کدگذاری کرده است.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">هر قانون اساسی تاریخی توسط دو کدگذار به طور مستقل ارزیابی می‌شود تا پایایی داده‌ها حفظ شود.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>exec_power</code>: شاخص قدرت قوه مجریه (هرچه بالاتر باشد، اختیارات رئیس دولت بیشتر و کنترل پارلمان کمتر است).</li>
          <li><code>leg_power</code>: شاخص قدرت قانون‌گذاری پارلمان.</li>
          <li><code>jud_ind</code>: شاخص استقلال اساسی قوه قضاییه.</li>
          <li><code>num_rights</code>: تعداد کل حقوق به رسمیت شناخته‌شده شهروندان در قانون اساسی.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">این دیتابیس برای سنجش رابطه بین «حقوق مالکیت و محدودیت‌های قدرت حاکم» با «رشد اقتصادی بلندمدت» (بررسی فرضیات نهادگرایی جدید) کاربرد دارد.</span></div>
      <div class="db-link">🔗 <a href="https://comparativeconstitutionsproject.org/" target="_blank">Comparative Constitutions Project</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۸</span> پروژه پولیتی (Polity IV / Polity V)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">ارزیابی سالانه ویژگی‌های رژیم‌های سیاسی جهان و ساختار قدرت در آن‌ها از سال ۱۸۰۰ میلادی به بعد.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">این پروژه حکومت‌ها را بر اساس نحوه انتخاب قوه مجریه، میزان محدودیت‌های اعمال‌شده بر رهبران، و سطح مشارکت سیاسی مردم ارزیابی کرده و دو شاخص مجزا بین ۰ تا ۱۰ می‌سازد.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>DEMOC</code>: شاخص دموکراسی نهادینه‌شده (بین ۰ تا ۱۰).</li>
          <li><code>AUTOC</code>: شاخص اتوکراسی (استبداد) نهادینه‌شده (بین ۰ تا ۱۰).</li>
          <li><code>POLITY</code>: شاخص نهایی از فرمول <code>DEMOC − AUTOC</code>؛ دامنه از ۱۰− (استبداد مطلق) تا ۱۰+ (دموکراسی کامل).</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">در تحلیل‌های آماری، معمولاً مقدار شاخص POLITY به سه دسته تقسیم می‌شود: از ۱۰− تا ۶− (حکومت‌های مستبد)؛ از ۵− تا ۵+ (آنوکراسی)؛ و از ۶+ تا ۱۰+ (دموکراسی‌های کامل).</span></div>
      <div class="db-link">🔗 <a href="http://www.systemicpeace.org/" target="_blank">Center for Systemic Peace — Polity Project</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۹</span> دیتابیس تاریخ اقتصادی پروس (iPEHD)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">مجموعه‌ای از غنی‌ترین داده‌های آماری، مذهبی، آموزشی و ساختاری در سطح شهرستان‌ها (Kreis) برای قرن نوزدهم در پادشاهی پروس (بخش اصلی آلمان امروزی).</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">استفاده از مستندات سرشماری‌های بسیار دقیق و منظم دولتی پروس در قرن ۱۹.</span></div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">این دیتابیس برای ارزیابی فرضیات کلاسیک اقتصاد سیاسی (مانند نظریه ماکس وبر درباره اخلاق پروتستان و روح سرمایه‌داری) و سنجش اثر مذهب بر سواد و انباشت سرمایه انسانی استفاده می‌شود.</span></div>
      <div class="db-link">🔗 <a href="https://www.ifo.de/en/ipehd" target="_blank">ifo Prussian Economic History Database</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ بخش ۳ ═══ -->
  <div class="section">
    <h2>⚔️ دیتابیس‌های جنگ، بودجه‌های نظامی و توانمندی‌های دفاعی</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۰</span> پروژه همبسته‌های جنگ (Correlates of War — COW)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">مرجع استاندارد روابط بین‌الملل و تاریخ نظامی برای تحلیل جنگ‌ها، اتحادها و توانمندی‌های نظامی کشورها. کلیدی‌ترین بخش آن «دیتابیس توانمندی‌های مادی ملی» (NMC) است.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">شاخص نهایی این دیتابیس یعنی <strong>CINC</strong> بر اساس سهم نسبی هر کشور از ۶ مولفه اساسی مادی در کل جهان محاسبه می‌شود تا وزن واقعی قدرت هر کشور مشخص شود.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>milex</code>: مخارج نظامی کشور به هزار دلار آمریکا.</li>
          <li><code>milper</code>: تعداد پرسنل فعال نظامی به هزار نفر.</li>
          <li><code>irst</code>: میزان تولید آهن و فولاد کشور به هزار تن (سنجش توان صنعتی برای پشتیبانی از جنگ).</li>
          <li><code>CINC</code>: میانگین سهم کشور از ۶ متغیر مادی در کل جهان (شاخص نهایی قدرت مادی، بین ۰ تا ۱).</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای سنجش احتمال پیروزی یا توازن قوا در یک دوره تاریخی خاص، متغیر <code>CINC</code> کشورهای رقیب را مقایسه کنید.</span></div>
      <div class="db-link">🔗 <a href="https://www.correlatesofwar.org/" target="_blank">Correlates of War</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۱</span> پایگاه داده مالیه دولت‌های اروپایی (ESFDB)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">مرجعی برای ارزیابی آمارهای مالیاتی، مخارج جنگی، ساختار بدهی‌های ملی و درآمدهای دولتی کشورهای اروپایی از قرن ۱۲ تا ۱۹ میلادی.</span></div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">داده‌های خام معمولاً بر اساس پول‌های ملی قدیمی (مانند «لیور» فرانسه یا «شیلینگ» انگلیس) هستند. برای کار با این داده‌ها، باید آن‌ها را ابتدا به وزن نقره تبدیل کرده و سپس بر جمعیت آن کشور در آن سال تقسیم کنید تا «بار مالیاتی سرانه» به دست آید.</span></div>
      <div class="db-link">🔗 <a href="https://www.esfdb.org/" target="_blank">European State Finance Database</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۲</span> کاتالوگ درگیری‌های پیتر برک (Peter Brecke's Conflict Catalog)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">کاتالوگی شامل اطلاعات بیش از ۳۷۰۰ درگیری نظامی، جنگ داخلی و شورش در سراسر جهان از سال ۱۴۰۰ میلادی به بعد.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">معیار برک برای ثبت یک درگیری، داشتن حداقل ۳۲ کشته در سال (طبق شاخص بزرگی ۱.۵ ریچاردسون) است. وی دوران پیش از قرن ۱۹ را نیز پوشش داده است.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>Conflict Name</code>: نام درگیری یا شورش.</li>
          <li><code>Start Year</code> / <code>End Year</code>: سال شروع و پایان جنگ.</li>
          <li><code>Fatalities (military)</code>: تخمین کشته‌های نظامی.</li>
          <li><code>Fatalities (civilian)</code>: تخمین تلفات غیرنظامی.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">این دیتابیس برای سنجش فراوانی و چگالی جنگ‌ها در مناطق مختلف جهان در سده‌های گذشته به کار می‌رود.</span></div>
      <div class="db-link">🔗 <a href="https://brecke.inta.gatech.edu/wp-content/uploads/sites/19/2018/09/Conflict-Catalog-18-vars.xlsx" target="_blank">Conflict Catalog — دانلود مستقیم فایل اکسل</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ بخش ۴ ═══ -->
  <div class="section">
    <h2>🌐 دیتابیس‌های تجارت بین‌الملل و پیچیدگی اقتصادی</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۳</span> اطلس پیچیدگی اقتصادی هاروارد (Atlas of Economic Complexity — AEC)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">پلتفرمی از مدرسه حکومت کندی دانشگاه هاروارد که جریان تجاری بیش از ۵۰ سال گذشته (از ۱۹۶۲) را برای بیش از ۲۵۰ کشور و ۵۰۰۰ محصول به تصویر می‌کشد. این پلتفرم نظریه «پیچیدگی اقتصادی» سزار هیدالگو و ریکاردو هاوسمن را به صورت عملی پیاده می‌کند.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">شاخص ECI بر اساس تنوع و ندرت سبد صادراتی یک کشور محاسبه می‌شود. داده‌های ثابت با استفاده از شاخص قیمت تولیدکننده (PPI) فدرال رزرو تعدیل می‌شوند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>ECI</code>: شاخص پیچیدگی اقتصادی کشور (Economic Complexity Index).</li>
          <li><code>PCI</code>: شاخص پیچیدگی محصول (Product Complexity Index).</li>
          <li><code>RCA</code>: مزیت نسبی آشکارشده (Revealed Comparative Advantage) برای هر محصول.</li>
          <li><code>export_val</code> / <code>import_val</code>: ارزش صادرات و واردات به تفکیک محصول و شریک تجاری.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای تحلیل ظرفیت‌های نهفته صنعتی و پیش‌بینی مسیر رشد اقتصادی کشورها در میان‌مدت. داده‌ها از طریق API قابل دسترسی هستند.</span></div>
      <div class="db-link">🔗 <a href="https://atlas.hks.harvard.edu/" target="_blank">Atlas of Economic Complexity</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۴</span> پایگاه داده تجارت و تولید CEPII (شامل BACI)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">مرکز تحقیقاتی بین‌المللی اقتصاد و اطلاعات فرانسه (CEPII) چندین پایگاه داده تجاری کلیدی را نگهداری می‌کند، از جمله BACI (داده‌های تجارت دوجانبه در سطح محصول بر اساس HS) و GeoDist (فاصله جغرافیایی و مشخصات ثقل بین کشورها).</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">BACI داده‌های UN Comtrade را با روش آشتی‌سازی (Reconciliation) بین ارقام صادرات گزارش‌شده توسط صادرکننده و واردات گزارش‌شده توسط واردکننده پالایش می‌کند تا مغایرت‌ها را کاهش دهد.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی (BACI):</span>
        <ul class="var-list">
          <li><code>t</code>: سال.</li>
          <li><code>i</code> / <code>j</code>: کد کشور صادرکننده / واردکننده.</li>
          <li><code>k</code>: کد محصول (HS شش رقمی).</li>
          <li><code>v</code>: ارزش تجارت به هزار دلار.</li>
          <li><code>q</code>: حجم تجارت به تن.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای تحلیل‌های اقتصادسنجی مدل جاذبه (Gravity Model) در تجارت بین‌الملل و بررسی اثر پیمان‌های تجاری تاریخی.</span></div>
      <div class="db-link">🔗 <a href="http://www.cepii.fr/CEPII/en/bdd_modele/bdd_modele.asp" target="_blank">CEPII Databases</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ بخش ۵ ═══ -->
  <div class="section">
    <h2>🏺 دیتابیس‌های پیچیدگی اجتماعی و تاریخ عمیق بشر</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۵</span> بانک داده تاریخ جهانی سِشات (Seshat: Global History Databank)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">جامع‌ترین دیتابیس کمّی در مقیاس ماقبل‌التاریخ و تاریخی که ۱۰٬۰۰۰ سال از تاریخ بشری را با بیش از ۱۵۰۰ متغیر برای بیش از ۳۷۰ سیاست (Polity) در ۳۵ منطقه جغرافیایی مختلف جهان پوشش می‌دهد. این پروژه توسط پیتر ترچین و همکاران بین‌المللی‌اش اجرا می‌شود.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">هر رکورد در سِشات نه تنها مقدار متغیر، بلکه درجه عدم قطعیت، اختلاف نظر کارشناسان، توضیحات روایی و مراجع کتابشناختی را نیز ثبت می‌کند. داده‌ها در گام‌های زمانی ۱۰۰ ساله ارزیابی می‌شوند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li>پیچیدگی اجتماعی (Social Complexity): جمعیت، وسعت قلمرو، جمعیت بزرگ‌ترین شهر، سلسله‌مراتب اداری.</li>
          <li>جنگ و فناوری نظامی (Warfare): نوع سلاح، استحکامات دفاعی، اندازه سپاه.</li>
          <li>دین و آیین‌ها (Religion &amp; Ritual): ماهیت خدایان اخلاقی، مناسک جمعی.</li>
          <li>کشاورزی و زیرساخت‌ها (Agriculture): نوع محصول، سیستم آبیاری.</li>
          <li>نهادها (Institutions): نظام مالیاتی، دیوان‌سالاری، سیستم قضایی.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای آزمون «پرسش‌های بزرگ» (Big Questions) مانند رابطه بین دین، جنگ و ظهور جوامع پیچیده. نسخه Equinox-2020 برای دانلود عمومی موجود است.</span></div>
      <div class="db-link">🔗 <a href="http://seshatdatabank.info/" target="_blank">Seshat Global History Databank</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۶</span> کلیوپاتریا — دیتابیس جغرافیایی موجودیت‌های سیاسی جهان (Cliopatria)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">یک پایگاه داده متن‌باز جغرافیایی (Geospatial) که موقعیت، حدود و طول دوره بیش از ۱۶۰۰ موجودیت سیاسی (دولت، امپراتوری، پادشاهی) را از سال ۳۴۰۰ پیش از میلاد تا ۲۰۲۴ میلادی ثبت کرده است. این پروژه در فوریه ۲۰۲۵ در مجله Nature Scientific Data منتشر شده است.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">داده‌ها در قالب فایل‌های GIS قابل استفاده در نرم‌افزارهایی مانند QGIS و ArcGIS هستند و با کدهای شناسایی یکتای سیاست‌ها قابل ادغام با سایر دیتابیس‌های تاریخی (مانند سِشات) هستند.</span></div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li>شناسه موجودیت سیاسی، نام، نوع (امپراتوری / دولت-شهر / ...)، سال شروع و پایان، مختصات مرزی.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای ایجاد نقشه‌های تاریخی پویا (Dynamic Historical Maps) و تحلیل مکانی-زمانی (Spatiotemporal Analysis) گسترش و فروپاشی قدرت‌های سیاسی.</span></div>
      <div class="db-link">🔗 <a href="https://github.com/jsbennett/Cliopatria" target="_blank">Cliopatria on GitHub</a> &nbsp;|&nbsp; <a href="https://doi.org/10.1038/s41597-025-04516-9" target="_blank">مقاله Nature Scientific Data</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ بخش ۶ ═══ -->
  <div class="section">
    <h2>🗂️ پورتال‌های تجمیع داده و توسعه انسانی</h2>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۷</span> کلایو اینفرا (Clio Infra)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">پروژه‌ای جهانی برای گردآوری داده‌های مربوط به شاخص‌های توسعه انسانی (قد، وزن، باسوادی)، نابرابری جنسیتی، سیستم‌های کار و نهادهای مالی در طول تاریخ.</span></div>
      <div class="db-row"><span class="db-label">منطق آماری:</span><span class="db-content">این پلتفرم از روش «همسان‌سازی استاندارد» (Harmonization) استفاده می‌کند؛ یعنی کدهای شناسایی کشورها و سال‌ها در تمام زیرمجموعه‌ها یکسان‌سازی شده تا کاربر بتواند به راحتی داده‌های توزیع درآمد، قد انسان‌ها و میزان تحصیلات را با هم تلفیق (Merge) کند.</span></div>
      <div class="db-link">🔗 <a href="https://clio-infra.eu/" target="_blank">Clio Infra Portal</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۸</span> جهان ما در قالب داده (Our World in Data — OWID)</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">پلتفرمی متعلق به دانشگاه آکسفورد که داده‌های پراکنده و خام سازمان‌های بین‌المللی و دیتابیس‌های تاریخی را گرفته و آن‌ها را به صورت متغیرهای زمانی همگن و مصورسازی‌شده ارائه می‌دهد.</span></div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">بخش اختصاصی <a href="https://ourworldindata.org/state-capacity" target="_blank">State Capacity</a> در این وب‌سایت، دسترسی به فایل‌های تجمیع‌شده درباره مالیات‌ستانی و بروکراسی دولتی در طول تاریخ را برای پژوهش‌های کلان تسهیل می‌کند.</span></div>
      <div class="db-link">🔗 <a href="https://ourworldindata.org/" target="_blank">Our World in Data</a></div>
    </div>

    <div class="db-card">
      <div class="db-title"><span class="db-num">۱۹</span> IPUMS — سری‌های داده میکرو یکپارچه برای استفاده عمومی</div>
      <div class="db-row"><span class="db-label">توضیحات:</span><span class="db-content">بزرگ‌ترین پایگاه داده جمعیتی در سطح فرد در جهان، که توسط دانشگاه مینه‌سوتا نگهداری می‌شود. IPUMS داده‌های سرشماری و پیمایشی از ۱۰۴ کشور (بیش از ۶۵۶ سرشماری و پیمایش) را در قالبی یکپارچه ارائه می‌کند و بیش از یک میلیارد رکورد فردی را در خود جای داده است.</span></div>
      <div class="db-row"><span class="db-label">زیرمجموعه‌های اصلی:</span>
        <ul class="var-list">
          <li><strong>IPUMS USA:</strong> داده‌های سرشماری آمریکا از ۱۷۹۰ تا کنون.</li>
          <li><strong>IPUMS International:</strong> سرشماری‌های بین‌المللی از ۱۹۶۰ به بعد.</li>
          <li><strong>IPUMS NHGIS:</strong> داده‌های جغرافیایی-تاریخی آمریکا با فایل‌های GIS از ۱۷۹۰ به بعد.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">متغیرهای کلیدی:</span>
        <ul class="var-list">
          <li><code>AGE</code>, <code>SEX</code>, <code>RACE</code>: ویژگی‌های جمعیت‌شناختی.</li>
          <li><code>OCC</code> / <code>IND</code>: شغل و صنعت هر فرد (قابل مقایسه در طول زمان).</li>
          <li><code>INCTOT</code>: درآمد کل فرد.</li>
          <li><code>EDUC</code>: سطح تحصیلات.</li>
        </ul>
      </div>
      <div class="db-row"><span class="db-label">نحوه استفاده:</span><span class="db-content">برای مطالعات نقل و انتقال بین‌نسلی، تحلیل بازار کار تاریخی، و بررسی تغییرات جمعیت‌شناختی بلندمدت.</span></div>
      <div class="db-link">🔗 <a href="https://www.ipums.org/" target="_blank">IPUMS</a></div>
    </div>
  </div>

  <hr>

  <!-- ═══ مشارکت ═══ -->
  <div class="contribution">
    <h2>🤝 راهنمای مشارکت (Contribution)</h2>
    <p style="color:#8b949e; font-size:14px; margin-bottom:16px;">اگر دیتابیس تاریخی، مالی یا سیاسی دیگری می‌شناسید که در این فهرست نیست و ساختار علمی و روش‌شناسی مشخصی دارد، خوشحال می‌شویم آن را به این مخزن اضافه کنید:</p>
    <ol class="contrib-list">
      <li>این مخزن را <strong>Fork</strong> کنید.</li>
      <li>دیتابیس مورد نظر خود را همراه با توضیحات، متغیرهای کلیدی، روش‌شناسی و لینک معتبر به انتهای این فایل اضافه کنید.</li>
      <li>یک <strong>Pull Request</strong> ارسال کنید تا تغییرات پس از بررسی ادغام شوند.</li>
    </ol>
  </div>

</div>
</body>
</html>
