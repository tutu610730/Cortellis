from pathlib import Path
import re

path = Path("/mnt/data/index.html")
html = path.read_text(encoding="utf-8")

official_url = "https://clarivate.com/drugs-to-watch/"

# 1) Replace/upgrade hero action buttons
html = html.replace(
'''<div class="actions"><a class="btn btnPrimary" href="#drugs">Explore drugs</a><button class="btn btnSecondary" data-open-contact>預約專家諮詢</button></div>''',
f'''<div class="actions">
          <a class="btn btnPrimary" href="{official_url}" target="_blank" rel="noopener">官方 Drugs to Watch ↗</a>
          <a class="btn btnSecondary" href="#drugs">Explore drugs</a>
          <button class="btn btnSecondary" data-open-contact>預約專家諮詢</button>
        </div>'''
)

# If exact action block differs, insert after subtitle fallback
if official_url not in html.split("</section>",1)[0]:
    html = html.replace(
        '<div class="actions">',
        f'<div class="actions"><a class="btn btnPrimary" href="{official_url}" target="_blank" rel="noopener">官方 Drugs to Watch ↗</a>',
        1
    )

# 2) Add CSS for official resource block if not present
css_insert = """
    .officialBox{margin-top:22px;border:1px solid #bfe9ef;background:linear-gradient(135deg,#eefcfc,#f7fbff);border-radius:22px;padding:24px;display:flex;justify-content:space-between;gap:22px;align-items:center}
    .officialBox h3{margin:0 0 8px;color:var(--navy);font-size:22px}
    .officialBox p{margin:0;color:var(--muted);font-size:14px}
    .rel a{display:inline-flex;margin-top:12px;color:#028f8a;font-weight:800;font-size:13px}
    @media(max-width:680px){.officialBox{display:block}.officialBox .btn{margin-top:16px}}
"""
if ".officialBox" not in html:
    html = html.replace("    @media(max-width:1000px)", css_insert + "\n    @media(max-width:1000px)")

# 3) Upgrade Related Resources with official links
old_resources = '''<section class="section reveal" id="resources">
        <h2>Related Resources</h2>
        <div class="relGrid">
          <div class="rel"><b>2026 Oncology Outlook</b><p>癌症治療策略與標靶蛋白降解市場洞察。</p></div>
          <div class="rel"><b>Future of Obesity Therapeutics</b><p>GLP-1、GIP、Glucagon 與口服療法競爭格局。</p></div>
          <div class="rel"><b>Targeted Protein Degradation Landscape</b><p>新一代 E3 ligase modulator 與 degrader 平台分析。</p></div>
          <div class="rel"><b>Rare Disease Innovation Report</b><p>罕見疾病管線、法規誘因與商業化策略。</p></div>
        </div>
      </section>'''
new_resources = f'''<section class="section reveal" id="resources">
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
      </section>'''
if old_resources in html:
    html = html.replace(old_resources, new_resources)
elif "Official Clarivate Drugs to Watch 2026" not in html:
    html = html.replace('<section class="section reveal" id="contact">', new_resources + '\n\n      <section class="section reveal" id="contact">')

# 4) Add official URL to footer
html = html.replace(
    '© Clarivate-style localized page concept｜Prepared for Traditional Chinese web presentation｜VtR internal web asset',
    f'© Clarivate-style localized page concept｜Prepared for Traditional Chinese web presentation｜<a href="{official_url}" target="_blank" rel="noopener" style="color:#b7e03a;font-weight:800">Official Drugs to Watch</a>｜VtR internal web asset'
)

# 5) Ensure CTA has official page option
html = html.replace(
'''<button class="btn btnPrimary" data-open-contact>填寫需求</button>''',
f'''<div style="display:flex;gap:12px;flex-wrap:wrap">
            <button class="btn btnPrimary" data-open-contact>填寫需求</button>
            <a class="btn btnSecondary" href="{official_url}" target="_blank" rel="noopener">官方頁面 ↗</a>
          </div>''',
1
)

# 6) Save as upgraded formal full site
out = Path("/mnt/data/Clarivate_Drugs_to_Watch_2026_Taiwan_v2_full_index.html")
out.write_text(html, encoding="utf-8")

print(str(out))
print(f"File size: {out.stat().st_size:,} bytes")

