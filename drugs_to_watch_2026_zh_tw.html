from pathlib import Path
from html import escape

official_url = "https://clarivate.com/drugs-to-watch/"

drugs = [
    ("BGB-16673", "Chronic lymphocytic leukemia (CLL) / small lymphocytic lymphoma (SLL)", "BeiGene", "Oncology", "新一代 BTK degrader，聚焦 BTK 抑制劑治療後的抗藥性與復發需求。"),
    ("Cenrifki (tolebrutinib)", "Multiple sclerosis", "Sanofi", "Neurology", "口服 BTK 抑制劑，關注多發性硬化症中樞神經發炎與疾病進展。"),
    ("Exdensur (depemokimab)", "Asthma", "GSK", "Immunology / Respiratory", "超長效 IL-5 抑制劑，目標降低重度氣喘患者給藥頻率並改善長期控制。"),
    ("Gedatolisib", "Breast cancer", "Celcuity", "Oncology", "PI3K / mTOR 路徑抑制策略，針對特定乳癌族群提供新治療選擇。"),
    ("ICOTYDE™ (icotrokinra)", "Plaque psoriasis", "Johnson & Johnson", "Immunology", "口服 IL-23 receptor pathway 相關療法，代表免疫皮膚疾病治療便利性的提升。"),
    ("INLEXZO™ (TAR-200)", "Bladder cancer", "Johnson & Johnson", "Oncology", "膀胱內局部持續釋放治療平台，改善膀胱癌局部治療策略。"),
    ("Lifyorli™ (relacorilant)", "Ovarian cancer", "Corcept Therapeutics", "Oncology / Women’s health", "Glucocorticoid receptor modulation 機制，應用於婦癌與難治性腫瘤治療。"),
    ("Mezigdomide", "Multiple myeloma", "Bristol Myers Squibb", "Oncology", "新一代 cereblon E3 ligase modulator，延伸多發性骨髓瘤治療策略。"),
    ("Orforglipron (Foundayo™)", "Obesity / Type 2 diabetes mellitus", "Eli Lilly", "Metabolic disease", "口服 GLP-1 receptor agonist，若成功商業化將改變減重與糖尿病治療可近性。"),
    ("Retatrutide", "Obesity / Type 2 diabetes mellitus", "Eli Lilly", "Metabolic disease", "GLP-1 / GIP / glucagon 三重受體作用機制，代表下一世代體重管理治療方向。"),
    ("VOYXACT® (sibeprenlimab)", "IgA nephropathy", "Otsuka / Visterra", "Rare disease / Nephrology", "APRIL pathway 相關抗體療法，聚焦 IgA 腎病變疾病修飾治療。"),
]

cards = "\n".join([
f'''          <article class="drug-card reveal" data-company="{escape(company)}" data-area="{escape(area)}" data-name="{escape(name.lower())}">
            <span class="tag">Drugs to Watch 2026</span>
            <h3>{escape(name)}</h3>
            <p class="indication">{escape(indication)}</p>
            <div class="meta-row"><span>{escape(company)}</span><span>{escape(area)}</span></div>
            <p class="why">{escape(why)}</p>
            <button class="text-btn" data-open-drug="{i}">查看重點 ↗</button>
          </article>'''
for i,(name, indication, company, area, why) in enumerate(drugs)
])

modal_data = ",\n".join([
    "{name:%r, indication:%r, company:%r, area:%r, why:%r}" % (name, indication, company, area, why)
    for name, indication, company, area, why in drugs
])

html = f"""<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Clarivate｜Drugs to Watch 2026｜繁體中文版</title>
  <meta name="description" content="Clarivate Drugs to Watch 2026 繁體中文網站，整合 11 項值得期待的創新療法、方法論、產業趨勢與官方連結。" />
  <style>
    :root{{
      --navy:#06162f;--navy2:#082753;--blue:#123c69;--cyan:#00a6c8;--teal:#18b7a0;--lime:#b7e03a;
      --ink:#13233a;--muted:#607086;--line:#dce5ef;--bg:#f5f8fb;--white:#fff;
      --shadow:0 18px 45px rgba(7,27,58,.12);--radius:24px;--max:1180px;
    }}
    *{{box-sizing:border-box}} html{{scroll-behavior:smooth}} body{{margin:0;font-family:"Microsoft JhengHei Light","Microsoft JhengHei","PingFang TC","Noto Sans TC",Arial,sans-serif;color:var(--ink);background:var(--bg);line-height:1.75;font-weight:300}}
    a{{color:inherit;text-decoration:none}} button,input,select,textarea{{font-family:inherit}} .page{{overflow:hidden;background:linear-gradient(180deg,#fff 0%,#f5f8fb 45%,#fff 100%)}}
    .progress{{position:fixed;top:0;left:0;width:0;height:4px;background:linear-gradient(90deg,var(--cyan),var(--lime));z-index:1000;box-shadow:0 0 18px rgba(0,166,200,.55)}}
    .topbar{{position:sticky;top:0;z-index:50;background:rgba(255,255,255,.94);backdrop-filter:blur(14px);border-bottom:1px solid var(--line)}}
    .nav{{max-width:var(--max);margin:auto;padding:16px 24px;display:flex;align-items:center;justify-content:space-between;gap:22px}}
    .brand{{font-size:24px;font-weight:800;color:var(--navy);letter-spacing:-.02em}} .brand span{{color:var(--cyan)}} .navlinks{{display:flex;gap:20px;font-size:14px;color:var(--muted)}} .navlinks a:hover{{color:var(--cyan)}}
    .hero{{position:relative;color:#fff;background:radial-gradient(circle at 78% 20%,rgba(0,166,200,.32),transparent 30%),linear-gradient(135deg,#06162f 0%,#0d315d 56%,#08213f 100%)}}
    .hero:after{{content:"";position:absolute;right:-120px;bottom:-120px;width:360px;height:360px;border-radius:50%;background:rgba(183,224,58,.16)}}
    .hero-inner{{max-width:var(--max);margin:auto;padding:84px 24px 78px;position:relative;z-index:2;display:grid;grid-template-columns:1.25fr .75fr;gap:46px;align-items:center}}
    .eyebrow{{display:inline-flex;gap:10px;align-items:center;border:1px solid rgba(255,255,255,.28);border-radius:999px;padding:7px 14px;font-size:13px;color:#d7eef7;background:rgba(255,255,255,.08)}} .eyebrow:before{{content:"";width:8px;height:8px;border-radius:50%;background:var(--lime)}}
    h1{{font-size:clamp(42px,6vw,72px);line-height:1.02;margin:22px 0 18px;letter-spacing:-.055em;font-weight:800}} .subtitle{{font-size:19px;max-width:780px;color:#d9e8f5;margin:0 0 28px}}
    .actions{{display:flex;gap:13px;flex-wrap:wrap}} .btn{{display:inline-flex;align-items:center;justify-content:center;gap:8px;border-radius:999px;padding:12px 20px;font-weight:800;font-size:15px;transition:.25s;border:1px solid transparent;cursor:pointer}} .btnPrimary{{background:var(--lime);color:#071b3a}} .btnPrimary:hover{{transform:translateY(-2px);box-shadow:0 12px 30px rgba(183,224,58,.25)}} .btnSecondary{{border-color:rgba(255,255,255,.35);color:#fff;background:rgba(255,255,255,.06)}} .btnSecondary:hover{{background:rgba(255,255,255,.14)}}
    .hero-card{{background:rgba(255,255,255,.10);border:1px solid rgba(255,255,255,.22);border-radius:28px;padding:28px;box-shadow:0 24px 80px rgba(0,0,0,.18);backdrop-filter:blur(10px)}} .metric{{display:grid;grid-template-columns:88px 1fr;gap:14px;align-items:center;border-bottom:1px solid rgba(255,255,255,.16);padding:17px 0}} .metric:last-child{{border-bottom:0}} .metric strong{{font-size:38px;color:var(--lime);line-height:1}} .metric span{{color:#e6f2fa;font-size:15px}}
    .layout{{max-width:var(--max);margin:-30px auto 0;padding:0 24px;display:grid;grid-template-columns:250px 1fr;gap:30px;position:relative;z-index:4}} .side{{position:sticky;top:86px;align-self:start;background:#fff;border:1px solid var(--line);border-radius:var(--radius);padding:20px;box-shadow:var(--shadow)}} .side h3{{margin:0 0 10px;font-size:13px;color:var(--navy);letter-spacing:.08em;text-transform:uppercase}} .toc{{list-style:none;margin:0;padding:0}} .toc li{{border-top:1px solid #edf2f7}} .toc a{{display:block;padding:9px 0;color:#53677d;font-size:13px}} .toc a:hover,.toc a.active{{color:#028f8a;font-weight:800}}
    main{{min-width:0}} .section{{background:#fff;border:1px solid var(--line);border-radius:var(--radius);box-shadow:var(--shadow);padding:36px 40px;margin-bottom:28px}} .section h2{{font-size:34px;line-height:1.18;margin:0 0 12px;color:var(--navy);letter-spacing:-.035em}} .lead{{max-width:790px;color:var(--muted);font-size:16px;margin:0 0 22px}}
    .filterbar{{display:grid;grid-template-columns:1fr 1fr 1.3fr;gap:12px;background:#f8fbfd;border:1px solid var(--line);border-radius:20px;padding:14px;margin:22px 0}} select,input,textarea{{width:100%;border:1px solid var(--line);border-radius:999px;padding:12px 15px;font-size:14px;color:var(--ink);background:#fff;outline:none}} select:focus,input:focus,textarea:focus{{border-color:var(--cyan);box-shadow:0 0 0 4px rgba(0,166,200,.12)}}
    .grid{{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}} .drug-card{{position:relative;min-height:270px;background:#fff;border:1px solid var(--line);border-radius:22px;padding:22px;box-shadow:0 10px 28px rgba(7,27,58,.06);transition:.25s;overflow:hidden}} .drug-card:before{{content:"";position:absolute;left:0;top:0;width:100%;height:5px;background:linear-gradient(90deg,var(--cyan),var(--lime))}} .drug-card:hover{{transform:translateY(-5px);box-shadow:var(--shadow)}} .tag{{display:inline-flex;border-radius:999px;background:#eef7fb;color:var(--blue);font-size:12px;font-weight:800;padding:5px 10px;margin-bottom:15px}} .drug-card h3{{font-size:22px;line-height:1.22;color:var(--navy);margin:0 0 8px;letter-spacing:-.02em}} .drug-card p{{margin:0 0 12px;color:var(--muted);font-size:14px}} .indication{{font-weight:700;color:#2b4b6c!important}} .why{{font-size:13px!important}} .meta-row{{display:flex;gap:8px;flex-wrap:wrap;margin:12px 0}} .meta-row span{{font-size:11px;background:#f3f8fb;border:1px solid #e2edf3;border-radius:999px;padding:4px 8px;color:#53677d;font-weight:700}} .text-btn{{border:0;background:transparent;color:#028f8a;font-weight:800;cursor:pointer;padding:0;font-size:14px}}
    .trend-grid,.method-grid,.relGrid{{display:grid;grid-template-columns:repeat(4,1fr);gap:16px}} .trend,.method-card,.rel{{background:linear-gradient(180deg,#fff,#f7fbfd);border:1px solid var(--line);border-radius:20px;padding:20px;min-height:160px}} .trend b,.method-card b,.rel b{{display:block;font-size:17px;color:var(--navy);margin-bottom:8px}} .trend p,.method-card p,.rel p{{font-size:13px;color:var(--muted);margin:0}} .icon{{width:40px;height:40px;border-radius:14px;background:linear-gradient(135deg,var(--cyan),var(--teal));margin-bottom:16px}}
    .officialBox{{margin-top:20px;border:1px solid #bfe9ef;background:linear-gradient(135deg,#eefcfc,#f7fbff);border-radius:22px;padding:24px;display:flex;justify-content:space-between;gap:22px;align-items:center}} .officialBox h3{{margin:0 0 8px;color:var(--navy);font-size:22px}} .officialBox p{{margin:0;color:var(--muted);font-size:14px}} .officialBox .btnSecondary{{color:var(--navy);border-color:#bfe9ef;background:#fff}} .rel a{{display:inline-flex;margin-top:12px;color:#028f8a;font-weight:800;font-size:13px}}
    .cta{{background:linear-gradient(135deg,var(--navy),#075766);color:#fff;border-radius:24px;padding:28px;display:flex;justify-content:space-between;gap:22px;align-items:center}} .cta h2{{color:#fff;margin:0 0 8px;font-size:26px}} .cta p{{color:#d5ffff;margin:0}} .cta .btnSecondary{{color:#fff}}
    footer{{background:#06162f;color:#c9d8e6;padding:32px 24px;text-align:center;font-size:13px}} footer a{{color:var(--lime);font-weight:800}}
    .reveal{{opacity:0;transform:translateY(18px);transition:opacity .7s ease,transform .7s ease}} .reveal.show{{opacity:1;transform:none}}
    .modal{{position:fixed;inset:0;background:rgba(3,12,28,.65);display:none;place-items:center;padding:22px;z-index:999}} .modal.show{{display:grid}} .modalCard{{width:min(720px,100%);max-height:92vh;overflow:auto;background:white;border-radius:24px;box-shadow:0 28px 80px rgba(0,0,0,.35)}} .modalHead{{padding:23px 26px;background:linear-gradient(135deg,var(--navy),#075766);color:white;display:flex;justify-content:space-between;gap:18px}} .modalHead h2{{margin:0 0 5px;color:#fff}} .modalHead p{{margin:0;color:#d7fffd;font-size:13px}} .close{{background:rgba(255,255,255,.13);border:1px solid rgba(255,255,255,.25);color:white;border-radius:50%;width:38px;height:38px;cursor:pointer;font-size:22px}} .form{{padding:24px 26px}} .formGrid{{display:grid;grid-template-columns:repeat(2,1fr);gap:14px}} .field label{{display:block;font-size:13px;color:#34465a;font-weight:800;margin-bottom:6px}} .field textarea{{border-radius:16px;min-height:105px;resize:vertical}} .full{{grid-column:1/-1}} .status{{font-size:13px;color:#53677d;margin:12px 0 0}}
    @media(max-width:1000px){{.hero-inner,.layout{{grid-template-columns:1fr}} .side{{position:relative;top:0}} .grid{{grid-template-columns:repeat(2,1fr)}} .trend-grid,.method-grid,.relGrid{{grid-template-columns:repeat(2,1fr)}} .navlinks{{display:none}}}}
    @media(max-width:680px){{.nav,.hero-inner,.layout{{padding-left:18px;padding-right:18px}} .section{{padding:28px 22px}} .grid,.trend-grid,.method-grid,.relGrid,.filterbar,.formGrid{{grid-template-columns:1fr}} .officialBox,.cta{{display:block}} .officialBox .btn,.cta .btn{{margin-top:16px}} h1{{font-size:38px}} .section h2{{font-size:29px}}}}
  </style>
</head>
<body>
<div class="page" id="top">
  <div class="progress" id="progress"></div>
  <header class="topbar">
    <nav class="nav">
      <a class="brand" href="#top">Clarivate<span>™</span></a>
      <div class="navlinks">
        <a href="#overview">Overview</a><a href="#method">Methodology</a><a href="#drugs">Drugs</a><a href="#trends">Trends</a><a href="#resources">Resources</a><a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <section class="hero">
    <div class="hero-inner">
      <div>
        <div class="eyebrow">Drugs to Watch 2026</div>
        <h1>11 項值得期待的創新療法</h1>
        <p class="subtitle">Clarivate 分析師系統性選出 11 項具潛力的治療藥物，預期在未來五年改變治療典範，或成為重磅級藥物。</p>
        <div class="actions">
          <a class="btn btnPrimary" href="{official_url}" target="_blank" rel="noopener">官方 Drugs to Watch ↗</a>
          <a class="btn btnSecondary" href="#drugs">Explore drugs</a>
          <button class="btn btnSecondary" data-open-contact>預約專家諮詢</button>
        </div>
      </div>
      <aside class="hero-card">
        <div class="metric"><strong>11</strong><span>具變革潛力的候選／新興治療藥物</span></div>
        <div class="metric"><strong>160+</strong><span>Clarivate 分析師參與評估</span></div>
        <div class="metric"><strong>10</strong><span>整合式、AI-enhanced 資料集</span></div>
      </aside>
    </div>
  </section>

  <div class="layout">
    <aside class="side reveal">
      <h3>本文目錄</h3>
      <ul class="toc">
        <li><a href="#overview">Drugs to Watch 概述</a></li>
        <li><a href="#method">評選方法論</a></li>
        <li><a href="#drugs">11 項重點藥物</a></li>
        <li><a href="#trends">產業趨勢觀察</a></li>
        <li><a href="#resources">Related Resources</a></li>
        <li><a href="#contact">Contact Us</a></li>
      </ul>
    </aside>

    <main>
      <section class="section reveal" id="overview">
        <h2>Drugs to Watch 2026 概述</h2>
        <p class="lead">本頁為 Clarivate Drugs to Watch 2026 的繁體中文展示版，適合用於台灣市場推廣、客戶簡報、Google Sites 內嵌與 GitHub Pages 部署。</p>
        <div class="trend-grid">
          <div class="trend"><div class="icon"></div><b>Next-generation GLP-1</b><p>口服與多重受體機制持續推動肥胖症與 T2DM 市場。</p></div>
          <div class="trend"><div class="icon"></div><b>Targeted Protein Degradation</b><p>Degrader 與 E3 ligase modulator 改寫腫瘤治療策略。</p></div>
          <div class="trend"><div class="icon"></div><b>Precision Medicine</b><p>罕見疾病、免疫疾病與腎臟疾病加速精準治療設計。</p></div>
          <div class="trend"><div class="icon"></div><b>Women’s Health</b><p>婦癌與女性健康未滿足需求成為創新重點。</p></div>
        </div>
      </section>

      <section class="section reveal" id="method">
        <h2>How We Identified the Drugs to Watch</h2>
        <p class="lead">Clarivate 年度 Drugs to Watch 報告結合分析師專業、全球生命科學資料資產與 AI-enhanced 分析流程，用於辨識具高臨床與商業化影響力的治療產品。</p>
        <div class="method-grid">
          <div class="method-card"><b>01｜Analyst Expertise</b><p>超過 160 位分析師，涵蓋數百種疾病、藥物、市場與競爭格局。</p></div>
          <div class="method-card"><b>02｜Integrated Datasets</b><p>整合 10 組 AI-enhanced 資料集，橫跨研發至商業化生命週期。</p></div>
          <div class="method-card"><b>03｜AI Validation</b><p>以 AI 平台輔助驗證候選藥物結果，並依產業趨勢進行分群。</p></div>
          <div class="method-card"><b>04｜Market Potential</b><p>評估治療典範改變、未滿足需求、商業化潛力與市場採用速度。</p></div>
        </div>
      </section>

      <section class="section reveal" id="drugs">
        <h2>2026 Drugs to Watch</h2>
        <p class="lead">涵蓋 GLP-1 減重與 T2DM、癌症標靶蛋白降解、罕見疾病精準醫療、女性健康與免疫疾病等重點領域。</p>
        <div class="filterbar">
          <select id="companyFilter"><option value="">All companies</option></select>
          <select id="areaFilter"><option value="">All therapy areas</option></select>
          <input id="searchBox" type="search" placeholder="Search by drug, company or indication" />
        </div>
        <div class="grid" id="drugGrid">
{cards}
        </div>
      </section>

      <section class="section reveal" id="trends">
        <h2>Industry Trends Driving Innovation</h2>
        <p class="lead">2026 年入選名單反映四大產業趨勢：肥胖症市場擴張、標靶蛋白降解進入商業化視野、罕見疾病精準醫療加速，以及女性健康重新成為投資重點。</p>
        <div class="trend-grid">
          <div class="trend"><div class="icon"></div><b>Obesity & T2DM</b><p>Orforglipron 與 Retatrutide 代表下一波 GLP-1 與多重受體療法競賽。</p></div>
          <div class="trend"><div class="icon"></div><b>Oncology Strategy</b><p>BGB-16673、Mezigdomide 與 TAR-200 顯示腫瘤治療策略更多元。</p></div>
          <div class="trend"><div class="icon"></div><b>Immunology</b><p>Icotrokinra、Depemokimab 與 Tolebrutinib 反映免疫疾病新機制。</p></div>
          <div class="trend"><div class="icon"></div><b>Rare Disease</b><p>Sibeprenlimab 聚焦 IgA nephropathy，凸顯高負擔罕見疾病創新。</p></div>
        </div>
      </section>

      <section class="section reveal" id="resources">
        <h2>Related Resources</h2>
        <p class="lead">延伸閱讀可串接 Clarivate 官方 Drugs to Watch 專區、完整報告下載入口與相關 webinar / insight 頁面。</p>
        <div class="officialBox">
          <div>
            <h3>Official Clarivate Drugs to Watch 2026</h3>
            <p>查看官方 Drugs to Watch 專區，包含完整藥物清單、評選方法論、分析師觀點、產業趨勢與報告下載入口。</p>
          </div>
          <a class="btn btnPrimary" href="{official_url}" target="_blank" rel="noopener">Visit Official Page ↗</a>
        </div>
        <div class="relGrid" style="margin-top:18px">
          <div class="rel"><b>Drugs to Watch Official Website</b><p>官方專區：11 項藥物、方法論、產業趨勢與 downloadable report。</p><a href="{official_url}" target="_blank" rel="noopener">Open official page ↗</a></div>
          <div class="rel"><b>2026 Oncology Outlook</b><p>癌症治療策略、標靶蛋白降解與新型腫瘤療法市場洞察。</p></div>
          <div class="rel"><b>Future of Obesity Therapeutics</b><p>GLP-1、GIP、Glucagon 與口服療法競爭格局。</p></div>
          <div class="rel"><b>Rare Disease Innovation Report</b><p>罕見疾病管線、法規誘因與商業化策略。</p></div>
        </div>
      </section>

      <section class="section reveal" id="contact">
        <div class="cta">
          <div>
            <h2>Contact Us</h2>
            <p>需要 Clarivate Cortellis、Drug Pipeline Analysis、Competitive Intelligence 或 Drugs to Watch 介紹？請留下需求。</p>
          </div>
          <div class="actions">
            <button class="btn btnPrimary" data-open-contact>填寫需求</button>
            <a class="btn btnSecondary" href="{official_url}" target="_blank" rel="noopener">官方頁面 ↗</a>
          </div>
        </div>
      </section>
    </main>
  </div>

  <footer>
    © Clarivate-style localized page concept｜Prepared for Traditional Chinese web presentation｜
    <a href="{official_url}" target="_blank" rel="noopener">Official Drugs to Watch</a>｜VtR internal web asset
  </footer>

  <div class="modal" id="drugModal" role="dialog" aria-modal="true">
    <div class="modalCard">
      <div class="modalHead"><div><h2 id="drugTitle">Drug</h2><p id="drugSub"></p></div><button class="close" data-close-drug>×</button></div>
      <div class="form">
        <p><b>Company：</b><span id="drugCompany"></span></p>
        <p><b>Therapy area：</b><span id="drugArea"></span></p>
        <p><b>關注原因：</b><span id="drugWhy"></span></p>
        <p><a class="btn btnPrimary" href="{official_url}" target="_blank" rel="noopener">前往 Clarivate 官方頁面 ↗</a></p>
      </div>
    </div>
  </div>

  <div class="modal" id="contactModal" role="dialog" aria-modal="true" aria-label="Contact Us 表單">
    <div class="modalCard">
      <div class="modalHead"><div><h2>Contact Us</h2><p>請留下您的需求，我們將協助提供 Clarivate Cortellis / Drugs to Watch 相關資訊。</p></div><button class="close" data-close-contact>×</button></div>
      <form class="form" id="contactForm">
        <div class="formGrid">
          <div class="field"><label>公司 / 學校 *</label><input name="公司或學校" required placeholder="例：XX Pharma / XX University" /></div>
          <div class="field"><label>單位 / 科系 *</label><input name="單位或科系" required placeholder="例：BD / R&D / IP / Library" /></div>
          <div class="field"><label>姓名 *</label><input name="姓名" required placeholder="請輸入姓名" /></div>
          <div class="field"><label>Email *</label><input name="Email" type="email" required placeholder="name@example.com" /></div>
          <div class="field"><label>電話</label><input name="電話" placeholder="手機或分機" /></div>
          <div class="field"><label>主要需求</label><select name="主要需求"><option>Cortellis</option><option>Drug Pipeline Analysis</option><option>Competitive Intelligence</option><option>Drugs to Watch Report</option><option>Market Landscape</option><option>其他</option></select></div>
          <div class="field full"><label>需求說明</label><textarea name="需求說明" placeholder="請簡述想了解的治療領域、藥物、市場、競品或報告需求。"></textarea></div>
        </div>
        <div class="actions" style="margin-top:18px"><button class="btn btnPrimary" type="submit">送出需求</button><button class="btn btnSecondary" type="button" data-close-contact style="color:var(--navy);border-color:var(--line)">稍後再說</button></div>
        <p class="status" id="formStatus">Google Apps Script endpoint 尚未設定時，系統會以 Email 草稿備援開啟。</p>
      </form>
    </div>
  </div>
</div>

<script>
(function(){{
  const OFFICIAL_URL = "{official_url}";
  const RECIPIENT = "murphychen@vtr.asia";
  const GAS_ENDPOINT = "";
  const DRUGS = [
    {modal_data}
  ];

  const progress = document.getElementById("progress");
  const companyFilter = document.getElementById("companyFilter");
  const areaFilter = document.getElementById("areaFilter");
  const searchBox = document.getElementById("searchBox");
  const cards = Array.from(document.querySelectorAll(".drug-card"));
  const contactModal = document.getElementById("contactModal");
  const drugModal = document.getElementById("drugModal");
  const form = document.getElementById("contactForm");
  const status = document.getElementById("formStatus");

  function updateProgress(){{
    const h = document.documentElement;
    const sc = h.scrollTop || document.body.scrollTop;
    const max = (h.scrollHeight - h.clientHeight) || 1;
    progress.style.width = Math.min(100, Math.max(0, sc / max * 100)) + "%";
  }}
  window.addEventListener("scroll", updateProgress, {{passive:true}});
  updateProgress();

  const io = new IntersectionObserver((entries)=>{{
    entries.forEach(e=>{{ if(e.isIntersecting){{ e.target.classList.add("show"); io.unobserve(e.target); }} }});
  }}, {{threshold:.12}});
  document.querySelectorAll(".reveal").forEach(el=>io.observe(el));

  function uniqueValues(attr){{
    return [...new Set(cards.map(c=>c.getAttribute(attr)).filter(Boolean))].sort();
  }}
  uniqueValues("data-company").forEach(v=>companyFilter.insertAdjacentHTML("beforeend", `<option value="${{v}}">${{v}}</option>`));
  uniqueValues("data-area").forEach(v=>areaFilter.insertAdjacentHTML("beforeend", `<option value="${{v}}">${{v}}</option>`));

  function filterCards(){{
    const c = companyFilter.value;
    const a = areaFilter.value;
    const q = (searchBox.value || "").toLowerCase().trim();
    cards.forEach(card=>{{
      const text = card.textContent.toLowerCase();
      const ok = (!c || card.getAttribute("data-company") === c) &&
                 (!a || card.getAttribute("data-area") === a) &&
                 (!q || text.includes(q));
      card.style.display = ok ? "" : "none";
    }});
  }}
  companyFilter.addEventListener("change", filterCards);
  areaFilter.addEventListener("change", filterCards);
  searchBox.addEventListener("input", filterCards);

  document.querySelectorAll("[data-open-contact]").forEach(btn=>btn.addEventListener("click",()=>contactModal.classList.add("show")));
  document.querySelectorAll("[data-close-contact]").forEach(btn=>btn.addEventListener("click",()=>contactModal.classList.remove("show")));
  contactModal.addEventListener("click",e=>{{ if(e.target === contactModal) contactModal.classList.remove("show"); }});

  document.querySelectorAll("[data-open-drug]").forEach(btn=>btn.addEventListener("click",()=>{{
    const d = DRUGS[Number(btn.dataset.openDrug)];
    document.getElementById("drugTitle").textContent = d.name;
    document.getElementById("drugSub").textContent = d.indication;
    document.getElementById("drugCompany").textContent = d.company;
    document.getElementById("drugArea").textContent = d.area;
    document.getElementById("drugWhy").textContent = d.why;
    drugModal.classList.add("show");
  }}));
  document.querySelectorAll("[data-close-drug]").forEach(btn=>btn.addEventListener("click",()=>drugModal.classList.remove("show")));
  drugModal.addEventListener("click",e=>{{ if(e.target === drugModal) drugModal.classList.remove("show"); }});
  document.addEventListener("keydown",e=>{{ if(e.key === "Escape"){{ contactModal.classList.remove("show"); drugModal.classList.remove("show"); }} }});

  function collectForm(){{
    const fd = new FormData(form);
    const obj = {{}};
    fd.forEach((v,k)=>{{ obj[k] = obj[k] ? obj[k] + ", " + v : v; }});
    obj["送出頁面"] = location.href;
    obj["送出時間"] = new Date().toLocaleString("zh-TW");
    return obj;
  }}
  function mailtoFallback(data){{
    const lines = Object.entries(data).map(([k,v])=>k + "：" + v).join("\\n");
    location.href = "mailto:" + RECIPIENT + "?subject=" + encodeURIComponent("Clarivate Drugs to Watch 諮詢需求 - " + (data["公司或學校"] || "")) + "&body=" + encodeURIComponent(lines);
  }}
  form.addEventListener("submit", async e=>{{
    e.preventDefault();
    const data = collectForm();
    status.textContent = "表單處理中...";
    if(GAS_ENDPOINT && GAS_ENDPOINT.startsWith("https://")){{
      try{{
        await fetch(GAS_ENDPOINT, {{method:"POST", mode:"no-cors", headers:{{"Content-Type":"application/json"}}, body:JSON.stringify(data)}});
        status.textContent = "已送出，謝謝您的填寫。";
        form.reset();
        setTimeout(()=>contactModal.classList.remove("show"), 900);
      }}catch(err){{
        status.textContent = "線上送出未完成，將改用 Email 草稿備援。";
        mailtoFallback(data);
      }}
    }} else {{
      status.textContent = "尚未設定 Google Apps Script endpoint，已開啟 Email 草稿備援。";
      mailtoFallback(data);
    }}
  }});
}})();
</script>
</body>
</html>
"""

# overwrite clean index.html and backup named file
out1 = Path("/mnt/data/index.html")
out2 = Path("/mnt/data/Clarivate_Drugs_to_Watch_2026_clean_index.html")
out1.write_text(html, encoding="utf-8")
out2.write_text(html, encoding="utf-8")

print("Created:")
print(out1)
print(out2)
print("Size:", out1.stat().st_size, "bytes")
print("Contains Python?", "from pathlib" in html or "Path(" in html)
