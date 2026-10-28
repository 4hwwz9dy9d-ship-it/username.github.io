<html lang="zh-CN">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>让教师被技术成全 · 个人数字化反思作品集 · 王俊杰</title>
<link rel="icon" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='7' fill='%23143B35'/%3E%3Cpath d='M8 22V10h2.4v8.2H18V22H8zm6.4-6.4V10h2.4v5.6h-2.4zM20 22V10h7.2v2.3h-4.6v2.3h4v2.2h-4V22H20z' fill='%23F5F6F2'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@600;700;900&family=Noto+Sans+SC:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<script src="https://fastly.jsdelivr.net/npm/echarts@5.5.1/dist/echarts.min.js"></script>
<style>
:root{
  --paper:#F5F6F2;
  --ink:#143B35;
  --ink-2:#2C5A51;
  --txt:#33453F;
  --mut:#6B7C76;
  --jade:#2E7D6B;
  --jade-soft:#E4EFEA;
  --amber:#C8872B;
  --amber-soft:#F5EBD9;
  --card:#FFFFFF;
  --line:rgba(20,59,53,.14);
  --serif:"Noto Serif SC",serif;
  --sans:"Noto Sans SC",system-ui,-apple-system,"PingFang SC","Microsoft YaHei",sans-serif;
  --shadow:0 4px 20px rgba(20,59,53,.06);
  --shadow-hover:0 8px 32px rgba(20,59,53,.12);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:var(--sans);color:var(--txt);background:var(--paper);line-height:1.75;font-size:16px;-webkit-font-smoothing:antialiased}
.wrap{max-width:1120px;margin:0 auto;padding:0 24px}
a{color:var(--jade);text-decoration:none}
a:hover{text-decoration:underline}

/* ===== 顶部进度条 ===== */
.progress-bar{position:fixed;top:0;left:0;height:3px;background:linear-gradient(90deg,var(--amber),var(--jade));z-index:100;width:0%;transition:width .1s linear}

/* ===== 顶栏 ===== */
.nav{position:sticky;top:0;z-index:50;background:rgba(245,246,242,.92);backdrop-filter:blur(10px);border-bottom:1px solid var(--line)}
.nav-in{display:flex;align-items:center;justify-content:space-between;height:60px}
.brand{font-family:var(--serif);font-weight:700;color:var(--ink);font-size:15px;letter-spacing:.02em}
.brand b{color:var(--amber)}
.nav-links{display:flex;gap:2px}
.nav-links a{color:var(--ink-2);font-size:13.5px;padding:7px 12px;border-radius:8px;font-weight:500;transition:all .2s}
.nav-links a:hover,.nav-links a.active{background:var(--jade-soft);text-decoration:none;color:var(--ink)}

/* ===== Hero ===== */
.hero{position:relative;overflow:hidden;background:linear-gradient(150deg,#143B35 0%,#1E5A4E 55%,#2E7D6B 100%);color:#F2F6F3;padding:92px 0 68px}
.hero::after{content:"";position:absolute;inset:0;background:radial-gradient(1200px 420px at 85% -10%,rgba(200,135,43,.28),transparent 60%),radial-gradient(800px 400px at -5% 110%,rgba(200,135,43,.16),transparent 55%);pointer-events:none}
.hero .wrap{position:relative;z-index:2}
.eyebrow{display:inline-flex;align-items:center;gap:8px;font-size:12.5px;letter-spacing:.14em;color:#C9E0D8;text-transform:uppercase;font-weight:600;margin-bottom:22px}
.eyebrow::before{content:"";width:26px;height:2px;background:var(--amber)}
.hero h1{font-family:var(--serif);font-weight:900;font-size:clamp(30px,4.6vw,52px);line-height:1.22;max-width:16em;letter-spacing:.01em}
.hero h1 .hl{color:#F0B45A}
.hero .sub{margin-top:22px;font-size:clamp(15px,1.8vw,18px);color:#D9E7E2;max-width:42em;font-weight:300}
.hero .meta{margin-top:30px;display:flex;flex-wrap:wrap;gap:10px}
.chip{background:rgba(255,255,255,.10);border:1px solid rgba(255,255,255,.22);padding:7px 14px;border-radius:100px;font-size:13px;color:#EAF2EF;backdrop-filter:blur(4px)}
.stats{position:relative;z-index:2;margin-top:42px;display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(255,255,255,.14);border:1px solid rgba(255,255,255,.18);border-radius:16px;overflow:hidden}
.stat{background:rgba(20,59,53,.18);padding:20px 16px;text-align:center;transition:background .3s}
.stat:hover{background:rgba(20,59,53,.28)}
.stat .num{font-family:var(--serif);font-weight:900;font-size:clamp(22px,2.6vw,30px);color:#F0B45A;font-variant-numeric:tabular-nums}
.stat .lbl{font-size:12.5px;color:#C9DED7;margin-top:5px;line-height:1.45}
.hero-note{margin-top:18px;font-size:13px;color:#A9C4BB;letter-spacing:.01em}

/* ===== 章节通用 ===== */
section{padding:76px 0;scroll-margin-top:60px}
.sec-head{display:flex;align-items:baseline;gap:16px;margin-bottom:36px}
.sec-no{font-family:var(--serif);font-weight:900;font-size:44px;color:var(--jade);line-height:1;opacity:.28}
.sec-title{font-family:var(--serif);font-weight:900;font-size:clamp(22px,3vw,30px);color:var(--ink);line-height:1.3}
.sec-title small{display:block;font-family:var(--sans);font-weight:500;font-size:14px;color:var(--mut);margin-top:6px;letter-spacing:.02em}
.sec-title i{font-style:normal;color:var(--amber)}
.card{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:28px 28px;box-shadow:var(--shadow);transition:box-shadow .25s,transform .25s}
.card:hover{box-shadow:var(--shadow-hover)}
.card + .card{margin-top:18px}
.h2{font-family:var(--serif);font-weight:700;font-size:18.5px;color:var(--ink);margin:24px 0 12px}
.h2:first-child{margin-top:0}
.h3{font-weight:600;color:var(--ink-2);font-size:15.5px;margin:14px 0 8px}
p{margin-bottom:12px}
p:last-child{margin-bottom:0}
.mut{color:var(--mut);font-size:14px}
.lead{font-size:16.5px}
strong{color:var(--ink)}
.em{color:var(--amber);font-weight:600}
.quote{border-left:3px solid var(--amber);background:var(--amber-soft);padding:16px 20px;border-radius:0 12px 12px 0;font-family:var(--serif);color:var(--ink);font-size:15.5px;margin:18px 0;line-height:1.8}

/* 三叉卡 */
.trio{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin:22px 0}
.trio .t{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:22px 20px;position:relative;overflow:hidden;transition:transform .25s,box-shadow .25s}
.trio .t:hover{transform:translateY(-3px);box-shadow:var(--shadow-hover)}
.trio .t .tag{display:inline-block;font-size:11.5px;font-weight:700;letter-spacing:.1em;color:var(--jade);margin-bottom:10px;background:var(--jade-soft);padding:3px 10px;border-radius:100px}
.trio .t h4{font-family:var(--serif);font-weight:700;color:var(--ink);font-size:17px;margin-bottom:8px}
.trio .t p{font-size:14px;color:var(--mut);line-height:1.7;margin:0}

/* 两栏 */
.cols{display:grid;grid-template-columns:1fr 1fr;gap:18px}
.cols .card{margin-top:0}

/* 图表 */
.chart{width:100%;height:380px}
.chart-sm{width:100%;height:300px}
.chart-title{font-weight:600;color:var(--ink);font-size:15.5px;margin-bottom:4px}
.chart-cap{font-size:13px;color:var(--mut);margin-bottom:14px}

/* ===== 工作流对比（核心多模态） ===== */
.workflow-compare{margin:24px 0}
.wf-header{display:grid;grid-template-columns:1fr 60px 1fr;gap:0;margin-bottom:12px}
.wf-header .side{text-align:center;font-weight:700;font-size:14.5px;padding:10px;border-radius:10px}
.wf-header .trad{background:#F8EDED;color:#9A4A4A}
.wf-header .ai{background:var(--jade-soft);color:var(--ink)}
.wf-header .mid{display:flex;align-items:center;justify-content:center;color:var(--mut);font-size:12px;font-weight:600}
.wf-row{display:grid;grid-template-columns:1fr 60px 1fr;gap:0;margin-bottom:10px;align-items:stretch}
.wf-node{border:1px solid var(--line);border-radius:12px;padding:12px 14px;font-size:13.5px;line-height:1.55;background:var(--card);position:relative}
.wf-node .step{font-weight:700;font-size:12px;display:block;margin-bottom:3px}
.wf-node.trad-side .step{color:#9A4A4A}
.wf-node.ai-side{border-color:var(--jade);background:linear-gradient(135deg,#F7FBF9 0%,var(--jade-soft) 100%)}
.wf-node.ai-side .step{color:var(--jade)}
.wf-mid{display:flex;align-items:center;justify-content:center;color:var(--amber);font-size:18px;font-weight:700}
.wf-save{display:inline-block;margin-top:6px;background:var(--amber-soft);color:var(--amber);font-weight:700;font-size:12px;padding:2px 9px;border-radius:6px}
.wf-insight{margin-top:18px;padding:16px 20px;background:var(--jade-soft);border-radius:12px;font-size:14.5px;color:var(--ink);line-height:1.75}

/* 机制四阶段增强 */
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:14px;margin:22px 0}
.step-card{position:relative;background:var(--card);border:1px solid var(--line);border-radius:16px;padding:22px 18px;min-height:230px;transition:transform .25s,box-shadow .25s}
.step-card:hover{transform:translateY(-4px);box-shadow:var(--shadow-hover)}
.step-card .no{font-family:var(--serif);font-weight:900;font-size:32px;color:var(--jade);opacity:.85;line-height:1}
.step-card .ph{font-weight:700;color:var(--ink);font-size:16.5px;margin:10px 0 6px}
.step-card .win{font-size:12.5px;font-weight:600;color:var(--amber);margin-bottom:8px;display:inline-block;background:var(--amber-soft);padding:2px 10px;border-radius:100px}
.step-card p{font-size:13.5px;color:var(--mut);line-height:1.7;margin:0}
.step-card .out{margin-top:12px;font-size:12.5px;color:var(--ink-2);font-weight:600;border-top:1px dashed var(--line);padding-top:10px}
.steps-arrow{position:absolute;right:-16px;top:50%;transform:translateY(-50%);color:var(--amber);font-size:22px;z-index:3;font-weight:700}
.step-card:last-child .steps-arrow{display:none}

/* 效果条 */
.eff{margin:18px 0}
.eff .row{display:flex;align-items:center;gap:14px;margin-bottom:16px}
.eff .lab{width:180px;font-size:14px;color:var(--ink-2);font-weight:500;flex-shrink:0}
.eff .bar{flex:1;background:#EDF0EC;border-radius:10px;height:28px;position:relative;overflow:hidden}
.eff .bar i{position:absolute;left:0;top:0;bottom:0;background:linear-gradient(90deg,var(--jade),var(--ink-2));border-radius:10px;display:block;transition:width 1.2s cubic-bezier(.22,1,.36,1)}
.eff .val{width:120px;font-family:var(--serif);font-weight:700;color:var(--ink);font-size:15px;font-variant-numeric:tabular-nums;text-align:right;flex-shrink:0}

/* Gibbs */
.gibbs{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.gibbs .g{background:var(--card);border:1px solid var(--line);border-radius:14px;padding:20px 18px;transition:transform .25s}
.gibbs .g:hover{transform:translateY(-2px)}
.gibbs .g .gno{font-weight:700;color:var(--amber);font-size:12.5px;letter-spacing:.06em}
.gibbs .g h5{font-family:var(--serif);font-weight:700;color:var(--ink);font-size:16px;margin:5px 0 8px}
.gibbs .g p{font-size:13.5px;color:var(--txt);line-height:1.7;margin:0}

/* 路线图时间轴 */
.timeline{margin:24px 0 0;position:relative;padding-left:0}
.tl{display:grid;grid-template-columns:150px 26px 1fr;gap:0;position:relative}
.tl-time{text-align:right;padding:8px 14px 8px 0;font-family:var(--serif);font-weight:700;color:var(--jade);font-size:15px;line-height:1.5}
.tl-axis{position:relative;display:flex;justify-content:center}
.tl-axis::before{content:"";position:absolute;top:0;bottom:0;width:2px;background:var(--line)}
.tl-dot{position:relative;z-index:2;width:16px;height:16px;border-radius:50%;background:var(--amber);border:3px solid var(--paper);margin-top:18px;box-shadow:0 0 0 2px var(--amber)}
.tl-body{padding:6px 0 28px 18px}
.tl-body h4{font-family:var(--serif);font-weight:700;color:var(--ink);font-size:17.5px;margin-bottom:6px}
.tl-body .goals{display:flex;flex-wrap:wrap;gap:6px;margin-top:10px}
.tl-body .goals span{background:var(--jade-soft);color:var(--ink-2);font-size:12.5px;padding:4px 12px;border-radius:100px;font-weight:500}

/* 反思引文 */
.think{font-family:var(--serif);color:var(--ink);font-size:17.5px;line-height:1.9;background:var(--jade-soft);border-radius:16px;padding:28px 30px;margin:22px 0;position:relative}
.think::before{content:""";position:absolute;top:12px;left:18px;font-size:48px;color:var(--jade);opacity:.25;font-family:Georgia,serif;line-height:1}

/* 引用 */
.refs{font-size:14px}
.refs ol{padding-left:22px}
.refs li{margin-bottom:11px;color:var(--txt);line-height:1.75}
.refs li .src{color:var(--mut);font-size:12.5px;display:block}
.refs a{color:var(--jade);text-decoration:none;border-bottom:1px dotted var(--jade);word-break:break-all}
.refs a:hover{color:var(--ink)}

/* AI声明 */
.ai-decl{background:var(--card);border:1px solid var(--line);border-radius:16px;padding:28px;font-size:14.5px;box-shadow:var(--shadow)}
.ai-decl h3{font-family:var(--serif);color:var(--ink);margin-bottom:14px;font-size:18px}
.ai-decl ul{padding-left:20px}
.ai-decl li{margin-bottom:11px;color:var(--txt);line-height:1.7}

/* 页脚 */
footer{background:var(--ink);color:#C9DED7;padding:44px 0;margin-top:24px}
footer .wrap{display:flex;justify-content:space-between;flex-wrap:wrap;gap:14px;font-size:13.5px}
footer .home{color:#F0B45A;font-weight:600}

/* 简历卡片 - 实心按钮 */
.cv-row{display:flex;gap:14px;flex-wrap:wrap;margin-top:18px}
.cv-btn{display:inline-flex;align-items:center;gap:9px;background:var(--ink);color:#F2F6F2;padding:13px 24px;border-radius:12px;font-weight:600;font-size:14.5px;text-decoration:none;transition:transform .15s,background .15s}
.cv-btn:hover{background:var(--jade);transform:translateY(-2px);color:#fff;text-decoration:none}
.cv-btn.alt{background:var(--amber)}
.cv-btn.alt:hover{background:var(--amber);filter:brightness(1.06)}
.cv-btn svg{width:17px;height:17px;flex-shrink:0}

/* 设计思维条 */
.dt-bar{display:flex;gap:8px;margin:20px 0 8px;flex-wrap:wrap}
.dt-bar span{background:var(--jade-soft);color:var(--ink);font-size:12.5px;font-weight:600;padding:5px 14px;border-radius:100px;border:1px solid rgba(46,125,107,.2)}

/* 关键洞察卡片 */
.insight-box{background:linear-gradient(135deg,var(--jade-soft) 0%,#F0F7F4 100%);border:1px solid rgba(46,125,107,.2);border-radius:14px;padding:18px 22px;margin:18px 0;font-size:14.5px;color:var(--ink);line-height:1.75}
.insight-box strong{color:var(--jade)}

/* 返回顶部 */
.back-top{position:fixed;bottom:28px;right:28px;width:44px;height:44px;background:var(--ink);color:#fff;border:none;border-radius:50%;cursor:pointer;display:none;align-items:center;justify-content:center;font-size:18px;z-index:40;box-shadow:0 4px 16px rgba(20,59,53,.25);transition:transform .2s,background .2s}
.back-top:hover{background:var(--jade);transform:translateY(-2px)}
.back-top.show{display:flex}

/* 响应式 */
@media (max-width:900px){
  .stats{grid-template-columns:repeat(2,1fr)}
  .trio{grid-template-columns:1fr}
  .cols{grid-template-columns:1fr}
  .steps{grid-template-columns:1fr 1fr}
  .gibbs{grid-template-columns:1fr}
  .steps-arrow{display:none}
  .eff .lab{width:130px}
  .eff .val{width:90px}
  .tl{grid-template-columns:92px 20px 1fr}
  .nav-links{display:none}
  section{padding:56px 0}
  .wf-header,.wf-row{grid-template-columns:1fr}
  .wf-mid{padding:6px 0;font-size:16px}
  .wf-header .mid{display:none}
  .chart{height:320px}
}
@media (max-width:520px){
  .steps{grid-template-columns:1fr}
  .hero{padding:72px 0 52px}
}
@media print{
  .nav,.progress-bar,.back-top{display:none}
  body{background:#fff;font-size:12.5px}
  section{padding:24px 0;scroll-margin-top:0}
  .card,.step-card,.gibbs .g{box-shadow:none;border-color:#ccc;break-inside:avoid}
  .hero{padding:32px 0;background:var(--ink)!important;-webkit-print-color-adjust:exact;print-color-adjust:exact}
  .chart{height:260px}
}
</style>
</head>
<body>

<!-- 顶部阅读进度 -->
<div class="progress-bar" id="progressBar"></div>

<!-- ===== 顶栏 ===== -->
<nav class="nav">
  <div class="wrap nav-in">
    <div class="brand">INT6140 · <b>未来工作 ePortfolio</b></div>
    <div class="nav-links">
      <a href="#p1">职业画像</a>
      <a href="#p2">科技剖析</a>
      <a href="#p3">福祉设计</a>
      <a href="#p4">反思与路线图</a>
      <a href="#ref">参考文献</a>
    </div>
  </div>
</nav>

<!-- ===== Hero ===== -->
<header class="hero">
  <div class="wrap">
    <div class="eyebrow">Personal Digital Portfolio · 王俊杰</div>
    <h1>让教师被技术成全<br>生成式AI时代，教育行业的<span class="hl">人才重塑</span>与福祉设计</h1>
    <p class="sub">以数据科学为底、以人力资源为眼、以教育场景为壤——一个 ETFW 硕士生，审视人工智能如何重塑教师的雇佣形态、技能图谱与职业幸福，并为自己规划一条“懂技术·懂教育·懂人才”的未来之路。</p>
    <div class="meta">
      <span class="chip">香港教育大学 GIET · ETFW 硕士</span>
      <span class="chip">数据科学与大数据 本科</span>
      <span class="chip">教育产品经理实习</span>
      <span class="chip">四年教学经验</span>
    </div>
    <div class="stats">
      <div class="stat"><div class="num" data-target="38.2">0</div><div class="lbl">中小学教师处于“亚健康”（《教育家》81,387份问卷）</div></div>
      <div class="stat"><div class="num" data-target="39.09">0</div><div class="lbl">教师存在抑郁、焦虑倾向</div></div>
      <div class="stat"><div class="num" data-target="14.77">0</div><div class="lbl">教师每天使用AI工具（53万样本）</div></div>
      <div class="stat"><div class="num" data-target="96.1">0</div><div class="lbl">教师愿意主动学习生成式AI</div></div>
    </div>
    <div class="hero-note">
      作品集在线访问：<a href="https://4maxpcd33btt1.doubao.link/app/app_17ggp8nvwmu" style="color:#F0B45A;font-weight:600">https://4maxpcd33btt1.doubao.link/app/app_17ggp8nvwmu</a>
    </div>
  </div>
</header>

<!-- ===== 模块一 ===== -->
<section id="p1">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">01</div><div class="sec-title">个人职业画像与未来工作哲学<small>Personal Profiling &amp; Future-Ready Philosophy</small></div></div>

    <div class="card">
      <div class="h2">我是谁：一个“技术 × 教育 × 产品”的交叉体</div>
      <p class="lead">我是王俊杰，香港教育大学全球新兴技术研究所（GIET）“新兴科技赋能人力资源”（ETFW）文学硕士在读生。本科主修数据科学与大数据技术；硕士聚焦新兴科技如何重塑人力资源与未来工作形态；曾在教育科技企业任教育产品经理，参与 AI 教育产品设计；并有四年家教及暑托班教学经验，亲历教师深夜手改试卷、独自制作课件的高负荷日常。</p>
      <p>我把自己定位为一名未来的<span class="em">数字化人力资源与人才发展从业者</span>——服务的对象，正是被人工智能重塑的教师等庞大职业群体。数据科学的训练让我能读得懂技术，教育产品实习让我看得见需求，一线教学让我摸得着痛点；三者交叉，构成了我观察“未来工作”的独特坐标。</p>
      <div class="trio">
        <div class="t"><span class="tag">DATA</span><h4>数据科学本科</h4><p>Python、数据挖掘、机器学习——理解技术逻辑与“用数据诊断组织”的能力。</p></div>
        <div class="t"><span class="tag">HR · ETFW</span><h4>人力资源硕士</h4><p>新兴科技如何重塑雇佣形态、技能图谱与员工福祉——这门课的核心关切。</p></div>
        <div class="t"><span class="tag">EDU · PRODUCT</span><h4>教育产品 + 教学</h4><p>教育产品经理实习 + 四年教学，直击一线教师真实痛点与工作场景。</p></div>
      </div>

    </div>

    <div class="card">
      <div class="h2">个人简历 · My CV</div>
      <p class="mut">欢迎点开我的简历，了解我的教育背景、实习与教学经历、技术与教学技能（中英两版，新窗口打开 PDF）。</p>
      <div class="cv-row">
        <a class="cv-btn" style="display:inline-flex;align-items:center;gap:8px;background:#143B35;color:#F2F6F2;padding:12px 24px;border-radius:14px;font-weight:600;font-size:14.5px;text-decoration:none;margin-right:16px;" href="https://aka.doubaocdn.com/s/IyxaVguyWt" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" width="17" height="17" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
          中文简历（PDF）
        </a>
        <a class="cv-btn alt" style="display:inline-flex;align-items:center;gap:8px;background:#C8872B;color:#FFFFFF;padding:12px 24px;border-radius:14px;font-weight:600;font-size:14.5px;text-decoration:none;" href="https://aka.doubaocdn.com/s/4ZO4iV4QpI" target="_blank" rel="noopener">
          <svg viewBox="0 0 24 24" width="17" height="17" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><polyline points="14 2 14 8 20 8"/></svg>
          English CV（PDF）
        </a>
      </div>
    </div>

    <div class="card">
      <div class="h2">我的未来工作哲学</div>
      <div class="quote">AI 不是教师的替代者，而是教师的“超级助手”。技术接管重复性劳动，把时间还给高价值工作；人机协同时代，最具竞争力的不是会写代码的人，而是能向 AI 清晰提问、并判断其输出质量的人。</div>
      <p>技术处理批改、素材生成、行政事务等重复性劳动，把时间还给个性化辅导、情感关怀与课程设计。情感连接、价值引领与创造力，是 AI 无法复制的人类内核。在我看来，<span class="em">会用 AI 工具利大于弊</span>——文科老师不必会写代码，会用现成工具、会核对结果即可；真正的“未来就绪”，是培养与智能体协作、并对其输出负责的判断力。</p>
    </div>
  </div>
</section>

<!-- ===== 模块二 ===== -->
<section id="p2">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">02</div><div class="sec-title">前沿科技深度剖析：生成式AI如何重塑教师职业<small>Deep-Dive: Emerging Tech &amp; Workforce Transformation</small></div></div>

    <div class="card">
      <div class="h2">2.1 技术聚焦：从生成式AI到智能体工作流</div>
      <p class="lead">生成式AI（Generative AI）能自动生成文本、图像、代码与语音，正走向“教学实践”。尤其随着<span class="em">智能体工作流（Agentic Workflow）</span>兴起，AI 从被动应答的工具，演化为能理解目标、规划步骤并自主完成任务的协作者，系统性地重塑教师的工作流程、雇佣形态与技能图谱。</p>
    </div>

    <div class="card">
      <div class="h2">2.2 行业痛点：教师负荷与职业倦怠的现实</div>
      <p>现实是，大量教师至今仍手改试卷、自制 PPT、手写教案，把时间消耗在机械劳动上。教师职业的减负需求，是 AI 赋能最迫切的现实背景。<strong>《教育家》杂志 2026 年全国中小学教师现状调查</strong>（有效问卷 81,387 份）显示：38.2% 的教师处于“亚健康”、39.09% 存在抑郁焦虑倾向、96.71% 睡眠不足 8 小时。<strong>中国科学院心理研究所 2022 年</strong>对 2 万余名教师的调研亦显示，约半数存在焦虑风险、超两成存在工作倦怠。教师高负荷、低掌控感，是技术介入的合理性基础。</p>
      <div class="chart" id="painChart"></div>
    </div>

    <div class="card">
      <div class="h2">2.3 AI应用现状：意愿高涨，落地受困</div>
      <p><strong>《2025 年中国中小学教师数字素养年度报告》</strong>（覆盖 19 省 53 万教师）显示，仅 14.77% 的教师每天使用 AI、3.41% 从未使用，但 85.17% 认为 AI 能拓展资源、81% 认为能节省备课时间。教育部指导的<strong>《中国教师生成式人工智能应用报告（2026）》</strong>（8.6 万教师）更揭示张力：96.1% 愿主动学习、92.3% 已融入课堂，却有 67.4% 反映“没有合适资源”、62.9% 遇“技术不稳定”、44.8%“不会用”。</p>
      <p class="em" style="color:var(--amber);font-weight:600">渗透的瓶颈不在意愿，而在工具适配与素养培育——这正是本作品集第三章创新方案的出发点。</p>
      <div class="chart chart-sm" id="adoptChart"></div>
    </div>

    <div class="card">
      <div class="h2">2.4 真实案例：AI减负已在真实课堂发生</div>
      <div class="cols">
        <div class="card">
          <div class="h3">案例一 · 烟台牟平育英艺术中学（山东）</div>
          <p>该校研发 AI 拍照阅卷系统：教师手机拍摄答题卡，系统 3–5 分钟即可完成全班批阅并生成可视化学情报告，让“因材施教”规模化落地（齐鲁网·闪电新闻，2025-12）。</p>
        </div>
        <div class="card">
          <div class="h3">案例二 · 成都石室东部新区实验学校（四川）</div>
          <p>作为成都首批“人工智能+教学”试点校，该校接入“文通云”AI 作业批改系统，以“教师手批—人机混合批—AI 智能批”三级体系把教师从重复批改中解放，转向学情驱动的个性化反馈（川观新闻，2025-12）。</p>
        </div>
      </div>
      <p class="mut" style="margin-top:14px">两地实践共同印证：AI 的价值不在“替代教师”，而在把教师从机械劳动中解放出来，回到育人的本质。</p>
    </div>

    <!-- ===== 核心多模态：工作流对比 ===== -->
    <div class="card">
      <div class="h2">2.5 工作流重构：传统教师 vs AI赋能教师</div>
      <p class="mut" style="margin-bottom:16px">以下对比图基于真实教学场景与试点学校实践，直观呈现 AI 如何系统性重构教师日常工作流，并释放高价值时间。</p>
      
      <div class="workflow-compare">
        <div class="wf-header">
          <div class="side trad">传统工作流 · 高负荷手工模式</div>
          <div class="mid">对比</div>
          <div class="side ai">AI赋能工作流 · 人机协同模式</div>
        </div>

        <div class="wf-row">
          <div class="wf-node trad-side">
            <span class="step">① 备课与课件制作</span>
            手动搜集素材、逐页制作PPT、反复调整排版，单次备课常耗时 3–5 小时。
          </div>
          <div class="wf-mid">→</div>
          <div class="wf-node ai-side">
            <span class="step">① AI辅助备课</span>
            输入教学目标与学情，一键生成教案框架 + 课件初稿，教师聚焦个性化调整。
            <span class="wf-save">节省 ≥40%</span>
          </div>
        </div>

        <div class="wf-row">
          <div class="wf-node trad-side">
            <span class="step">② 作业批改与反馈</span>
            逐份手改、统计错题、手写评语，全班批改常占晚间 2–3 小时，反馈滞后。
          </div>
          <div class="wf-mid">→</div>
          <div class="wf-node ai-side">
            <span class="step">② AI智能批改 + 人机混合</span>
            拍照/扫描自动批阅，生成学情报告；教师重点审核疑难题并给出深度反馈。
            <span class="wf-save">节省 ≥60%</span>
          </div>
        </div>

        <div class="wf-row">
          <div class="wf-node trad-side">
            <span class="step">③ 学情分析与分层教学</span>
            依赖经验与零散笔记，难以精准定位每位学生的薄弱点，分层设计耗时费力。
          </div>
          <div class="wf-mid">→</div>
          <div class="wf-node ai-side">
            <span class="step">③ 数据驱动学情诊断</span>
            AI自动聚类错题与知识点掌握度，生成个性化练习建议，支持规模化因材施教。
            <span class="wf-save">效率倍增</span>
          </div>
        </div>

        <div class="wf-row">
          <div class="wf-node trad-side">
            <span class="step">④ 行政与家校沟通</span>
            手工统计成绩、撰写通知、逐一回复家长，挤占核心教学时间。
          </div>
          <div class="wf-mid">→</div>
          <div class="wf-node ai-side">
            <span class="step">④ 智能行政助手</span>
            自动生成成绩汇总、家校沟通草稿，教师把关后一键发送，回归育人核心。
            <span class="wf-save">显著减负</span>
          </div>
        </div>
      </div>

      <div class="wf-insight">
        <strong>关键洞察：</strong>AI 并非简单“替代步骤”，而是重构了价值创造的路径——重复性、标准化工作被接管，教师的核心价值向“判断力、情感连接、课程设计与价值引领”集中。人机协同下的教师，从“时间的奴隶”转变为“时间的主人”。
      </div>
    </div>

    <div class="card">
      <div class="h2">2.6 雇佣形态与技能图谱重塑</div>
      <p>教师角色正从“知识传授者”转向“学习引导者、情感陪伴者与人机协同设计师”，技能图谱从“学科知识+手工技能”迁移至“AI 工具使用+教学判断力+情感关怀+课程设计”，核心价值聚焦于价值引领、情感共振与拥抱不确定性。</p>
      <div class="chart-title">技能图谱重心迁移 · 传统教师 vs AI时代教师</div>
      <div class="chart-cap">雷达图对比六个维度的能力重心（0–100 相对强度，为作者基于本节分析的概念化呈现）</div>
      <div class="chart" id="radarChart"></div>
      <div class="insight-box">
        <strong>技能升值与贬值判断：</strong>纯手工批改、基础课件制作等技能将显著贬值；“精准提问与输出校验”“跨学科课程设计”“情感支持与心理洞察”“数据驱动决策”将成为新的核心竞争力。数据科学背景使我对“数据素养”维度的升值有更直观的体感。
      </div>
    </div>

    <div class="card">
      <div class="h2">2.7 全球化与人口结构视角</div>
      <p>中国教师队伍正面临结构性收缩：国家统计局数据显示，<strong>2025 年全国出生人口 792 万</strong>，较 2016 年峰值 1786 万下降逾 55%；2022–2024 年学前教育专任教师减少 41.23 万人；乡村教师年流失率 6.01%，远高于县城的 2.18%。</p>
      <p>在人力总量收缩与结构失衡下，<span class="em">“用 AI 提升存量教师效率、补充人力缺口”成为必然</span>。国务院《关于深入实施“人工智能+”行动的意见》（2025）与教育部等五部门《“人工智能+教育”行动计划》（2026-04）均明确“赋能教师教学、为教师减负增效”。同时需警惕技术可及性差异可能加剧城乡教育公平问题——这也是后续福祉设计必须回应的伦理维度。</p>
    </div>
  </div>
</section>

<!-- ===== 模块三 ===== -->
<section id="p3">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">03</div><div class="sec-title">未来工作场所与员工福祉创新设计<small>Workplace Environment &amp; Workforce Well-being Design</small></div></div>

    <div class="card">
      <div class="h2">3.1 痛点识别：从员工（教师）视角出发</div>
      <p class="lead">运用设计思维，我从教师这一“雇员”群体的真实处境出发，识别出三重叠加的技术性职场痛点：</p>
      <div class="dt-bar">
        <span>Empathize 共情</span>
        <span>Define 定义</span>
        <span>Ideate 构思</span>
        <span>Prototype 原型</span>
        <span>Test 测试</span>
      </div>
      <div class="trio">
        <div class="t"><span class="tag">痛点一</span><h4>认知门槛高</h4><p>很多文科出身的老师不会编程，误以为“用AI=学写代码”，觉得比自己手动改卷、做PPT还难。其实根本不用写代码——会用现成工具、会提需求就行。44.8% 的教师困于“不会用、学习成本高”，本质是被“技术想象”吓退。</p></div>
        <div class="t"><span class="tag">痛点二</span><h4>工具碎片化</h4><p>需在多个平台间反复切换，缺乏一站式解决方案，67.4% 的教师反映“没有合适的 AI 教育资源”。</p></div>
        <div class="t"><span class="tag">痛点三</span><h4>伦理与负荷焦虑</h4><p>担忧学生过度依赖 AI、数据隐私泄露、生成内容不准确；同时批改与备课的高负荷挤压了教师的休息与陪伴时间。</p></div>
      </div>
    </div>

    <div class="card">
      <div class="h2">3.2 创新方案：“AI教师助手”——教师福祉与 AI 素养发展机制</div>
      <p>区别于常规“上几节课”的培训，我设计了一套<span class="em">以教师福祉为中心、以人才发展为目标的四阶段机制</span>：</p>
      <div class="steps">
        <div class="step-card">
          <span class="no">01</span>
          <div class="ph">认知唤醒</div>
          <div class="win">第 1–2 周</div>
          <p>用真实教学场景工作坊演示 AI 能做什么（拍照阅卷、一键生成教案、自动制作课件），消除“AI 很复杂”的认知障碍，建立“我也能做到”的信心。</p>
          <div class="out">产出：认知破除工作坊 + 信心基线调研</div>
          <span class="steps-arrow">→</span>
        </div>
        <div class="step-card">
          <span class="no">02</span>
          <div class="ph">工具上手</div>
          <div class="win">第 3–4 周</div>
          <p>精选 3–5 个“即学即用”的 AI 工具，配套按备课、上课、批改、评价等场景预设好的“提示词模板库”，教师替换关键词即可上手。</p>
          <div class="out">产出：场景化提示词模板库 + 工具速查卡</div>
          <span class="steps-arrow">→</span>
        </div>
        <div class="step-card">
          <span class="no">03</span>
          <div class="ph">场景深耕</div>
          <div class="win">第 5–8 周</div>
          <p>围绕四大教学场景开展实战演练，每位教师产出一个“AI 赋能教学”案例，在教研组内分享，沉淀为校内最佳实践库。</p>
          <div class="out">产出：个人AI教学案例 + 校级实践库</div>
          <span class="steps-arrow">→</span>
        </div>
        <div class="step-card">
          <span class="no">04</span>
          <div class="ph">持续迭代</div>
          <div class="win">长期</div>
          <p>建立校内 AI 教师互助社群，定期分享心得、共同审核 AI 输出准确性、收集学生反馈，形成“使用—反馈—优化”的闭环。</p>
          <div class="out">产出：社群机制 + 伦理守则落地</div>
        </div>
      </div>

      <div class="quote">福祉机制的关键，不只是“教会用工具”，更是<span style="color:var(--amber)">“时间返还”与“伦理护航”</span>：把 AI 节省的批改时间，制度化地转化为备课深化、学生陪伴与教师休息，防止“减负变增压”；并配套《教师 AI 伦理守则》与数据隐私保护。</div>

      <div class="insight-box">
        <strong>时间返还制度设计（关键福祉落点）：</strong><br>
        • 批改时间节省的 60% 中，至少 30% 强制转化为“学生个别辅导/情感支持时段”；<br>
        • 20% 转化为“深度备课与课程创新时段”；<br>
        • 剩余部分明确为教师休息与个人发展时间，纳入校级工作量核算，避免“省下来的时间被新任务填满”。
      </div>

      <div class="think" style="margin-top:16px">我的真实想法：AI 的目的不是取代教师，而是让老师用现成工具（拍照阅卷、AI 一键绘制 PPT、AI 教案）把重复劳动降下来。老师的角色是“核对者 + 训练者”——只需核对 AI 结果对不对，并通过持续反馈让它的准确率逐步提升。即便偶尔批改有误，学生发现后会主动深究这道题、反过来找老师讨论，反而激发他们对正确答案的追求，也顺势拉近了师生关系。所以我坚定认为：使用 AI 工具，利大于弊。</div>
    </div>

    <div class="card">
      <div class="h2">3.3 预期效果与评估</div>
      <div class="eff">
        <div class="row"><div class="lab">备课时间</div><div class="bar"><i style="width:70%"></i></div><div class="val">减少 ≥ 30%</div></div>
        <div class="row"><div class="lab">作业批改时间</div><div class="bar"><i style="width:90%"></i></div><div class="val">减少 ≥ 60%</div></div>
        <div class="row"><div class="lab">职业倦怠感</div><div class="bar"><i style="width:55%"></i></div><div class="val">显著下降</div></div>
        <div class="row"><div class="lab">工具独立使用率</div><div class="bar"><i style="width:80%"></i></div><div class="val">3个月内 ≥ 80%</div></div>
      </div>
      <p class="mut">评估采用“效率 + 福祉 + 质量 + 采纳”四维指标，AI 内容准确率经“教师审核 + 学生反馈”双轨校验。福祉维度将引入简易倦怠量表与睡眠质量追踪，确保“减负”真正转化为教师主观幸福感的提升。</p>
    </div>
  </div>
</section>

<!-- ===== 模块四 ===== -->
<section id="p4">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">04</div><div class="sec-title">学习反思与未来行动路线图<small>Reflective Learning Journey &amp; Strategic Career Roadmap</small></div></div>

    <div class="card">
      <div class="h2">4.1 结构化反思（Gibbs 反思循环）</div>
      <div class="think">“我最大的认知转折，是从‘技术崇拜’走向‘人机协同’：真正有价值的不是会用 AI 工具，而是知道在什么场景用、如何用、能否判断输出质量。”</div>
      <div class="gibbs">
        <div class="g"><div class="gno">DESCRIPTION · 描述</div><h5>我看见了什么</h5><p>课程初期，我把 AI 视为“提高效率的技术工具”。随着学习深入，我意识到它正在重新定义“工作的本质”——竞争力从“谁会写代码”转向“谁会提问、谁有判断力”。</p></div>
        <div class="g"><div class="gno">FEELINGS · 感受</div><h5>我的情绪变化</h5><p>我曾担忧被 AI 取代而一度职业焦虑，但当我用 AI 代理完成网页与小游戏时，真切体会到“AI 是放大器，不是替代者”。交叉背景既是优势，也可能变成“什么都懂一点但都不深”的陷阱，这种张力促使我更聚焦。</p></div>
        <div class="g"><div class="gno">EVALUATION · 评估</div><h5>什么最有价值</h5><p>数据科学背景让我理解技术逻辑，教育产品实习让我理解用户需求，教学经验让我理解真实痛点——三者的交叉，正是我在 AI 时代最稀缺的核心竞争力。</p></div>
        <div class="g"><div class="gno">ANALYSIS · 分析</div><h5>与课程目标对表</h5><p>CILO1 让我看清 AI 重塑产业与技能；CILO2 让我找到福祉切入点；CILO3 让我理解人口结构约束；CILO4 让我明确战略方向。四者共同构成“技术—人—组织—战略”的完整分析框架。</p></div>
        <div class="g"><div class="gno">CONCLUSION · 结论</div><h5>我的立场</h5><p>AI 越强大，“人”的部分越珍贵。教师最不可替代的价值在于价值引领、情感陪伴与创造性教学——技术应当放大这些，而非侵蚀它们。我会持续站在“成全教师”而非“替代教师”的立场上行动。</p></div>
        <div class="g"><div class="gno">ACTION · 行动</div><h5>我接下来做什么</h5><p>把认知转化为可落地的行动：深度使用 AI 教育工具、推动 AI 功能落地、并在未来两年深耕“教育 × 人力资源数字化”这一交叉领域，成为连接技术与教师福祉的桥梁型人才。</p></div>
      </div>
    </div>

    <div class="card">
      <div class="h2">4.2 未来 1–2 年职业适应性战略路线图</div>
      <div class="timeline">
        <div class="tl">
          <div class="tl-time">短期 · 3个月</div>
          <div class="tl-axis"><span class="tl-dot"></span></div>
          <div class="tl-body"><h4>扎根：建立 AI 教育实践底座</h4><p>深入使用 2–3 个 AI 教育工具，完成 5 个“AI+教学”实战案例；精读权威报告，养成数据驱动决策习惯。成功指标：案例可对外分享、工具使用达到熟练。</p>
          <div class="goals"><span>AI教育工具 ×2-3</span><span>实战案例 ×5</span><span>数据决策习惯</span></div></div>
        </div>
        <div class="tl">
          <div class="tl-time">中期 · 6个月</div>
          <div class="tl-axis"><span class="tl-dot"></span></div>
          <div class="tl-body"><h4>验证：推动真实场景落地</h4><p>在教育产品实习中推动至少 1 个 AI 功能落地；参与 AI 教育行业社群，建立人脉网络。风险应对：若功能落地受阻，转向小范围教师共创试点。</p>
          <div class="goals"><span>AI功能落地 ×1</span><span>行业人脉</span><span>多模态制品</span></div></div>
        </div>
        <div class="tl">
          <div class="tl-time">长期 · 1–2年</div>
          <div class="tl-axis"><span class="tl-dot"></span></div>
          <div class="tl-body"><h4>深耕：成为“教育×人才数字化”复合型人才</h4><p>进入教育科技或人力资源数字化领域，成为“懂技术 + 懂教育 + 懂产品 + 懂人才”的复合型从业者；推动 AI 工具在更多学校落地，为教师减负、为福祉增值。</p>
          <div class="goals"><span>复合型人才</span><span>AI减负落地</span><span>持续学习</span></div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ===== 参考文献 ===== -->
<section id="ref">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">◆</div><div class="sec-title">参考文献<small>References（正文引用除外，不计入字数）</small></div></div>
    <div class="card refs">
      <ol>
        <li>教育部等五部门. “人工智能+教育”行动计划（教科信〔2026〕1号）[Z]. 2026-04-10.<span class="src"><a href="https://www.gov.cn/zhengce/zhengceku/202604/content_7065138.htm" target="_blank" rel="noopener">gov.cn/zhengce/zhengceku/202604/content_7065138.htm</a></span></li>
        <li>国务院. 关于深入实施“人工智能+”行动的意见（国发〔2025〕11号）[Z]. 2025-08-26.<span class="src"><a href="https://www.gov.cn/zhengce/zhengceku/202508/content_7037862.htm" target="_blank" rel="noopener">gov.cn/zhengce/zhengceku/202508/content_7037862.htm</a></span></li>
        <li>教育部教育技术与资源发展中心（中央电化教育馆）组编, 教育部教师工作司指导. 中国教师生成式人工智能应用报告(2026)[R]. 2026-05-12.<span class="src"><a href="https://www.ncet.edu.cn/zhuzhan/syzyxw/20260514/6764.html" target="_blank" rel="noopener">ncet.edu.cn/zhuzhan/syzyxw/20260514/6764.html</a></span></li>
        <li>中国教育发展战略学会区域教育专业委员会. 2025年中国中小学教师数字素养年度报告[R]. 2026-05-12.<span class="src"><a href="https://m.gmw.cn/2026-05/12/content_1304453633.htm" target="_blank" rel="noopener">m.gmw.cn/2026-05/12/content_1304453633.htm</a></span></li>
        <li>中国教育发展战略学会区域教育专业委员会, 学科网等. 2025年中小学教师人群应用人工智能情况调研报告[R]. 2025.<span class="src"><a href="https://app.xinhuanet.com/news/article.html?articleId=5538e9f61ad23921dc89bcb4aa9c4791" target="_blank" rel="noopener">app.xinhuanet.com/news/article.html?articleId=5538e9f61ad23921dc89bcb4aa9c4791</a></span></li>
        <li>《教育家》杂志. 全国中小学教师现状调查报告[R]. 2026-01-14.<span class="src"><a href="http://psy.china.com.cn/2026-01/20/content_43338041.htm" target="_blank" rel="noopener">psy.china.com.cn/2026-01/20/content_43338041.htm</a></span></li>
        <li>中国科学院心理研究所. 中国国民心理健康发展报告（2021～2022）[R]. 2022.<span class="src"><a href="https://www.psych.ac.cn/news/zhxw/202302/t20230224_6682792.html" target="_blank" rel="noopener">psych.ac.cn/news/zhxw/202302/t20230224_6682792.html</a></span></li>
        <li>中国教育科学研究院. 中小学教师工作量专项调查[R]. 2018.<span class="src"><a href="http://www.news.cn/politics/2021-09/10/c_1127846273.htm" target="_blank" rel="noopener">news.cn/politics/2021-09/10/c_1127846273.htm</a></span></li>
        <li>国家统计局. 中华人民共和国2025年国民经济和社会发展统计公报[R]. 2026-02-28.<span class="src"><a href="https://www.stats.gov.cn/xxgk/sjfb/tjgb2020/202602/t20260228_1962662.html" target="_blank" rel="noopener">stats.gov.cn/xxgk/sjfb/tjgb2020/202602/t20260228_1962662.html</a></span></li>
        <li>教育部. 2024年全国教育事业发展统计公报[R]. 2025-06-11.<span class="src"><a href="http://www.moe.gov.cn/jyb_sjzl/sjzl_fztjgb/202506/t20250611_1193760.html" target="_blank" rel="noopener">moe.gov.cn/jyb_sjzl/sjzl_fztjgb/202506/t20250611_1193760.html</a></span></li>
        <li>齐鲁网·闪电新闻. 烟台市牟平区：AI阅卷 让因材施教落地[N]. 2025-12-02.<span class="src"><a href="http://m.toutiao.com/group/7579140496870703650" target="_blank" rel="noopener">m.toutiao.com/group/7579140496870703650</a></span></li>
        <li>川观新闻. AI也能批改作业了，“人机双师”如何实现“1+1&gt;2”[N]. 2025-12-18.<span class="src"><a href="https://cbgc.scol.com.cn/news/7079510" target="_blank" rel="noopener">cbgc.scol.com.cn/news/7079510</a></span></li>
        <li>澎湃新闻. 身心俱疲的老师教不好学生（《教育家》报告解读）[N]. 2026-01-22.<span class="src"><a href="https://www.thepaper.cn/newsDetail_forward_32446902" target="_blank" rel="noopener">thepaper.cn/newsDetail_forward_32446902</a></span></li>
      </ol>
    </div>
  </div>
</section>

<!-- ===== AI使用声明 ===== -->
<section id="decl">
  <div class="wrap">
    <div class="sec-head"><div class="sec-no">◆</div><div class="sec-title">生成式AI使用声明<small>Generative AI Usage Declaration</small></div></div>
    <div class="ai-decl">
      <h3>本人在完成本作品集过程中的 AI 使用情况</h3>
      <ul>
        <li><strong>资料检索与整理</strong>：使用 AI 辅助检索并整理关于教师工作负担、AI 教育应用现状的公开数据与政策文件，并对检索结果进行交叉验证以确保数据真实可溯源。</li>
        <li><strong>数据分析</strong>：使用 AI 辅助对行业报告数据进行分类归纳与趋势分析；本作品集引用的所有数字均经原始报告或权威媒体报道核实，未使用 AI 编造任何数据或案例。</li>
        <li><strong>内容撰写</strong>：核心论点构建、案例分析、个人反思均由本人独立完成；AI 仅在语言润色、结构编排与可视化制品的技术实现上提供辅助。</li>
        <li><strong>人机分工边界</strong>：AI 作为信息检索与表达辅助助手，本人作为分析判断与内容创作的主体；所有引用均标注来源，所有观点均为本人独立思考的结果。</li>
      </ul>
    </div>
  </div>
</section>

<!-- ===== 页脚 ===== -->
<footer>
  <div class="wrap">
    <div class="home">王俊杰 · 香港教育大学 GIET · INT6140 个人数字化反思作品集</div>
    <div>数据来源均已标注 · 本作品集核心论述约 2000 字（引用除外）</div>
  </div>
  <div class="wrap" style="margin-top:12px;padding-top:14px;border-top:1px solid rgba(255,255,255,.16);font-size:13px">
    <span>本作品集在线访问（公开链接）：</span>
    <a href="https://4maxpcd33btt1.doubao.link/app/app_17ggp8nvwmu" style="color:#F0B45A;font-weight:600">https://4maxpcd33btt1.doubao.link/app/app_17ggp8nvwmu</a>
  </div>
</footer>

<!-- 返回顶部 -->
<button class="back-top" id="backTop" title="返回顶部">↑</button>

<script>
(function(){
  // ===== 阅读进度条 =====
  const progressBar = document.getElementById('progressBar');
  window.addEventListener('scroll', () => {
    const scrollTop = window.scrollY;
    const docHeight = document.documentElement.scrollHeight - window.innerHeight;
    const progress = docHeight > 0 ? (scrollTop / docHeight) * 100 : 0;
    progressBar.style.width = progress + '%';
    
    // 返回顶部按钮
    const backTop = document.getElementById('backTop');
    if (scrollTop > 400) backTop.classList.add('show');
    else backTop.classList.remove('show');
  });
  document.getElementById('backTop').addEventListener('click', () => {
    window.scrollTo({top: 0, behavior: 'smooth'});
  });

  // ===== Hero 数字滚动动画 =====
  function animateNumbers() {
    const nums = document.querySelectorAll('.stat .num');
    nums.forEach(el => {
      const target = parseFloat(el.getAttribute('data-target'));
      const isDecimal = target % 1 !== 0;
      let current = 0;
      const duration = 1600;
      const start = performance.now();
      function update(now) {
        const elapsed = now - start;
        const progress = Math.min(elapsed / duration, 1);
        const eased = 1 - Math.pow(1 - progress, 3);
        current = target * eased;
        el.textContent = isDecimal ? current.toFixed(2) : Math.round(current);
        if (progress < 1) requestAnimationFrame(update);
        else el.textContent = isDecimal ? target.toFixed(2) : target;
      }
      requestAnimationFrame(update);
    });
  }
  // 触发一次
  setTimeout(animateNumbers, 300);

  // ===== 图表 =====
  var jade='#2E7D6B', amber='#C8872B', ink='#143B35', mut='#6B7C76', grid='#EDF0EC';
  var AX={color:mut,fontSize:12};
  function base(o){
    return Object.assign({grid:{left:8,right:30,top:24,bottom:8,containLabel:true},
      tooltip:{trigger:'axis',axisPointer:{type:'shadow'},confine:true},
      color:[amber]}, o);
  }
  // 2.2 教师身心健康与负荷
  var pain = echarts.init(document.getElementById('painChart'));
  pain.setOption(base({
    title:{text:'教师身心健康与负荷（2026《教育家》调查，n=81,387）',textStyle:{fontSize:15,fontWeight:600,color:ink},left:0},
    grid:{left:8,right:40,top:44,bottom:8,containLabel:true},
    xAxis:{type:'value',max:100,axisLabel:{...AX,formatter:'{value}%'},splitLine:{lineStyle:{color:grid}}},
    yAxis:{type:'category',inverse:true,data:['睡眠不足8小时','存在抑郁/焦虑倾向','处于“亚健康”','自评“非常健康”'],axisLabel:AX,axisLine:{lineStyle:{color:ink}}},
    series:[{type:'bar',data:[96.71,39.09,38.2,8.14],barWidth:'52%',
      label:{show:true,position:'right',formatter:'{c}%',fontWeight:700,color:ink,fontFamily:'Noto Serif SC'},
      itemStyle:{color:amber,borderRadius:[0,6,6,0]},
      emphasis:{itemStyle:{color:'#B07522'}}}]
  }));
  // 2.3 意愿高企 vs 实际使用偏低
  var adopt = echarts.init(document.getElementById('adoptChart'));
  adopt.setOption(base({
    title:{text:'认知意愿高企 vs 实际使用偏低（%）',textStyle:{fontSize:15,fontWeight:600,color:ink},left:0},
    grid:{left:8,right:40,top:44,bottom:8,containLabel:true},
    xAxis:{type:'value',max:100,axisLabel:{...AX,formatter:'{value}%'},splitLine:{lineStyle:{color:grid}}},
    yAxis:{type:'category',inverse:true,
      data:['愿意主动学习生成式AI','已将AI融入课堂教学','认为AI能拓展教学资源','认为AI能节省备课时间','每天使用AI工具','从未使用过AI'],
      axisLabel:AX,axisLine:{lineStyle:{color:ink}}},
    series:[{type:'bar',data:[96.1,92.3,85.17,81,14.77,3.41],barWidth:'52%',
      label:{show:true,position:'right',formatter:'{c}%',fontWeight:700,color:ink,fontFamily:'Noto Serif SC'},
      itemStyle:{color:function(p){return p.dataIndex>=4?mut:jade},borderRadius:[0,6,6,0]},
      emphasis:{itemStyle:{opacity:0.85}}}]
  }));
  // 2.5 技能图谱雷达
  var radar = echarts.init(document.getElementById('radarChart'));
  radar.setOption({
    color:[amber,jade],
    tooltip:{trigger:'item',confine:true},
    legend:{bottom:0,data:['传统教师','AI时代教师'],icon:'circle',itemWidth:10,itemHeight:10,textStyle:{color:mut,fontSize:12}},
    radar:{indicator:[
      {name:'学科知识',max:100},{name:'教学判断力',max:100},{name:'AI工具使用',max:100},
      {name:'情感关怀',max:100},{name:'课程设计',max:100},{name:'数据素养',max:100}],
      radius:'62%',center:['50%','46%'],
      axisName:{color:ink,fontSize:12,fontWeight:600},
      splitArea:{areaStyle:{color:['rgba(46,125,107,.04)','rgba(46,125,107,.08)']}},
      splitLine:{lineStyle:{color:grid}},axisLine:{lineStyle:{color:grid}}},
    series:[{type:'radar',areaStyle:{opacity:.18},
      data:[
        {value:[95,62,15,68,58,20],name:'传统教师',lineStyle:{color:amber,width:2},itemStyle:{color:amber}},
        {value:[80,90,90,85,85,75],name:'AI时代教师',lineStyle:{color:jade,width:2},itemStyle:{color:jade}}
      ]}]
  });
  window.addEventListener('resize',function(){pain.resize();adopt.resize();radar.resize();});

  // 导航高亮当前导航
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a');
  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(sec => {
      const top = sec.offsetTop - 80;
      if (window.scrollY >= top) current = sec.getAttribute('id');
    });
    navLinks.forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href') === '#' + current) link.classList.add('active');
    });
  });
})();
</script>
</body>
</html>
<!-- （注：内容由AI生成） -->
