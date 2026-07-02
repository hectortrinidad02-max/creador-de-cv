<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; font-src https://fonts.gstatic.com; img-src 'self' data:; script-src 'self' 'unsafe-inline'; connect-src 'none'; frame-src 'none'; object-src 'none'; base-uri 'none';">
<title>Generador de CV Profesional</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&family=IBM+Plex+Mono:wght@400;500;600&family=JetBrains+Mono:wght@400;600;700&family=Work+Sans:wght@400;500;600&family=Bebas+Neue&family=Playfair+Display:wght@600;700;800&family=Source+Sans+3:wght@400;500;600&family=Poppins:wght@400;500;600;700&family=Nunito+Sans:wght@400;600;700&family=Cormorant+Garamond:wght@500;600;700&family=Lora:wght@400;500;600&family=Fraunces:opsz,wght@9..144,500;9..144,600;9..144,700&family=Oswald:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=Sora:wght@500;600;700;800&family=Manrope:wght@500;600;700&display=swap" rel="stylesheet">
<style>
/* ============ APP SHELL TOKENS ============ */
:root{
  --app-bg:#EEF0F4;
  --app-panel:#FFFFFF;
  --app-ink:#171A21;
  --app-ink-soft:#5B6070;
  --app-line:#DDE1E9;
  --app-accent:#3730A9;
  --app-accent-soft:#E7E5FB;
  --app-mono:'IBM Plex Mono', monospace;
  --app-display:'Space Grotesk', sans-serif;
  --app-body:'Inter', sans-serif;
  --radius:14px;
}
*{box-sizing:border-box;}
html,body{margin:0;padding:0;}
body{
  background:var(--app-bg);
  color:var(--app-ink);
  font-family:var(--app-body);
  -webkit-font-smoothing:antialiased;
}

/* ============ APP HEADER ============ */
.app-topbar{
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:18px 32px;
  background:var(--app-panel);
  border-bottom:1px solid var(--app-line);
  position:sticky;
  top:0;
  z-index:20;
}
.app-brand{display:flex; align-items:center; gap:12px;}
.app-brand-mark{
  width:34px;height:34px;border-radius:9px;
  background:linear-gradient(135deg,#3730A9,#6C63FF);
  display:flex;align-items:center;justify-content:center;
  color:#fff;font-family:var(--app-mono);font-weight:600;font-size:13px;
}
.app-brand-text h1{
  font-family:var(--app-display);
  font-size:16px;
  margin:0;
  letter-spacing:.2px;
}
.app-brand-text p{
  margin:0;
  font-size:12px;
  color:var(--app-ink-soft);
  font-family:var(--app-mono);
}
.security-chip{
  display:flex;align-items:center;gap:6px;
  font-family:var(--app-mono);
  font-size:11.5px;
  color:#1C7C4E;
  background:#EAF8F0;
  border:1px solid #BFE9D3;
  padding:6px 12px;
  border-radius:999px;
}
.security-chip svg{width:13px;height:13px;flex-shrink:0;}

/* ============ LAYOUT ============ */
.app-layout{
  display:grid;
  grid-template-columns:400px 1fr;
  gap:0;
  min-height:calc(100vh - 71px);
  align-items:start;
}
.form-panel{
  padding:28px 26px 80px;
  border-right:1px solid var(--app-line);
  background:var(--app-panel);
  height:calc(100vh - 71px);
  overflow-y:auto;
  position:sticky;
  top:71px;
}
.preview-panel{
  padding:36px;
  display:flex;
  flex-direction:column;
  align-items:center;
  gap:18px;
}

/* ============ FORM ELEMENTS ============ */
.form-step{
  margin-bottom:26px;
}
.form-step-label{
  display:flex;align-items:center;gap:8px;
  font-family:var(--app-mono);
  font-size:11px;
  color:var(--app-ink-soft);
  text-transform:uppercase;
  letter-spacing:.08em;
  margin-bottom:10px;
}
.form-step-label .num{
  width:18px;height:18px;border-radius:5px;
  background:var(--app-accent-soft);
  color:var(--app-accent);
  display:flex;align-items:center;justify-content:center;
  font-size:10.5px;font-weight:600;
}
.field{margin-bottom:12px;}
.field label{
  display:block;
  font-size:12.5px;
  font-weight:600;
  margin-bottom:5px;
  color:var(--app-ink);
}
.field-hint{font-size:11px;color:var(--app-ink-soft); margin-top:4px;}
.two-col{display:grid; grid-template-columns:1fr 1fr; gap:10px;}
input[type=text],input[type=email],input[type=tel],input[type=month],select,textarea{
  width:100%;
  padding:9px 11px;
  border:1.4px solid var(--app-line);
  border-radius:9px;
  font-family:var(--app-body);
  font-size:13.5px;
  color:var(--app-ink);
  background:#FCFCFD;
  outline:none;
  transition:border-color .15s;
}
input:focus,select:focus,textarea:focus{border-color:var(--app-accent);}
textarea{resize:vertical; min-height:64px; line-height:1.4;}
select{appearance:none; background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='10' height='6'%3E%3Cpath d='M0 0l5 6 5-6z' fill='%235B6070'/%3E%3C/svg%3E"); background-repeat:no-repeat; background-position:right 12px center;}

.entry-card{
  border:1.4px dashed var(--app-line);
  border-radius:11px;
  padding:12px;
  margin-bottom:10px;
  position:relative;
  background:#FBFBFC;
}
.entry-remove{
  position:absolute; top:8px; right:8px;
  background:none; border:none; cursor:pointer;
  color:#B33636; font-size:11px; font-family:var(--app-mono);
  padding:2px 6px;
}
.btn-add{
  width:100%;
  padding:9px;
  border-radius:9px;
  border:1.4px solid var(--app-accent);
  background:#fff;
  color:var(--app-accent);
  font-weight:600;
  font-size:12.5px;
  cursor:pointer;
  font-family:var(--app-body);
}
.btn-add:hover{background:var(--app-accent-soft);}

.btn-primary{
  width:100%;
  padding:12px;
  border-radius:10px;
  border:none;
  background:var(--app-ink);
  color:#fff;
  font-weight:600;
  font-size:13.5px;
  cursor:pointer;
  font-family:var(--app-body);
  display:flex;align-items:center;justify-content:center;gap:8px;
}
.btn-primary:hover{background:#000;}

.objective-row{display:flex; align-items:center; justify-content:space-between; margin-bottom:5px;}
.btn-mini{
  font-family:var(--app-mono);
  font-size:10.5px;
  color:var(--app-accent);
  background:var(--app-accent-soft);
  border:none;
  padding:4px 8px;
  border-radius:6px;
  cursor:pointer;
}

/* ============ PREVIEW TOOLBAR ============ */
.preview-toolbar{
  width:100%;
  max-width:794px;
  display:flex;
  align-items:center;
  justify-content:space-between;
}
.theme-tag{
  font-family:var(--app-mono);
  font-size:11.5px;
  color:var(--app-ink-soft);
  display:flex;align-items:center;gap:8px;
}
.theme-swatch{width:12px;height:12px;border-radius:3px; display:inline-block;}
.download-btn{
  padding:10px 18px;
  border-radius:9px;
  border:none;
  background:var(--app-accent);
  color:#fff;
  font-weight:600;
  font-size:12.5px;
  cursor:pointer;
  font-family:var(--app-body);
  display:flex; align-items:center; gap:7px;
}
.download-btn:hover{background:#2b258a;}

/* ============ CV SHEET (shared skeleton) ============ */
.cv-sheet-wrap{
  width:100%;
  max-width:794px;
  box-shadow:0 1px 3px rgba(20,20,30,.08), 0 20px 45px -25px rgba(20,20,30,.35);
  background:#fff;
}
.cv{
  --t-bg:#FFFFFF;
  --t-primary:#2451B7;
  --t-secondary:#1F2430;
  --t-ink:#1F2430;
  --t-ink-soft:#5A5F70;
  --t-panel:#F4F5F7;
  --t-display:'Manrope', sans-serif;
  --t-body:'Inter', sans-serif;
  --t-mono:'IBM Plex Mono', monospace;
  width:794px;
  min-height:1123px;
  background:var(--t-bg);
  color:var(--t-ink);
  font-family:var(--t-body);
  position:relative;
  overflow:hidden;
}
.cv-header{
  position:relative;
  padding:38px 44px 26px;
  display:flex;
  align-items:center;
  gap:20px;
  overflow:hidden;
}
.cv-avatar{
  width:70px;height:70px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-family:var(--t-display);
  font-weight:700;
  font-size:24px;
  flex-shrink:0;
  z-index:2;
}
.cv-heading{z-index:2; flex:1;}
.cv-name{
  font-family:var(--t-display);
  font-size:30px;
  margin:0 0 3px;
  line-height:1.1;
  font-weight:700;
}
.cv-role{
  margin:0;
  font-size:13.5px;
  font-family:var(--t-mono);
  letter-spacing:.03em;
}
.cv-contact{
  padding:10px 44px;
  display:flex;
  flex-wrap:wrap;
  gap:4px 18px;
  font-size:11.3px;
  border-bottom:1px solid rgba(0,0,0,.08);
}
.cv-contact span{display:flex; align-items:center; gap:5px; color:var(--t-ink-soft);}
.cv-objective{padding:20px 44px 4px;}
.cv-objective h2, .cv-body h2{
  font-family:var(--t-display);
  font-size:12.5px;
  text-transform:uppercase;
  letter-spacing:.09em;
  margin:0 0 8px;
  color:var(--t-primary);
  display:flex; align-items:center; gap:8px;
}
.cv-objective p{margin:0; font-size:12.8px; line-height:1.55; color:var(--t-ink);}
.cv-body{display:grid; grid-template-columns:1fr 240px; gap:0; padding:14px 0 30px;}
.cv-main{padding:12px 22px 0 44px;}
.cv-sidebar{padding:12px 44px 0 22px; border-left:1px solid rgba(0,0,0,.07);}
.cv-main section, .cv-sidebar section{margin-bottom:22px;}
.exp-item, .edu-item{margin-bottom:14px;}
.exp-item-top{display:flex; justify-content:space-between; align-items:baseline; gap:10px;}
.exp-title{font-weight:600; font-size:13px; color:var(--t-ink);}
.exp-company{font-size:12px; color:var(--t-primary); font-weight:500;}
.exp-dates{font-size:10.8px; font-family:var(--t-mono); color:var(--t-ink-soft); white-space:nowrap;}
.exp-desc{font-size:11.8px; color:var(--t-ink-soft); line-height:1.5; margin:4px 0 0;}
.edu-degree{font-weight:600; font-size:12.8px;}
.edu-school{font-size:11.8px; color:var(--t-ink-soft);}
.edu-dates{font-size:10.6px; font-family:var(--t-mono); color:var(--t-ink-soft);}
.skill-pill{
  display:inline-block;
  font-size:10.8px;
  padding:4px 10px;
  border-radius:999px;
  margin:0 5px 6px 0;
  background:var(--t-panel);
  color:var(--t-ink);
  border:1px solid rgba(0,0,0,.06);
}
.lang-item{display:flex; justify-content:space-between; font-size:11.8px; margin-bottom:5px;}
.lang-item span:last-child{color:var(--t-ink-soft); font-size:10.6px; font-family:var(--t-mono);}
.cert-item{font-size:11.5px; margin-bottom:6px; line-height:1.4; color:var(--t-ink-soft);}
.cert-item b{color:var(--t-ink); display:block; font-size:11.8px; font-weight:600;}
.empty-note{font-size:11px; color:#aaa; font-style:italic;}

/* ============ THEME: GENERAL ============ */
.cv[data-theme="general"]{ --t-primary:#2451B7; --t-secondary:#1F2430; --t-panel:#F1F4FA; --t-display:'Manrope',sans-serif; }
.cv[data-theme="general"] .cv-header{background:var(--t-panel);}
.cv[data-theme="general"] .cv-avatar{background:var(--t-primary); color:#fff;}

/* ============ THEME: TECH ============ */
.cv[data-theme="tech"]{ --t-primary:#4F7CFF; --t-secondary:#22D3AE; --t-ink:#0B1220; --t-ink-soft:#5B677E; --t-panel:#EEF2FF; --t-display:'JetBrains Mono',monospace; --t-mono:'JetBrains Mono',monospace; }
.cv[data-theme="tech"] .cv-header{background:#0B1220; color:#fff;}
.cv[data-theme="tech"] .cv-name{color:#fff;}
.cv[data-theme="tech"] .cv-role{color:var(--t-secondary);}
.cv[data-theme="tech"] .cv-role::before{content:'> ';}
.cv[data-theme="tech"] .cv-avatar{background:linear-gradient(135deg,var(--t-primary),var(--t-secondary)); color:#0B1220;}
.cv[data-theme="tech"] .cv-objective h2::before, .cv[data-theme="tech"] .cv-body h2::before{content:'//'; color:var(--t-secondary); font-family:'JetBrains Mono',monospace;}
.cv[data-theme="tech"] .skill-pill{font-family:'JetBrains Mono',monospace; background:#0B1220; color:var(--t-secondary); border:none;}
.cv[data-theme="tech"] .cv-contact{background:#F5F7FF;}

/* ============ THEME: DESIGN ============ */
.cv[data-theme="design"]{ --t-primary:#FF3D6E; --t-secondary:#FFD23F; --t-ink:#161616; --t-ink-soft:#6b6b6b; --t-panel:#FFF1F5; --t-display:'Bebas Neue',sans-serif; --t-body:'Work Sans',sans-serif; }
.cv[data-theme="design"] .cv-header{background:var(--t-ink); clip-path:polygon(0 0,100% 0,100% 88%,0 100%);}
.cv[data-theme="design"] .cv-name{color:#fff; font-size:38px; letter-spacing:.5px;}
.cv[data-theme="design"] .cv-role{color:var(--t-secondary); font-family:'Work Sans',sans-serif; font-weight:600; text-transform:uppercase; letter-spacing:.08em;}
.cv[data-theme="design"] .cv-avatar{background:var(--t-primary); color:#fff; border-radius:10px;}
.cv[data-theme="design"] .cv-objective h2, .cv[data-theme="design"] .cv-body h2{color:var(--t-primary); font-family:'Bebas Neue',sans-serif; font-size:16px; letter-spacing:.06em;}
.cv[data-theme="design"] .skill-pill{background:var(--t-primary); color:#fff; border:none; font-weight:600;}
.cv[data-theme="design"] .cv-contact{background:var(--t-panel);}

/* ============ THEME: BUSINESS ============ */
.cv[data-theme="business"]{ --t-primary:#0F1E3D; --t-secondary:#C9A227; --t-ink:#1B1B1B; --t-ink-soft:#666; --t-panel:#F8F6EF; --t-display:'Playfair Display',serif; --t-body:'Source Sans 3',sans-serif; --t-mono:'Source Sans 3',sans-serif; }
.cv[data-theme="business"] .cv-header{background:var(--t-panel); flex-direction:column; text-align:center; padding-top:44px;}
.cv[data-theme="business"] .cv-heading{text-align:center;}
.cv[data-theme="business"] .cv-name{font-size:32px;}
.cv[data-theme="business"] .cv-role{font-family:'Source Sans 3',sans-serif; letter-spacing:.15em; text-transform:uppercase; font-size:11px; color:var(--t-secondary); font-weight:600;}
.cv[data-theme="business"] .cv-header::after{content:''; position:absolute; bottom:0; left:44px; right:44px; height:2px; background:var(--t-secondary);}
.cv[data-theme="business"] .cv-avatar{background:var(--t-primary); color:var(--t-secondary); border-radius:4px;}
.cv[data-theme="business"] .cv-objective h2, .cv[data-theme="business"] .cv-body h2{font-family:'Playfair Display',serif; font-weight:700; color:var(--t-primary); letter-spacing:.02em;}
.cv[data-theme="business"] .skill-pill{background:transparent; border:1px solid var(--t-secondary); color:var(--t-primary);}

/* ============ THEME: HEALTH ============ */
.cv[data-theme="health"]{ --t-primary:#0E7C7B; --t-secondary:#4FB8B0; --t-ink:#1D2B2A; --t-ink-soft:#5C6E6D; --t-panel:#EAF6F6; --t-display:'Poppins',sans-serif; --t-body:'Nunito Sans',sans-serif; --t-mono:'Nunito Sans',sans-serif; }
.cv[data-theme="health"] .cv-header{background:var(--t-panel);}
.cv[data-theme="health"] .cv-avatar{background:var(--t-primary); color:#fff;}
.cv[data-theme="health"] .cv-role::before{content:'+ '; color:var(--t-primary); font-weight:700;}
.cv[data-theme="health"] .cv-objective h2, .cv[data-theme="health"] .cv-body h2{color:var(--t-primary);}
.cv[data-theme="health"] .skill-pill{background:#fff; color:var(--t-primary); border:1px solid var(--t-secondary); border-radius:999px;}
.cv[data-theme="health"] .exp-title, .cv[data-theme="health"] .edu-degree{font-family:'Poppins',sans-serif;}

/* ============ THEME: LEGAL ============ */
.cv[data-theme="legal"]{ --t-primary:#6B1E2B; --t-secondary:#22201E; --t-ink:#22201E; --t-ink-soft:#6b645c; --t-panel:#F7F3EC; --t-display:'Cormorant Garamond',serif; --t-body:'Lora',serif; --t-mono:'Lora',serif; }
.cv[data-theme="legal"] .cv-header{background:#fff; border-bottom:3px double var(--t-primary); padding-bottom:22px;}
.cv[data-theme="legal"] .cv-name{font-size:34px; letter-spacing:.03em;}
.cv[data-theme="legal"] .cv-role{font-family:'Lora',serif; font-style:italic; color:var(--t-primary);}
.cv[data-theme="legal"] .cv-avatar{background:var(--t-primary); color:#F7F3EC; border-radius:0;}
.cv[data-theme="legal"] .cv-objective h2, .cv[data-theme="legal"] .cv-body h2{font-family:'Cormorant Garamond',serif; font-weight:700; font-size:15px; color:var(--t-primary); border-bottom:1px solid rgba(0,0,0,.15); padding-bottom:5px;}
.cv[data-theme="legal"] .skill-pill{background:none; color:var(--t-ink); border-bottom:1px solid var(--t-primary); border-radius:0; padding:2px 4px 2px 0; margin-right:10px;}
.cv[data-theme="legal"] .cv-contact{background:var(--t-panel);}

/* ============ THEME: EDUCATION ============ */
.cv[data-theme="education"]{ --t-primary:#6B7A4F; --t-secondary:#C1622D; --t-ink:#2E2A22; --t-ink-soft:#6b6355; --t-panel:#FBF6EC; --t-display:'Fraunces',serif; --t-body:'Nunito Sans',sans-serif; --t-mono:'Nunito Sans',sans-serif; }
.cv[data-theme="education"] .cv-header{background:var(--t-panel);}
.cv[data-theme="education"] .cv-avatar{background:var(--t-secondary); color:#fff;}
.cv[data-theme="education"] .cv-role{color:var(--t-secondary); font-weight:700;}
.cv[data-theme="education"] .cv-objective h2, .cv[data-theme="education"] .cv-body h2{color:var(--t-primary); position:relative;}
.cv[data-theme="education"] .skill-pill{background:#fff; border:1.5px solid var(--t-primary); color:var(--t-primary);}

/* ============ THEME: ENGINEERING ============ */
.cv[data-theme="engineering"]{ --t-primary:#3A3F44; --t-secondary:#FF6A13; --t-ink:#22262A; --t-ink-soft:#666; --t-panel:#EDF1F4; --t-display:'Oswald',sans-serif; --t-body:'IBM Plex Sans',sans-serif; --t-mono:'IBM Plex Mono',monospace; }
.cv[data-theme="engineering"] .cv-header{background:var(--t-primary); color:#fff;}
.cv[data-theme="engineering"] .cv-name{color:#fff; text-transform:uppercase; letter-spacing:.03em;}
.cv[data-theme="engineering"] .cv-role{color:var(--t-secondary); font-weight:600; text-transform:uppercase; font-size:11.5px; letter-spacing:.08em;}
.cv[data-theme="engineering"] .cv-avatar{background:var(--t-secondary); color:#22262A; border-radius:3px;}
.cv[data-theme="engineering"] .cv-objective h2, .cv[data-theme="engineering"] .cv-body h2{font-family:'Oswald',sans-serif; color:var(--t-primary); font-weight:600;}
.cv[data-theme="engineering"] .cv-objective h2::after, .cv[data-theme="engineering"] .cv-body h2::after{content:''; flex:1; height:1px; background:var(--t-secondary); margin-left:6px;}
.cv[data-theme="engineering"] .skill-pill{background:var(--t-panel); border-left:3px solid var(--t-secondary); border-radius:2px;}
.cv[data-theme="engineering"] .cv-contact{background:var(--t-panel);}

/* ============ THEME: MARKETING ============ */
.cv[data-theme="marketing"]{ --t-primary:#C6237D; --t-secondary:#FF7A1A; --t-ink:#231428; --t-ink-soft:#6b5f70; --t-panel:#FBEFF6; --t-display:'Sora',sans-serif; --t-body:'Inter',sans-serif; --t-mono:'Sora',sans-serif; }
.cv[data-theme="marketing"] .cv-header{background:linear-gradient(120deg,#2B0B3F,#6B1E93 55%,#C6237D); clip-path:polygon(0 0,100% 0,100% 100%,0 88%);}
.cv[data-theme="marketing"] .cv-name{color:#fff;}
.cv[data-theme="marketing"] .cv-role{color:var(--t-secondary); font-weight:600;}
.cv[data-theme="marketing"] .cv-avatar{background:var(--t-secondary); color:#231428;}
.cv[data-theme="marketing"] .cv-objective h2, .cv[data-theme="marketing"] .cv-body h2{color:var(--t-primary); font-weight:700;}
.cv[data-theme="marketing"] .skill-pill{background:linear-gradient(120deg,var(--t-primary),var(--t-secondary)); color:#fff; border:none;}

/* ============ FOOTER NOTE ============ */
.privacy-note{
  max-width:794px; width:100%;
  font-size:11.5px;
  color:var(--app-ink-soft);
  background:#fff;
  border:1px solid var(--app-line);
  border-radius:11px;
  padding:12px 16px;
  line-height:1.5;
  display:flex; gap:10px;
}
.privacy-note svg{flex-shrink:0; margin-top:2px;}

/* ============ RESPONSIVE ============ */
@media (max-width:980px){
  .app-layout{grid-template-columns:1fr;}
  .form-panel{position:static; height:auto; border-right:none; border-bottom:1px solid var(--app-line);}
  .cv{width:100%; min-height:auto;}
  .cv-sheet-wrap{max-width:100%;}
}

/* ============ PRINT ============ */
@media print{
  .app-topbar, .form-panel, .preview-toolbar, .privacy-note{display:none !important;}
  .app-layout{display:block;}
  .preview-panel{padding:0;}
  .cv-sheet-wrap{box-shadow:none; max-width:100%;}
  .cv{width:210mm; min-height:297mm;}
  body{background:#fff;}
  @page{ size:A4; margin:0; }
}
</style>
</head>
<body>

<div class="app-topbar">
  <div class="app-brand">
    <div class="app-brand-mark">CV</div>
    <div class="app-brand-text">
      <h1>Generador de CV Profesional</h1>
      <p>estilo &amp; objetivo adaptados a tu profesión</p>
    </div>
  </div>
  <div class="security-chip">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 2l8 4v6c0 5-3.5 8.5-8 10-4.5-1.5-8-5-8-10V6l8-4z"/><path d="M9 12l2 2 4-4"/></svg>
    100% local · sin servidor · tus datos no salen del navegador
  </div>
</div>

<div class="app-layout">
  <!-- ============ FORM PANEL ============ -->
  <aside class="form-panel">
    <form id="cvForm" autocomplete="off">

      <div class="form-step">
        <div class="form-step-label"><span class="num">1</span>Datos personales</div>
        <div class="field"><label for="f-name">Nombre completo</label><input type="text" id="f-name" maxlength="60" placeholder="Ej. Marielys Peña Rodríguez" value="Marielys Peña Rodríguez"></div>
        <div class="two-col">
          <div class="field"><label for="f-email">Correo</label><input type="email" id="f-email" maxlength="60" placeholder="correo@ejemplo.com" value="marielys.pena@email.com"></div>
          <div class="field"><label for="f-phone">Teléfono</label><input type="tel" id="f-phone" maxlength="30" placeholder="+1 809 000 0000" value="+1 809 555 0142"></div>
        </div>
        <div class="two-col">
          <div class="field"><label for="f-location">Ubicación</label><input type="text" id="f-location" maxlength="50" placeholder="Santo Domingo, RD" value="Santo Domingo, RD"></div>
          <div class="field"><label for="f-linkedin">LinkedIn / Portafolio</label><input type="text" id="f-linkedin" maxlength="60" placeholder="linkedin.com/in/usuario" value="linkedin.com/in/marielyspena"></div>
        </div>
      </div>

      <div class="form-step">
        <div class="form-step-label"><span class="num">2</span>Perfil profesional</div>
        <div class="field">
          <label for="f-category">Área / Profesión</label>
          <select id="f-category">
            <option value="tech">Tecnología y Desarrollo</option>
            <option value="design">Diseño y Creatividad</option>
            <option value="business">Negocios y Finanzas</option>
            <option value="health">Salud y Medicina</option>
            <option value="legal">Legal y Derecho</option>
            <option value="education">Educación</option>
            <option value="engineering">Ingeniería</option>
            <option value="marketing">Marketing y Ventas</option>
            <option value="general">General / Otro</option>
          </select>
        </div>
        <div class="two-col">
          <div class="field"><label for="f-role">Puesto que buscas</label><input type="text" id="f-role" maxlength="50" placeholder="Ej. Desarrolladora Frontend" value="Desarrolladora Frontend"></div>
          <div class="field"><label for="f-years">Años de experiencia</label><input type="text" id="f-years" maxlength="10" placeholder="Ej. 4" value="4"></div>
        </div>
        <div class="field"><label for="f-sector">Sector objetivo (opcional)</label><input type="text" id="f-sector" maxlength="50" placeholder="Ej. fintech, retail, salud..." value="fintech"></div>
        <div class="objective-row">
          <label for="f-objective" style="margin:0;">Objetivo profesional</label>
          <button type="button" class="btn-mini" id="btnGenObjective">✨ Generar según profesión</button>
        </div>
        <textarea id="f-objective" maxlength="500"></textarea>
        <p class="field-hint">Se sugiere automáticamente al cambiar la profesión. Puedes editarlo libremente.</p>
      </div>

      <div class="form-step">
        <div class="form-step-label"><span class="num">3</span>Experiencia laboral</div>
        <div id="expList"></div>
        <button type="button" class="btn-add" id="btnAddExp">+ Añadir experiencia</button>
      </div>

      <div class="form-step">
        <div class="form-step-label"><span class="num">4</span>Educación</div>
        <div id="eduList"></div>
        <button type="button" class="btn-add" id="btnAddEdu">+ Añadir estudio</button>
      </div>

      <div class="form-step">
        <div class="form-step-label"><span class="num">5</span>Habilidades e idiomas</div>
        <div class="field"><label for="f-skills">Habilidades (separadas por coma)</label><textarea id="f-skills" maxlength="300">HTML &amp; CSS, JavaScript, React, Diseño de interfaces, Trabajo en equipo</textarea></div>
        <div class="field"><label for="f-languages">Idiomas — formato: Idioma:Nivel, uno por línea</label><textarea id="f-languages" maxlength="200">Español:Nativo
Inglés:Avanzado</textarea></div>
        <div class="field"><label for="f-certs">Certificaciones — formato: Título:Institución, una por línea</label><textarea id="f-certs" maxlength="300">Certificación en Desarrollo Web:Plataforma XYZ</textarea></div>
      </div>

      <button type="button" class="btn-primary" id="btnPrint">
        <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M6 9V2h12v7"/><path d="M6 18H4a2 2 0 01-2-2v-5a2 2 0 012-2h16a2 2 0 012 2v5a2 2 0 01-2 2h-2"/><path d="M6 14h12v8H6z"/></svg>
        Descargar CV en PDF
      </button>
    </form>
  </aside>

  <!-- ============ PREVIEW PANEL ============ -->
  <section class="preview-panel">
    <div class="preview-toolbar">
      <div class="theme-tag"><span class="theme-swatch" id="themeSwatch"></span><span id="themeLabel">Tecnología y Desarrollo</span></div>
    </div>

    <div class="cv-sheet-wrap">
      <div class="cv" id="cvSheet" data-theme="tech">
        <header class="cv-header">
          <div class="cv-avatar" id="cvAvatar">MP</div>
          <div class="cv-heading">
            <h1 class="cv-name" id="cvName">Marielys Peña Rodríguez</h1>
            <p class="cv-role" id="cvRole">Desarrolladora Frontend</p>
          </div>
        </header>
        <div class="cv-contact" id="cvContact"></div>
        <section class="cv-objective">
          <h2>Objetivo Profesional</h2>
          <p id="cvObjective"></p>
        </section>
        <div class="cv-body">
          <main class="cv-main">
            <section class="cv-experience">
              <h2>Experiencia</h2>
              <div id="cvExperience"></div>
            </section>
            <section class="cv-education">
              <h2>Educación</h2>
              <div id="cvEducation"></div>
            </section>
          </main>
          <aside class="cv-sidebar">
            <section class="cv-skills"><h2>Habilidades</h2><div id="cvSkills"></div></section>
            <section class="cv-languages"><h2>Idiomas</h2><div id="cvLanguages"></div></section>
            <section class="cv-certs"><h2>Certificaciones</h2><div id="cvCerts"></div></section>
          </aside>
        </div>
      </div>
    </div>

    <div class="privacy-note">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#1C7C4E" stroke-width="2"><path d="M12 2l8 4v6c0 5-3.5 8.5-8 10-4.5-1.5-8-5-8-10V6l8-4z"/></svg>
      <div>Esta página funciona enteramente en tu navegador: no envía datos a ningún servidor, no usa cookies ni almacenamiento persistente, y no realiza conexiones externas (salvo cargar las tipografías). Al cerrar o recargar la pestaña, la información desaparece. Eso significa que no existe una base de datos remota que pueda ser vulnerada — la superficie de ataque típica de "hackeo" simplemente no aplica aquí.</div>
    </div>
  </section>
</div>

<script>
(function(){
  'use strict';

  /* ---------- Seguridad: escape estricto de todo texto insertado en el DOM ---------- */
  function esc(str){
    return String(str == null ? '' : str).replace(/[&<>"'`=\/]/g, function(c){
      return ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;','`':'&#96;','=':'&#61;','/':'&#47;'})[c];
    });
  }
  function escMultiline(str){ return esc(str).replace(/\n/g,'<br>'); }

  /* ---------- Definición de temas ---------- */
  var THEMES = {
    tech:        { label:'Tecnología y Desarrollo', swatch:'#4F7CFF' },
    design:      { label:'Diseño y Creatividad',     swatch:'#FF3D6E' },
    business:    { label:'Negocios y Finanzas',       swatch:'#0F1E3D' },
    health:      { label:'Salud y Medicina',          swatch:'#0E7C7B' },
    legal:       { label:'Legal y Derecho',           swatch:'#6B1E2B' },
    education:   { label:'Educación',                 swatch:'#6B7A4F' },
    engineering: { label:'Ingeniería',                swatch:'#3A3F44' },
    marketing:   { label:'Marketing y Ventas',        swatch:'#C6237D' },
    general:     { label:'General / Otro',            swatch:'#2451B7' }
  };

  /* ---------- Generador de objetivo por profesión ---------- */
  function buildObjective(cat, data){
    var role = data.role || 'profesional del área';
    var years = data.years ? (data.years + ' años de ') : '';
    var top = data.skillsTop.length ? data.skillsTop.join(', ') : 'las herramientas propias del sector';
    var sector = data.sector ? (' en el sector ' + data.sector) : '';

    var T = {
      tech: 'Profesional con ' + years + 'experiencia en ' + top + ', enfocado/a en construir productos digitales escalables y de alta calidad' + sector + '. Busco incorporarme como ' + role + ' en un equipo que valore el código limpio, la mejora continua y la colaboración técnica.',
      design: 'Creativo/a con ' + years + 'trayectoria en ' + top + ', apasionado/a por diseñar experiencias visuales memorables' + sector + '. Aspiro a desempeñarme como ' + role + ' aportando una mirada estética sólida, atención al detalle y sentido de marca.',
      business: 'Profesional orientado/a a resultados, con ' + years + 'experiencia en ' + top + sector + '. Busco la posición de ' + role + ' para impulsar el crecimiento, la eficiencia operativa y la toma de decisiones estratégicas basada en datos.',
      health: 'Profesional de la salud con ' + years + 'experiencia en ' + top + ', comprometido/a con la atención centrada en el paciente' + sector + '. Busco desempeñarme como ' + role + ', aportando rigor clínico, empatía y actualización constante.',
      legal: 'Profesional del derecho con ' + years + 'experiencia en ' + top + sector + '. Aspiro a la posición de ' + role + ', aportando análisis riguroso, ética profesional y capacidad de argumentación en la defensa de los intereses representados.',
      education: 'Educador/a con ' + years + 'experiencia en ' + top + ', comprometido/a con el aprendizaje significativo' + sector + '. Busco integrarme como ' + role + ' para acompañar procesos formativos con creatividad, paciencia y vocación de servicio.',
      engineering: 'Ingeniero/a con ' + years + 'experiencia en ' + top + ', enfocado/a en soluciones técnicas seguras y eficientes' + sector + '. Busco la posición de ' + role + ' para aportar precisión, resolución de problemas y cumplimiento de estándares técnicos.',
      marketing: 'Profesional de marketing con ' + years + 'experiencia en ' + top + ', orientado/a a construir marcas relevantes y campañas de alto impacto' + sector + '. Busco desempeñarme como ' + role + ' aportando creatividad, pensamiento analítico y foco en resultados medibles.',
      general: 'Profesional con ' + years + 'experiencia en ' + top + sector + '. Busco desarrollarme como ' + role + ', aportando compromiso, capacidad de aprendizaje y disposición para trabajar en equipo.'
    };
    return T[cat] || T.general;
  }

  /* ---------- Estado de listas dinámicas ---------- */
  var expCount = 0, eduCount = 0;

  function addExpRow(prefill){
    expCount++;
    var id = 'exp' + expCount;
    var wrap = document.createElement('div');
    wrap.className = 'entry-card';
    wrap.dataset.id = id;
    wrap.innerHTML =
      '<button type="button" class="entry-remove" data-remove="' + id + '">eliminar</button>' +
      '<div class="field"><label>Puesto</label><input type="text" maxlength="60" class="exp-title-in" placeholder="Ej. Desarrolladora Frontend"></div>' +
      '<div class="field"><label>Empresa</label><input type="text" maxlength="60" class="exp-company-in" placeholder="Ej. Empresa S.R.L."></div>' +
      '<div class="two-col">' +
        '<div class="field"><label>Desde</label><input type="text" maxlength="20" class="exp-from-in" placeholder="Ene 2022"></div>' +
        '<div class="field"><label>Hasta</label><input type="text" maxlength="20" class="exp-to-in" placeholder="Presente"></div>' +
      '</div>' +
      '<div class="field"><label>Descripción</label><textarea maxlength="260" class="exp-desc-in" placeholder="Logros y responsabilidades principales..."></textarea></div>';
    document.getElementById('expList').appendChild(wrap);
    if(prefill){
      wrap.querySelector('.exp-title-in').value = prefill.title;
      wrap.querySelector('.exp-company-in').value = prefill.company;
      wrap.querySelector('.exp-from-in').value = prefill.from;
      wrap.querySelector('.exp-to-in').value = prefill.to;
      wrap.querySelector('.exp-desc-in').value = prefill.desc;
    }
  }

  function addEduRow(prefill){
    eduCount++;
    var id = 'edu' + eduCount;
    var wrap = document.createElement('div');
    wrap.className = 'entry-card';
    wrap.dataset.id = id;
    wrap.innerHTML =
      '<button type="button" class="entry-remove" data-remove="' + id + '">eliminar</button>' +
      '<div class="field"><label>Título / Programa</label><input type="text" maxlength="60" class="edu-degree-in" placeholder="Ej. Ingeniería en Sistemas"></div>' +
      '<div class="field"><label>Institución</label><input type="text" maxlength="60" class="edu-school-in" placeholder="Ej. Universidad XYZ"></div>' +
      '<div class="two-col">' +
        '<div class="field"><label>Desde</label><input type="text" maxlength="20" class="edu-from-in" placeholder="2018"></div>' +
        '<div class="field"><label>Hasta</label><input type="text" maxlength="20" class="edu-to-in" placeholder="2022"></div>' +
      '</div>';
    document.getElementById('eduList').appendChild(wrap);
    if(prefill){
      wrap.querySelector('.edu-degree-in').value = prefill.degree;
      wrap.querySelector('.edu-school-in').value = prefill.school;
      wrap.querySelector('.edu-from-in').value = prefill.from;
      wrap.querySelector('.edu-to-in').value = prefill.to;
    }
  }

  document.getElementById('expList').addEventListener('input', renderCV);
  document.getElementById('eduList').addEventListener('input', renderCV);
  document.getElementById('expList').addEventListener('click', function(e){
    var btn = e.target.closest('[data-remove]');
    if(!btn) return;
    var row = btn.closest('.entry-card');
    if(row) row.remove();
    renderCV();
  });
  document.getElementById('eduList').addEventListener('click', function(e){
    var btn = e.target.closest('[data-remove]');
    if(!btn) return;
    var row = btn.closest('.entry-card');
    if(row) row.remove();
    renderCV();
  });
  document.getElementById('btnAddExp').addEventListener('click', function(){ addExpRow(); renderCV(); });
  document.getElementById('btnAddEdu').addEventListener('click', function(){ addEduRow(); renderCV(); });

  /* ---------- Prefill inicial de ejemplo ---------- */
  addExpRow({title:'Desarrolladora Frontend', company:'Estudio Digital RD', from:'Ene 2023', to:'Presente', desc:'Construcción de interfaces con React, mejora de rendimiento en un 30% y coordinación con diseño para nuevas funciones.'});
  addExpRow({title:'Desarrolladora Junior', company:'Innovatech', from:'Jun 2021', to:'Dic 2022', desc:'Mantenimiento de aplicaciones web y soporte en la migración de sistemas legados.'});
  addEduRow({degree:'Ingeniería en Sistemas', school:'Universidad Autónoma', from:'2017', to:'2021'});

  /* ---------- Utilidades de parsing ---------- */
  function parseSkills(raw){
    return raw.split(',').map(function(s){return s.trim();}).filter(Boolean);
  }
  function parseLines(raw){
    return raw.split('\n').map(function(s){return s.trim();}).filter(Boolean);
  }
  function initials(name){
    var parts = name.trim().split(/\s+/).filter(Boolean);
    if(!parts.length) return '—';
    if(parts.length === 1) return parts[0].slice(0,2).toUpperCase();
    return (parts[0][0] + parts[1][0]).toUpperCase();
  }

  var objectiveManuallyEdited = false;
  document.getElementById('f-objective').addEventListener('input', function(){
    objectiveManuallyEdited = true;
  });
  document.getElementById('btnGenObjective').addEventListener('click', function(){
    objectiveManuallyEdited = false;
    suggestObjective();
    renderCV();
  });

  function suggestObjective(){
    var cat = document.getElementById('f-category').value;
    var role = document.getElementById('f-role').value.trim();
    var years = document.getElementById('f-years').value.trim();
    var sector = document.getElementById('f-sector').value.trim();
    var skills = parseSkills(document.getElementById('f-skills').value);
    var text = buildObjective(cat, {role:role, years:years, sector:sector, skillsTop:skills.slice(0,3)});
    document.getElementById('f-objective').value = text;
  }

  /* ---------- Render principal ---------- */
  function renderCV(){
    var cat = document.getElementById('f-category').value;
    var theme = THEMES[cat] || THEMES.general;

    var name = document.getElementById('f-name').value.trim() || 'Tu nombre';
    var role = document.getElementById('f-role').value.trim() || 'Puesto deseado';
    var email = document.getElementById('f-email').value.trim();
    var phone = document.getElementById('f-phone').value.trim();
    var location = document.getElementById('f-location').value.trim();
    var linkedin = document.getElementById('f-linkedin').value.trim();

    if(!objectiveManuallyEdited || !document.getElementById('f-objective').value.trim()){
      suggestObjective();
    }
    var objective = document.getElementById('f-objective').value.trim();

    document.getElementById('cvSheet').setAttribute('data-theme', cat);
    document.getElementById('themeSwatch').style.background = theme.swatch;
    document.getElementById('themeLabel').textContent = theme.label;

    document.getElementById('cvAvatar').textContent = initials(name);
    document.getElementById('cvName').innerHTML = esc(name);
    document.getElementById('cvRole').innerHTML = esc(role);
    document.getElementById('cvObjective').innerHTML = escMultiline(objective);

    var contactBits = [];
    if(email) contactBits.push('<span>✉ ' + esc(email) + '</span>');
    if(phone) contactBits.push('<span>☎ ' + esc(phone) + '</span>');
    if(location) contactBits.push('<span>📍 ' + esc(location) + '</span>');
    if(linkedin) contactBits.push('<span>🔗 ' + esc(linkedin) + '</span>');
    document.getElementById('cvContact').innerHTML = contactBits.join('');

    /* Experiencia */
    var expHtml = '';
    document.querySelectorAll('#expList .entry-card').forEach(function(row){
      var title = row.querySelector('.exp-title-in').value.trim();
      var company = row.querySelector('.exp-company-in').value.trim();
      var from = row.querySelector('.exp-from-in').value.trim();
      var to = row.querySelector('.exp-to-in').value.trim();
      var desc = row.querySelector('.exp-desc-in').value.trim();
      if(!title && !company) return;
      expHtml += '<div class="exp-item">' +
        '<div class="exp-item-top"><span class="exp-title">' + esc(title) + '</span><span class="exp-dates">' + esc(from) + (from||to?' – ':'') + esc(to) + '</span></div>' +
        (company ? '<div class="exp-company">' + esc(company) + '</div>' : '') +
        (desc ? '<p class="exp-desc">' + escMultiline(desc) + '</p>' : '') +
      '</div>';
    });
    document.getElementById('cvExperience').innerHTML = expHtml || '<p class="empty-note">Añade tu experiencia laboral en el panel izquierdo.</p>';

    /* Educación */
    var eduHtml = '';
    document.querySelectorAll('#eduList .entry-card').forEach(function(row){
      var degree = row.querySelector('.edu-degree-in').value.trim();
      var school = row.querySelector('.edu-school-in').value.trim();
      var from = row.querySelector('.edu-from-in').value.trim();
      var to = row.querySelector('.edu-to-in').value.trim();
      if(!degree && !school) return;
      eduHtml += '<div class="edu-item">' +
        '<div class="exp-item-top"><span class="edu-degree">' + esc(degree) + '</span><span class="edu-dates">' + esc(from) + (from||to?' – ':'') + esc(to) + '</span></div>' +
        (school ? '<div class="edu-school">' + esc(school) + '</div>' : '') +
      '</div>';
    });
    document.getElementById('cvEducation').innerHTML = eduHtml || '<p class="empty-note">Añade tu formación académica.</p>';

    /* Habilidades */
    var skills = parseSkills(document.getElementById('f-skills').value);
    document.getElementById('cvSkills').innerHTML = skills.length
      ? skills.map(function(s){ return '<span class="skill-pill">' + esc(s) + '</span>'; }).join('')
      : '<p class="empty-note">Añade tus habilidades.</p>';

    /* Idiomas */
    var langs = parseLines(document.getElementById('f-languages').value);
    document.getElementById('cvLanguages').innerHTML = langs.length
      ? langs.map(function(l){
          var parts = l.split(':');
          var name = parts[0] ? parts[0].trim() : l;
          var level = parts[1] ? parts[1].trim() : '';
          return '<div class="lang-item"><span>' + esc(name) + '</span><span>' + esc(level) + '</span></div>';
        }).join('')
      : '<p class="empty-note">Añade idiomas.</p>';

    /* Certificaciones */
    var certs = parseLines(document.getElementById('f-certs').value);
    document.getElementById('cvCerts').innerHTML = certs.length
      ? certs.map(function(c){
          var parts = c.split(':');
          var title = parts[0] ? parts[0].trim() : c;
          var inst = parts[1] ? parts[1].trim() : '';
          return '<div class="cert-item"><b>' + esc(title) + '</b>' + (inst ? esc(inst) : '') + '</div>';
        }).join('')
      : '<p class="empty-note">Añade certificaciones (opcional).</p>';
  }

  /* ---------- Listeners globales ---------- */
  document.getElementById('cvForm').addEventListener('input', renderCV);
  document.getElementById('f-category').addEventListener('change', function(){
    if(!objectiveManuallyEdited) suggestObjective();
    renderCV();
  });
  document.getElementById('btnPrint').addEventListener('click', function(){
    window.print();
  });

  /* ---------- Render inicial ---------- */
  suggestObjective();
  renderCV();
})();
</script>
</body>
</html>
