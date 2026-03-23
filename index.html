<index.html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="theme-color" content="#0a0a0a">
<title>StockAudit V</title>
<!-- 
  FIREBASE HOSTING STEPS:
  1. npm install -g firebase-tools
  2. firebase login
  3. firebase init hosting (select your project, public dir = ".", single page app = yes)
  4. firebase deploy
  Your app will be live at: https://YOUR_PROJECT.web.app
-->
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
<style>
:root{
  --pri:#2d1b69;--pri2:#5b2d8e;--acc:#00b4d8;
  --bg:#f0eaff;--card:#fff;--border:#d4c5f9;
  --text:#1a0533;--muted:#7c6fa0;--thead:#ede7ff;
  --ok:#0f6e56;--ok-bg:#e1f5ee;--warn:#854f0b;--warn-bg:#faeeda;
  --danger:#c0392b;--danger-bg:#fcebeb;
}
*{box-sizing:border-box;margin:0;padding:0;}
body{font-family:'Segoe UI',system-ui,sans-serif;background:var(--bg);color:var(--text);font-size:14px;}

/* ── LOGIN ── */
.login-wrap{min-height:100vh;display:flex;align-items:center;justify-content:center;background:#0a0a0a;}
.login-card{background:#1a1a2e;border:1px solid rgba(255,255,255,.1);border-radius:16px;padding:2rem 1.8rem;width:360px;max-width:95vw;}
.login-logo{text-align:center;margin-bottom:1.4rem;}
.login-logo h1{font-size:22px;font-weight:700;color:var(--acc);}
.login-logo p{font-size:12px;color:rgba(255,255,255,.4);margin-top:3px;}
.tab-row{display:flex;border:1px solid rgba(255,255,255,.1);border-radius:8px;overflow:hidden;margin-bottom:1.2rem;}
.tab-btn{flex:1;padding:9px;font-size:13px;font-weight:600;background:rgba(255,255,255,.05);color:rgba(255,255,255,.4);border:none;cursor:pointer;transition:all .2s;}
.tab-btn.active{background:var(--acc);color:#fff;}
.fg{margin-bottom:.9rem;}
.fg label{display:block;font-size:11px;font-weight:600;color:rgba(255,255,255,.4);text-transform:uppercase;letter-spacing:.5px;margin-bottom:5px;}
.fg input,.fg select{width:100%;padding:10px 12px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.12);border-radius:8px;font-size:14px;color:#fff;outline:none;font-family:inherit;}
.fg input::placeholder{color:rgba(255,255,255,.25);}
.fg input:focus{border-color:var(--acc);}
.btn-login{width:100%;padding:11px;background:linear-gradient(135deg,var(--pri),var(--acc));color:#fff;border:none;border-radius:8px;font-size:15px;font-weight:600;cursor:pointer;margin-top:.3rem;}
.login-err{color:#ff6b6b;font-size:12px;text-align:center;margin-top:.5rem;min-height:16px;}


/* OTP boxes */
.otp-row{display:flex;gap:6px;justify-content:center;margin:8px 0;}
.otp-row input{width:42px;height:48px;text-align:center;font-size:22px;font-weight:700;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.15);border-radius:8px;color:#fff;outline:none;}
.otp-row input:focus{border-color:var(--acc);}

/* ── APP LAYOUT ── */
.app{display:none;min-height:100vh;flex-direction:row;}
.sidebar{width:220px;background:linear-gradient(180deg,var(--pri) 0%,#1a0533 100%);color:#fff;display:flex;flex-direction:column;position:fixed;top:0;left:0;height:100vh;z-index:100;transition:transform .3s;}
.sb-logo{padding:1rem 1rem .7rem;border-bottom:1px solid rgba(255,255,255,.1);}
.sb-logo h2{font-size:15px;font-weight:700;}
.sb-logo span{font-size:11px;opacity:.5;}
.sb-nav{flex:1;padding:.6rem 0;overflow-y:auto;}
.nav-item{display:flex;align-items:center;gap:9px;padding:9px 1rem;cursor:pointer;font-size:13px;border-left:3px solid transparent;transition:background .15s;}
.nav-item:hover{background:rgba(255,255,255,.07);}
.nav-item.active{background:rgba(255,255,255,.13);border-left-color:var(--acc);font-weight:600;}
.sb-foot{padding:.8rem 1rem;border-top:1px solid rgba(255,255,255,.1);font-size:12px;opacity:.6;}
.main{margin-left:220px;min-height:100vh;display:flex;flex-direction:column;}
.topbar{background:var(--card);border-bottom:1px solid var(--border);padding:.8rem 1.2rem;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:50;gap:8px;}
.topbar h3{font-size:17px;font-weight:700;color:var(--pri);}
.user-info{display:flex;align-items:center;gap:8px;font-size:12px;color:var(--muted);}
.avatar{width:30px;height:30px;background:var(--acc);border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:13px;color:#fff;}
.logout-btn{background:none;border:1px solid var(--border);color:var(--muted);padding:4px 10px;border-radius:6px;cursor:pointer;font-size:12px;}
.content{padding:1.2rem;flex:1;}

/* MOB TOGGLE */
.mob-btn{display:none;background:none;border:none;font-size:22px;cursor:pointer;color:var(--pri);padding:2px 6px;}
.mob-overlay{display:none;position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:99;}
@media(max-width:768px){
  .mob-btn{display:block;}
  .sidebar{transform:translateX(-100%);}
  .sidebar.open{transform:translateX(0);}
  .mob-overlay.show{display:block;}
  .main{margin-left:0;}
  .content{padding:.8rem;}
  .stat-row{grid-template-columns:1fr 1fr!important;}
}

/* ── COMPONENTS ── */
.stat-row{display:grid;grid-template-columns:repeat(auto-fit,minmax(140px,1fr));gap:10px;margin-bottom:1.2rem;}
.stat-card{background:var(--card);border:1px solid var(--border);border-radius:10px;padding:.9rem 1rem;}
.stat-card .lbl{font-size:11px;color:var(--muted);font-weight:600;text-transform:uppercase;letter-spacing:.4px;}
.stat-card .val{font-size:24px;font-weight:700;color:var(--pri);margin-top:3px;}

.card{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;margin-bottom:1rem;}
.card-hdr{padding:.8rem 1rem;display:flex;align-items:center;justify-content:space-between;border-bottom:1px solid var(--border);flex-wrap:wrap;gap:8px;}
.card-hdr b{font-size:13px;color:var(--pri);}
.tbl-wrap{overflow-x:auto;}
table{width:100%;border-collapse:collapse;font-size:12px;}
thead{background:var(--thead);}
th{padding:8px 10px;text-align:left;font-weight:600;color:var(--pri);font-size:11px;text-transform:uppercase;white-space:nowrap;}
td{padding:8px 10px;border-bottom:1px solid #f0f2f7;white-space:nowrap;}
tr:last-child td{border-bottom:none;}
tr:hover td{background:#f8f6ff;}

.badge{display:inline-block;padding:2px 8px;border-radius:20px;font-size:10px;font-weight:600;}
.b-ok{background:var(--ok-bg);color:var(--ok);}
.b-warn{background:var(--warn-bg);color:var(--warn);}
.b-pend{background:#f1efe8;color:#5f5e5a;}
.b-info{background:#e6f1fb;color:#0C447C;}

.btn{padding:6px 14px;border:none;border-radius:7px;font-size:12px;font-weight:600;cursor:pointer;white-space:nowrap;}
.btn-pri{background:var(--pri);color:#fff;}
.btn-acc{background:var(--acc);color:#fff;}
.btn-ok{background:#1d6e3e;color:#fff;}
.btn-warn{background:var(--warn);color:#fff;}
.btn-sub{background:var(--ok);color:#fff;}
.btn-ghost{background:var(--bg);border:1px solid var(--border);color:var(--text);}
.btn-sm{padding:3px 8px;font-size:11px;}
.fr{display:flex;gap:8px;align-items:center;flex-wrap:wrap;}

/* ACCORDION */
.acc{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;margin-bottom:.5rem;}
.acc-hdr{padding:.8rem 1rem;display:flex;align-items:center;justify-content:space-between;cursor:pointer;user-select:none;}
.acc-hdr:hover{background:#f8f6ff;}
.acc-hdr.open{border-bottom:1px solid var(--border);}
.acc-body{display:none;padding:.7rem;}
.acc-body.open{display:block;}
.arr{font-size:11px;color:var(--pri);display:inline-block;transition:transform .25s;margin-right:6px;}
.arr.open{transform:rotate(90deg);}

/* EXCEL VIEW */
.ex-wrap{background:var(--card);border:1px solid var(--border);border-radius:10px;overflow:hidden;}
.ex-hdr{background:#217346;padding:.5rem .8rem;display:flex;align-items:center;gap:8px;flex-wrap:wrap;}
.ex-hdr span{color:#fff;font-size:13px;font-weight:600;}
.ex-tbl{width:100%;border-collapse:collapse;font-size:12px;}
.ex-tbl th{background:#d8e4bc;color:#1f4e79;padding:5px 8px;border:1px solid #b8c9a3;text-align:center;font-size:10px;font-weight:700;text-transform:uppercase;white-space:nowrap;}
.ex-tbl td{padding:4px 8px;border:1px solid #dde;background:#fff;white-space:nowrap;}
.ex-tbl tr:nth-child(even) td{background:#f7faff;}
.editable{background:#fffde7!important;cursor:text;}
.editable:focus{background:#fff9c4!important;outline:2px solid #217346;}

/* SBOX */
.sbox{display:flex;align-items:center;gap:6px;border:1px solid var(--border);border-radius:7px;padding:5px 10px;background:var(--bg);}
.sbox input{border:none;outline:none;background:transparent;font-size:12px;width:160px;}

/* MODAL */
.modal-ov{position:fixed;inset:0;background:rgba(0,0,0,.5);z-index:200;display:flex;align-items:center;justify-content:center;padding:1rem;}
.modal{background:var(--card);border-radius:12px;width:460px;max-width:100%;max-height:90vh;overflow-y:auto;}
.m-hdr{padding:1rem 1.2rem;border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;}
.m-hdr h3{font-size:15px;font-weight:700;color:var(--pri);}
.m-body{padding:1rem 1.2rem;}
.m-foot{padding:.8rem 1.2rem;border-top:1px solid var(--border);display:flex;justify-content:flex-end;gap:8px;}
.mfg{margin-bottom:.8rem;}
.mfg label{display:block;font-size:11px;font-weight:600;color:var(--muted);text-transform:uppercase;letter-spacing:.4px;margin-bottom:4px;}
.mfg input,.mfg select,.mfg textarea{width:100%;padding:8px 10px;border:1px solid var(--border);border-radius:7px;font-size:13px;outline:none;font-family:inherit;}
.mfg input:focus,.mfg select:focus{border-color:var(--acc);}
.hidden{display:none!important;}
.upzone{border:2px dashed var(--border);border-radius:10px;padding:1.5rem;text-align:center;background:var(--bg);cursor:pointer;}
.upzone:hover{border-color:var(--acc);}
.col-chips{display:flex;flex-wrap:wrap;gap:4px;padding:.5rem 0;}
.col-chip{padding:3px 8px;background:var(--thead);color:var(--pri);border-radius:4px;font-size:10px;font-weight:600;border:1px solid var(--border);cursor:default;white-space:nowrap;}
</style>
</head>
<body>

<!-- ═══════════ LOGIN ═══════════ -->
<div class="login-wrap" id="loginWrap">
  <div class="login-card">
    <div class="login-logo">
      <h1>StockAudit V</h1>
      <p>Inventory Auditing System</p>
    </div>
    <div class="tab-row">
      <button class="tab-btn active" onclick="switchRole('auditor')">Auditor Login</button>
      <button class="tab-btn" onclick="switchRole('master')">Master Login</button>
    </div>

    <!-- Master Fields -->
    <div id="masterSec">
      <div class="fg"><label>Username</label><input id="mUser" placeholder="Master username" onkeydown="if(event.key==='Enter')doLogin()"></div>
      <div class="fg"><label>Password</label><input type="password" id="mPass" placeholder="Master password" onkeydown="if(event.key==='Enter')doLogin()"></div>
      <button class="btn-login" onclick="doLogin()">Login as Master</button>
    </div>

    <!-- Auditor Fields -->
    <div id="auditorSec" class="hidden">
      <div id="aStep1">
        <div class="fg"><label>Phone Number</label><input type="tel" id="aPhone" placeholder="Registered phone number" onkeydown="if(event.key==='Enter')sendOTP()"></div>
        <div class="fg"><label>OR Username</label><input id="aUser" placeholder="auditor01" onkeydown="if(event.key==='Enter')doAuditorUsernameLogin()"></div>
        <div class="fg"><label>Password (for username login)</label><input type="password" id="aPass" placeholder="Audit@01" onkeydown="if(event.key==='Enter')doAuditorUsernameLogin()"></div>
        <div class="fr">
          <button class="btn-login" style="flex:1" onclick="sendOTP()">Send OTP</button>
          <button class="btn-login" style="flex:1;background:linear-gradient(135deg,#2d1b69,#5b2d8e)" onclick="doAuditorUsernameLogin()">Login with Username</button>
        </div>
      </div>
      <div id="aStep2" class="hidden"><p style="font-size:12px;color:rgba(255,255,255,.5);text-align:center;margin-bottom:.5rem">OTP sent to <span id="otpPhoneDisp" style="color:var(--acc)"></span></p>
        <div class="fg"><label>OTP sent to your phone</label>
          <div class="otp-row">
            <input type="text" id="o1" maxlength="1" oninput="otpNext(this,'o2')" onkeydown="otpBack(event,this,null)">
            <input type="text" id="o2" maxlength="1" oninput="otpNext(this,'o3')" onkeydown="otpBack(event,this,'o1')">
            <input type="text" id="o3" maxlength="1" oninput="otpNext(this,'o4')" onkeydown="otpBack(event,this,'o2')">
            <input type="text" id="o4" maxlength="1" oninput="otpNext(this,'o5')" onkeydown="otpBack(event,this,'o3')">
            <input type="text" id="o5" maxlength="1" oninput="otpNext(this,'o6')" onkeydown="otpBack(event,this,'o4')">
            <input type="text" id="o6" maxlength="1" oninput="autoVerify()" onkeydown="otpBack(event,this,'o5')">
          </div>
        </div>
        <button class="btn-login" onclick="verifyOTP()">Verify OTP</button>
        <p style="text-align:center;font-size:11px;color:rgba(255,255,255,.4);margin-top:.5rem;cursor:pointer" onclick="backToPhone()">← Change number</p>
      </div>
    </div>

    <div class="login-err" id="loginErr"></div>

  </div>
</div>

<!-- ═══════════ APP ═══════════ -->
<div class="app" id="appWrap">
  <div class="mob-overlay" id="mobOv" onclick="toggleSidebar()"></div>
  <div class="sidebar" id="sidebar">
    <div class="sb-logo"><h2>StockAudit V</h2><span id="roleLabel">Panel</span></div>
    <div class="sb-nav" id="sbNav"></div>
    <div class="sb-foot" id="sbFoot"></div>
  </div>
  <div class="main">
    <div class="topbar">
      <div class="fr" style="gap:6px">
        <button class="mob-btn" onclick="toggleSidebar()">&#9776;</button>
        <h3 id="pageTitle">Dashboard</h3>
        <span id="fbBadge" style="font-size:10px;padding:2px 8px;border-radius:20px;background:var(--bg);border:1px solid var(--border);color:var(--muted)">&#9679; Local</span>
      </div>
      <div class="user-info">
        <div class="avatar" id="avIcon">A</div>
        <span id="uName"></span>
        <button class="logout-btn" onclick="doLogout()">Logout</button>
      </div>
    </div>
    <div class="content" id="mainContent"></div>
  </div>
</div>

<!-- MODAL -->
<div class="modal-ov hidden" id="modalOv">
  <div class="modal">
    <div class="m-hdr"><h3 id="mTitle">-</h3><button style="background:none;border:none;font-size:18px;cursor:pointer;color:var(--muted)" onclick="closeModal()">✕</button></div>
    <div class="m-body" id="mBody"></div>
    <div class="m-foot" id="mFoot"></div>
  </div>
</div>
<script>
// ═══════════ DATA ═══════════
// ═══════════ FIREBASE CONFIG ═══════════
// Replace with your real Firebase config from console.firebase.google.com
// ══════════════════════════════════════════════════════
// PASTE YOUR FIREBASE CONFIG HERE
// Get it from: console.firebase.google.com
// Project Settings > Your apps > Web app > Config
// ══════════════════════════════════════════════════════
var FB_CONFIG = {
  apiKey: "AIzaSyDkDhtwbtxPMf7q-gFcDpLJQ322AWzSUCo",
  authDomain: "stockaudit-v.firebaseapp.com",
  databaseURL: "https://stockaudit-v-default-rtdb.asia-southeast1.firebasedatabase.app",
  projectId: "stockaudit-v",
  storageBucket: "stockaudit-v.firebasestorage.app",
  messagingSenderId: "901847490955",
  appId: "1:901847490955:web:a01bd888e01c4d6c0e0f8e"
};

var FB_READY = false;
var db = null;
var fbAuth = null;
var recaptchaVerifier = null;
var confirmationResult = null;

function initFirebase(){
  try {
    if(typeof firebase === 'undefined') { console.warn('Firebase not loaded'); return; }
    if(FB_CONFIG.apiKey === 'YOUR_API_KEY') {
      console.log('Firebase not configured — paste your config to enable. Using local mode.');
      return;
    }
    firebase.initializeApp(FB_CONFIG);
    db = firebase.database();
    fbAuth = firebase.auth();
    FB_READY = true;
    console.log('Firebase ready');
    var badge = document.getElementById('fbBadge');
    if(badge) badge.innerHTML = '<span style="color:var(--ok)">&#9679;</span> Firebase Live';
    // Save default master credentials to Firebase if not exist
    db.ref('master_credentials').once('value').then(function(snap){
      if(!snap.val()){
        db.ref('master_credentials').set({username:MASTER.u, password:MASTER.p});
      }
    });
    // Real-time listeners for each data path
    db.ref('stock').on('value', function(snap){
      var data = snap.val();
      if(!CU) return;
      if(data) STOCK = Object.values(data).filter(function(s){return s&&s.id;});
      else STOCK = [];
      if(PAGE) go(PAGE);
    });
    db.ref('menus').on('value', function(snap){
      var data = snap.val();
      if(!CU) return;
      if(data){
        MENUS = Object.values(data).filter(function(m){return m&&m.id;});
        MENUS.forEach(function(m){if(!Array.isArray(m.subs))m.subs=[];});
      }
      if(PAGE) go(PAGE);
    });
    db.ref('auditors').on('value', function(snap){
      var data = snap.val();
      if(!CU) return;
      if(data) AUDITORS = Object.values(data).filter(function(a){return a&&a.id;});
      if(PAGE) go(PAGE);
    });
    db.ref('meta').on('value', function(snap){
      var data = snap.val();
      if(!data) return;
      if(data.nextSID) nextSID = parseInt(data.nextSID)||1;
      if(data.nextMID) nextMID = parseInt(data.nextMID)||8;
      if(data.locked) LOCKED_COLS = data.locked;
    });
  } catch(e) {
    console.warn('Firebase init error:', e);
  }
}

function setupRecaptcha(){
  if(!FB_READY || !fbAuth) return;
  try {
    if(recaptchaVerifier) return;
    // Use INVISIBLE recaptcha — no user interaction needed
    recaptchaVerifier = new firebase.auth.RecaptchaVerifier('sendOtpBtn', {
      'size': 'invisible',
      'callback': function(response) {
        console.log('reCAPTCHA verified');
      }
    });
  } catch(e) {
    console.warn('reCAPTCHA setup error:', e);
  }
}

var CU=null, ROLE='auditor', PAGE='';
var ONLINE={}, OTP_STORE={}, LOCKED_COLS={};
var MASTER={u:'YourUsername',p:'YourPassword'};

var AUDITORS=[];
(function(){
  for(var i=1;i<=50;i++){
    var n=i<10?'0'+i:''+i;
    AUDITORS.push({id:i,username:'auditor'+n,password:'Audit@'+n,name:'Auditor '+n,phone:'',location:'',assignedMenuId:null,lastLogin:''});
  }
})();
var nextAID=41;

var MENUS=[
  {id:1,name:'Store',subs:[]},
  {id:2,name:'Warehouse',subs:[]},
  {id:3,name:'Service Center',subs:[]},
  {id:4,name:'TVM',subs:[]},
  {id:5,name:'EMS',subs:[]},
  {id:6,name:'MADUL 4',subs:[]},
  {id:7,name:'Vendor Location',subs:[]}
];
var nextMID=8;

var ECOLS=['Sl.No','Material','Description','Plant','Storage Location','Unrestricted Stock','Storage Bin','MAP/SPC','Stock Values','Physical Quantity','Quantity Variance','Discrepancy Value','SAA Team','Remarks','DATE','TIME'];

var STOCK=[];
var nextSID=1;

// ═══════════ LOCAL STORAGE PERSISTENCE ═══════════
function saveToLocal(){
  try{
    localStorage.setItem('sav_stock', JSON.stringify(STOCK));
    localStorage.setItem('sav_menus', JSON.stringify(MENUS));
    localStorage.setItem('sav_auditors', JSON.stringify(AUDITORS));
    localStorage.setItem('sav_nextSID', nextSID);
    localStorage.setItem('sav_nextMID', nextMID);
    localStorage.setItem('sav_locked', JSON.stringify(LOCKED_COLS));
    // Save current user session
    if(CU) localStorage.setItem('sav_cu', JSON.stringify(CU));
    // Save to Firebase
    if(FB_READY && db){
      var stockObj={}; for(var i=0;i<STOCK.length;i++) stockObj[STOCK[i].id]=STOCK[i]; db.ref('stock').set(stockObj).catch(function(e){console.warn('FB stock save:',e);});
      var menusObj={}; for(var i=0;i<MENUS.length;i++) menusObj[i]=MENUS[i]; db.ref('menus').set(menusObj).catch(function(e){console.warn('FB menus save:',e);});
      var audObj={}; for(var i=0;i<AUDITORS.length;i++) audObj[AUDITORS[i].id]=AUDITORS[i]; db.ref('auditors').set(audObj).catch(function(e){console.warn('FB auditors save:',e);});
      db.ref('meta').set({nextSID:nextSID,nextMID:nextMID,locked:LOCKED_COLS,updated:Date.now()}).catch(function(e){console.warn('FB meta save:',e);});
    }
    var badge=document.getElementById('fbBadge');
    if(badge){
      badge.innerHTML='<span style="color:var(--ok)">&#9679;</span> '+(FB_READY?'Saving...':'Saving...');
      setTimeout(function(){
        var b=document.getElementById('fbBadge');
        if(b) b.innerHTML='<span style="color:var(--ok)">&#9679;</span> '+(FB_READY?'Firebase Live':'Local');
      },1500);
    }
  }catch(e){console.warn('Save error:',e);}
}

function loadFromLocal(){
  try{
    var s=localStorage.getItem('sav_stock');
    if(s) STOCK=JSON.parse(s);
    var savedMenus=localStorage.getItem('sav_menus');
    if(savedMenus){
      var pm=JSON.parse(savedMenus);
      // Sanitize: filter out null/undefined, ensure subs array
      MENUS=pm.filter(function(x){return x&&x.id;}).map(function(x){
        return {id:parseInt(x.id)||x.id,name:x.name||'Location',subs:Array.isArray(x.subs)?x.subs:[]};
      });
    }
    var a=localStorage.getItem('sav_auditors');
    if(a) AUDITORS=JSON.parse(a);
    var ns=localStorage.getItem('sav_nextSID');
    if(ns) nextSID=parseInt(ns)||1;
    var nm=localStorage.getItem('sav_nextMID');
    if(nm) nextMID=parseInt(nm)||8;
    var lk=localStorage.getItem('sav_locked');
    if(lk) LOCKED_COLS=JSON.parse(lk);
    // Sanitize MENUS — ensure all entries have valid structure
    MENUS=MENUS.filter(function(m){return m&&typeof m==='object'&&m.id;});
    MENUS.forEach(function(m){if(!Array.isArray(m.subs))m.subs=[];});
    // Sanitize STOCK
    STOCK=STOCK.filter(function(s){return s&&typeof s==='object'&&s.id;});
    var badge=document.getElementById('fbBadge');
    if(badge) badge.innerHTML='<span style="color:var(--ok)">&#9679;</span> '+(s?'Loaded':'Local');
  }catch(e){console.warn('Load error:',e);}
}

// ═══════════ HELPERS ═══════════
function sn(sm){return typeof sm==='object'?sm.name:sm;}
function sc(sm){return typeof sm==='object'?(sm.cols||ECOLS):ECOLS;}
function menuById(id){var nid=parseInt(id)||id;for(var i=0;i<MENUS.length;i++){if(!MENUS[i])continue;if(MENUS[i].id===nid||MENUS[i].id===id)return MENUS[i];}return null;}
function auditorById(id){for(var i=0;i<AUDITORS.length;i++) if(AUDITORS[i].id===id) return AUDITORS[i]; return null;}
function stockById(id){for(var i=0;i<STOCK.length;i++) if(STOCK[i].id===id) return STOCK[i]; return null;}
function badge(s){var c=s==='submitted'?'b-ok':s==='process'?'b-warn':'b-pend'; return '<span class="badge '+c+'">'+s+'</span>';}
function today(){return new Date().toISOString().split('T')[0];}
function nowTime(){return new Date().toTimeString().slice(0,5);}
function fg(lbl,inp){return '<div class="mfg"><label>'+lbl+'</label>'+inp+'</div>';}
function modal(title,body,foot){
  document.getElementById('mTitle').textContent=title;
  document.getElementById('mBody').innerHTML=body;
  document.getElementById('mFoot').innerHTML=foot;
  document.getElementById('modalOv').classList.remove('hidden');
}
function closeModal(){document.getElementById('modalOv').classList.add('hidden');}
document.getElementById('modalOv').addEventListener('click',function(e){if(e.target===this)closeModal();});

// ═══════════ AUTH ═══════════
function switchRole(r){
  ROLE=r;
  var tabs=document.querySelectorAll('.tab-btn');
  tabs[0].classList.toggle('active',r==='auditor');
  tabs[1].classList.toggle('active',r==='master');
  document.getElementById('masterSec').classList.toggle('hidden',r==='auditor');
  document.getElementById('auditorSec').classList.toggle('hidden',r==='master');
  document.getElementById('loginErr').textContent='';
  if(r==='auditor') setTimeout(setupRecaptcha, 100);
  var cd=document.getElementById('credDisp');
  if(cd){
    if(r==='master') cd.innerHTML='<div>&#128273; <b>Master:</b> Vishnu27 / Vishnu@27</div>';
    else cd.innerHTML='<div>&#128100; <b>Username login:</b> auditor01/Audit@01 ... auditor40/Audit@40</div><div style="margin-top:4px;opacity:.6;font-size:11px">Or phone OTP (set phone in Users first)</div>';
  }
}

function doLogin(){
  var u=document.getElementById('mUser').value.trim();
  var p=document.getElementById('mPass').value.trim();
  var err=document.getElementById('loginErr');
  if(!u||!p){err.textContent='Enter username and password';return;}
  err.textContent='';
  // Check Firebase for master credentials if connected
  if(FB_READY && db){
    db.ref('master_credentials').once('value').then(function(snap){
      var mc = snap.val();
      var mu = mc ? mc.username : MASTER.u;
      var mp = mc ? mc.password : MASTER.p;
      if(u===mu && p===mp){
        CU={name:u, role:'master'};
        launch();
      } else if(u===MASTER.u && p===MASTER.p){
        // Also allow default credentials
        CU={name:u, role:'master'};
        launch();
      } else {
        document.getElementById('loginErr').textContent='Invalid master credentials';
      }
    }).catch(function(){
      // Firebase failed — fall back to local check
      if(u===MASTER.u && p===MASTER.p){CU={name:u,role:'master'};launch();}
      else document.getElementById('loginErr').textContent='Invalid master credentials';
    });
  } else {
    if(u===MASTER.u && p===MASTER.p){CU={name:u,role:'master'};launch();}
    else err.textContent='Invalid master credentials';
  }
}

function doAuditorUsernameLogin(){
  var u=document.getElementById('aUser').value.trim();
  var p=document.getElementById('aPass').value.trim();
  var err=document.getElementById('loginErr');
  if(!u||!p){err.textContent='Enter username and password';return;}
  var f=null;
  for(var i=0;i<AUDITORS.length;i++) if(AUDITORS[i].username.toLowerCase()===u.toLowerCase()&&AUDITORS[i].password===p){f=AUDITORS[i];break;}
  if(f){
    ONLINE[f.username]=true;
    f.lastLogin=new Date().toLocaleString();
    saveToLocal();
    CU={name:f.name,role:'auditor',username:f.username,assignedMenuId:f.assignedMenuId||null};
    launch();
  } else err.textContent='Invalid auditor credentials';
}

function sendOTP(){
  var rawPhone = document.getElementById('aPhone').value.trim();
  var err = document.getElementById('loginErr');
  var cleanPhone = rawPhone.replace(/\D/g,'');
  if(cleanPhone.length < 10){ err.textContent = 'Enter valid phone number'; return; }

  // Format phone with country code
  var phoneWithCode = rawPhone.startsWith('+') ? rawPhone : '+91' + cleanPhone;

  // Check if phone is registered
  var found = null;
  for(var i=0;i<AUDITORS.length;i++){
    if(AUDITORS[i].phone && AUDITORS[i].phone.replace(/\D/g,'').slice(-10) === cleanPhone.slice(-10)){
      found = AUDITORS[i]; break;
    }
  }

  if(!found){
    err.textContent = 'Phone not registered. Ask master to add your phone in Users.';
    return;
  }

  OTP_STORE['pending_auditor'] = found.id;
  err.textContent = '';

  // Use Firebase Phone Auth if available
  if(FB_READY && fbAuth){
    if(!recaptchaVerifier) setupRecaptcha();
    err.textContent = 'Sending OTP...';
    fbAuth.signInWithPhoneNumber(phoneWithCode, recaptchaVerifier)
      .then(function(result){
        confirmationResult = result;
        document.getElementById('aStep1').classList.add('hidden');
        document.getElementById('aStep2').classList.remove('hidden');
        document.getElementById('o1').focus();
        err.textContent = '';
        // Store phone display
        var disp = document.getElementById('otpPhoneDisp');
        if(disp) disp.textContent = phoneWithCode;
      })
      .catch(function(e){
        err.textContent = 'Failed to send OTP: ' + (e.message||e.code||'unknown error');
        console.error('OTP send error:', e);
        // Reset recaptcha on error
        if(recaptchaVerifier){
          recaptchaVerifier.clear();
          recaptchaVerifier = null;
          setupRecaptcha();
        }
      });
  } else {
    // Fallback: mock OTP (for testing without Firebase)
    var mockOtp = Math.floor(100000 + Math.random()*900000).toString();
    OTP_STORE[cleanPhone] = {otp:mockOtp, auditorId:found.id, expires:Date.now()+300000};
    alert('TEST MODE\nOTP for ' + found.name + ': ' + mockOtp + '\n\n(Connect Firebase for real SMS)');
    document.getElementById('aStep1').classList.add('hidden');
    document.getElementById('aStep2').classList.remove('hidden');
    document.getElementById('o1').focus();
    err.textContent = '';
  }
}

function getOTPVal(){return ['o1','o2','o3','o4','o5','o6'].map(function(id){return document.getElementById(id).value;}).join('');}
function otpNext(el,nextId){if(el.value&&nextId){var n=document.getElementById(nextId);if(n)n.focus();}}
function otpBack(e,el,prevId){if(e.key==='Backspace'&&!el.value&&prevId){var p=document.getElementById(prevId);if(p){p.value='';p.focus();}}}
function autoVerify(){if(getOTPVal().length===6)verifyOTP();}

function verifyOTP(){
  var entered = getOTPVal();
  var err = document.getElementById('loginErr');
  if(entered.length !== 6){ err.textContent = 'Enter 6-digit OTP'; return; }

  // Firebase OTP verification
  if(FB_READY && confirmationResult){
    err.textContent = 'Verifying...';
    confirmationResult.confirm(entered)
      .then(function(userCredential){
        // OTP correct — find auditor from pending store
        var audId = OTP_STORE['pending_auditor'];
        var f = audId ? auditorById(audId) : null;
        if(!f){
          // Try to match by phone
          var rawPhone = document.getElementById('aPhone').value.trim().replace(/\D/g,'');
          for(var i=0;i<AUDITORS.length;i++){
            if(AUDITORS[i].phone && AUDITORS[i].phone.replace(/\D/g,'').slice(-10) === rawPhone.slice(-10)){
              f = AUDITORS[i]; break;
            }
          }
        }
        if(!f){ err.textContent = 'Auditor account not found'; return; }
        delete OTP_STORE['pending_auditor'];
        confirmationResult = null;
        ONLINE[f.username] = true;
        f.lastLogin = new Date().toLocaleString();
        if(FB_READY && db) db.ref('logins/'+f.id).set({name:f.name,username:f.username,phone:f.phone||'',time:f.lastLogin,status:'active'});
        saveToLocal();
        CU = {name:f.name, role:'auditor', username:f.username, assignedMenuId:f.assignedMenuId||null};
        launch();
      })
      .catch(function(e){
        err.textContent = 'Invalid OTP. Please try again. (' + (e.code||'error') + ')';
        console.error('OTP verify error:', e);
      });
  } else {
    // Fallback mock verify
    var cleanPhone = document.getElementById('aPhone').value.trim().replace(/\D/g,'');
    var rec = OTP_STORE[cleanPhone];
    if(!rec){ err.textContent = 'Request OTP first'; return; }
    if(Date.now() > rec.expires){ err.textContent = 'OTP expired'; delete OTP_STORE[cleanPhone]; backToPhone(); return; }
    if(rec.otp !== entered){ err.textContent = 'Invalid OTP'; return; }
    var f = auditorById(rec.auditorId);
    if(!f){ err.textContent = 'Auditor not found'; return; }
    delete OTP_STORE[cleanPhone];
    ONLINE[f.username] = true;
    f.lastLogin = new Date().toLocaleString();
    saveToLocal();
    CU = {name:f.name, role:'auditor', username:f.username, assignedMenuId:f.assignedMenuId||null};
    launch();
  }
}

function backToPhone(){
  document.getElementById('aStep1').classList.remove('hidden');
  document.getElementById('aStep2').classList.add('hidden');
  ['o1','o2','o3','o4','o5','o6'].forEach(function(id){document.getElementById(id).value='';});
  document.getElementById('loginErr').textContent='';
}

function doLogout(){
  if(CU&&CU.role==='auditor') delete ONLINE[CU.username];
  CU=null;
  localStorage.removeItem('sav_cu');
  document.getElementById('appWrap').style.display='none';
  document.getElementById('loginWrap').style.display='flex';
  document.getElementById('mUser').value='';
  document.getElementById('mPass').value='';
  document.getElementById('loginErr').textContent='';
}

function launch(){
  // Try Firebase first, fallback to localStorage
  if(FB_READY && db){
    // Load all data in parallel from Firebase
    var loaded = {stock:false, menus:false, auditors:false, meta:false};
    function tryLaunch(){
      if(loaded.stock && loaded.menus && loaded.auditors && loaded.meta) _doLaunch();
    }
    db.ref('stock').once('value').then(function(snap){
      var data = snap.val();
      if(data){
        var vals = Object.values(data);
        STOCK = vals.filter(function(s){return s&&s.id;});
        localStorage.setItem('sav_stock', JSON.stringify(STOCK));
      }
      loaded.stock = true; tryLaunch();
    }).catch(function(){ loaded.stock=true; tryLaunch(); });

    db.ref('menus').once('value').then(function(snap){
      var data = snap.val();
      if(data){
        var vals = Object.values(data);
        MENUS = vals.filter(function(m){return m&&m.id;});
        MENUS.forEach(function(m){if(!Array.isArray(m.subs))m.subs=[];});
        localStorage.setItem('sav_menus', JSON.stringify(MENUS));
      }
      loaded.menus = true; tryLaunch();
    }).catch(function(){ loaded.menus=true; tryLaunch(); });

    db.ref('auditors').once('value').then(function(snap){
      var data = snap.val();
      if(data){
        var vals = Object.values(data);
        AUDITORS = vals.filter(function(a){return a&&a.id;});
        localStorage.setItem('sav_auditors', JSON.stringify(AUDITORS));
      }
      loaded.auditors = true; tryLaunch();
    }).catch(function(){ loaded.auditors=true; tryLaunch(); });

    db.ref('meta').once('value').then(function(snap){
      var data = snap.val();
      if(data){
        if(data.nextSID) nextSID = parseInt(data.nextSID)||1;
        if(data.nextMID) nextMID = parseInt(data.nextMID)||8;
        if(data.locked) LOCKED_COLS = data.locked;
      }
      loaded.meta = true; tryLaunch();
    }).catch(function(){ loaded.meta=true; tryLaunch(); });
    return;
  }
  loadFromLocal();
  _doLaunch();
}

function _doLaunch(){
  // Save session so refresh doesn't log out
  if(CU) localStorage.setItem('sav_cu', JSON.stringify(CU));
  document.getElementById('loginWrap').style.display='none';
  document.getElementById('appWrap').style.display='flex';
  document.getElementById('roleLabel').textContent=CU.role==='master'?'Master Panel':'Auditor Panel';
  document.getElementById('uName').textContent=CU.name;
  document.getElementById('avIcon').textContent=CU.name[0].toUpperCase();
  buildNav();
  go(CU.role==='master'?'mDash':'aDash');
}

// ═══════════ NAV ═══════════
var MNAV=[
  {p:'mDash',i:'',l:'Dashboard'},
  {p:'mStock',i:'',l:'Stock Data'},
  {p:'mLoc',i:'',l:'Location'},
  {p:'mUsers',i:'',l:'Users'},
  {p:'mAuditors',i:'',l:'Auditor Accounts'},
  {p:'mReports',i:'',l:'Daily Reports'},
  {p:'mTotal',i:'',l:'Total Report'},
  {p:'mChart',i:'',l:'Progress Chart'}
];
var ANAV=[
  {p:'aDash',i:'',l:'Dashboard'},
  {p:'aLoc',i:'',l:'Location'},
  {p:'aHistory',i:'',l:'My Submissions'}
];
var TITLES={mDash:'Dashboard',mStock:'Stock Data',mLoc:'Location',mUsers:'Users',mAuditors:'Auditor Accounts',mReports:'Daily Reports',mTotal:'Total Report',mChart:'Progress Chart',aDash:'Dashboard',aLoc:'Location',aHistory:'My Submissions',aStock:'Stock Entry'};

function buildNav(){
  var items=CU.role==='master'?MNAV:ANAV;
  var h='';
  for(var i=0;i<items.length;i++) h+='<div class="nav-item" id="nav_'+items[i].p+'" onclick="go(\''+items[i].p+'\');closeSidebar()">'+items[i].l+'</div>';
  document.getElementById('sbNav').innerHTML=h;
  document.getElementById('sbFoot').textContent=(CU.role==='master'?'Master: ':'Auditor: ')+CU.name;
}

function setNav(p){
  document.querySelectorAll('.nav-item').forEach(function(el){el.classList.remove('active');});
  var el=document.getElementById('nav_'+p); if(el) el.classList.add('active');
}

function go(p){
  loadFromLocal(); // Always reload from storage so master+auditor see same data
  PAGE=p; setNav(p);
  document.getElementById('pageTitle').textContent=TITLES[p]||p;
  var c=document.getElementById('mainContent');
  if(p==='mDash') c.innerHTML=pgMDash();
  else if(p==='mStock') c.innerHTML=pgMStock();
  else if(p==='mLoc') c.innerHTML=pgMLoc();
  else if(p==='mUsers') c.innerHTML=pgMUsers();
  else if(p==='mAuditors') c.innerHTML=pgMAuditors();
  else if(p==='mReports') c.innerHTML=pgMReports();
  else if(p==='mTotal') c.innerHTML=pgMTotal();
  else if(p==='mChart') c.innerHTML=pgMChart();
  else if(p==='aDash') c.innerHTML=pgADash();
  else if(p==='aLoc') c.innerHTML=pgALoc();
  else if(p==='aHistory') c.innerHTML=pgAHistory();
}

function toggleSidebar(){
  document.getElementById('sidebar').classList.toggle('open');
  document.getElementById('mobOv').classList.toggle('show');
}
function closeSidebar(){
  document.getElementById('sidebar').classList.remove('open');
  document.getElementById('mobOv').classList.remove('show');
}

// ═══════════ SHARED TABLE ═══════════
function tbl(items,actions,showAud){
  if(!items.length) return '<p style="padding:1.5rem;text-align:center;color:var(--muted)">No records</p>';
  var h='<table><thead><tr><th>Material</th><th>Description</th><th>Sub Location</th><th>Sys Qty</th><th>Phy Qty</th><th>Variance</th><th>MAP/SPC</th><th>Stock Value</th>'+(showAud?'<th>Auditor</th><th>Date</th>':'')+'<th>Status</th>'+(actions?'<th>Actions</th>':'')+'</tr></thead><tbody>';
  for(var i=0;i<items.length;i++){
    var s=items[i],ex=s.extra||{};
    var dc=(s.disc||0)<0?'var(--danger)':(s.disc||0)>0?'green':'var(--muted)';
    h+='<tr>'
      +'<td style="font-weight:600">'+(ex.material||s.sku||'—')+'</td>'
      +'<td>'+s.name+'</td>'
      +'<td>'+s.sub+'</td>'
      +'<td style="text-align:center">'+s.sQty+'</td>'
      +'<td style="text-align:center">'+(s.pQty!==null?s.pQty:'—')+'</td>'
      +'<td style="text-align:center;color:'+dc+';font-weight:600">'+(s.disc!==null?s.disc:'—')+'</td>'
      +'<td style="text-align:right">'+(ex.mapSpc||s.rate||'—')+'</td>'
      +'<td style="text-align:right">'+s.amt.toLocaleString()+'</td>'
      +(showAud?'<td>'+(s.aud||'—')+'</td><td>'+(s.date||'—')+'</td>':'')
      +'<td>'+badge(s.st)+'</td>'
      +(actions?'<td><div class="fr"><button class="btn btn-ghost btn-sm" onclick="editStk('+s.id+')">✏</button><button class="btn btn-ghost btn-sm" style="color:var(--danger)" onclick="delStk('+s.id+')">Del</button></div></td>':'')
      +'</tr>';
  }
  return h+'</tbody></table>';
}

// ═══════════ MASTER: DASHBOARD ═══════════
function pgMDash(){
  var tot=STOCK.length,sub=0,pro=0,pen=0,val=0;
  for(var i=0;i<STOCK.length;i++){if(STOCK[i].st==='submitted')sub++;else if(STOCK[i].st==='process')pro++;else pen++;val+=STOCK[i].amt;}
  var compVal=0;
  for(var i=0;i<STOCK.length;i++) if(STOCK[i].st==='submitted') compVal+=STOCK[i].amt;
  var td=STOCK.filter(function(s){return s.date===today();});
  
  // Calculate completion percentage
  var completionPct = tot > 0 ? Math.round((sub / tot) * 100) : 0;
  
  // Audit Summary by Location
  var locSummary = '';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    if(!m||!m.id) continue;
    var locItems=STOCK.filter(function(s){return s.mid===m.id;});
    var locSub=0, locPro=0, locPen=0;
    for(var k=0;k<locItems.length;k++){
      if(locItems[k].st==='submitted')locSub++;
      else if(locItems[k].st==='process')locPro++;
      else locPen++;
    }
    var locPct = locItems.length > 0 ? Math.round((locSub / locItems.length) * 100) : 0;
    locSummary+='<tr>'
      +'<td><b>'+m.name+'</b></td>'
      +'<td style="text-align:center"><span class="badge b-pend">'+locItems.length+'</span></td>'
      +'<td style="text-align:center"><span class="badge b-ok">'+locSub+'</span></td>'
      +'<td style="text-align:center"><span class="badge b-warn">'+locPro+'</span></td>'
      +'<td style="text-align:center"><span class="badge">'+locPen+'</span></td>'
      +'<td><div style="background:#e0d4ff;border-radius:3px;height:6px;width:100px;overflow:hidden;display:inline-block">'
      +'<div style="background:var(--pri2);height:100%;width:'+locPct+'%"></div></div></td>'
      +'<td style="text-align:center;font-weight:600">'+locPct+'%</td>'
      +'</tr>';
  }
  
  // Daily Status Summary
  var dailySummary = '';
  var todayItems = STOCK.filter(function(s){return s.date===today();});
  var todaySub=0, todayPro=0, todayPen=0;
  for(var k=0;k<todayItems.length;k++){
    if(todayItems[k].st==='submitted')todaySub++;
    else if(todayItems[k].st==='process')todayPro++;
    else todayPen++;
  }
  
  // Auditor Performance
  var auditorPerf = '';
  for(var i=0;i<AUDITORS.length;i++){
    var a=AUDITORS[i];
    var audItems=STOCK.filter(function(s){return s.aud===a.name;});
    if(audItems.length===0) continue;
    var audSub=0;
    for(var k=0;k<audItems.length;k++) if(audItems[k].st==='submitted') audSub++;
    var audPct = audItems.length > 0 ? Math.round((audSub / audItems.length) * 100) : 0;
    var isOn=!!ONLINE[a.username];
    auditorPerf+='<tr>'
      +'<td><b>'+a.name+'</b></td>'
      +'<td style="color:var(--acc);font-family:monospace">'+a.username+'</td>'
      +'<td><span class="badge '+(isOn?'b-ok':'b-pend')+'">'+(isOn?'🟢 Online':'🔴 Offline')+'</span></td>'
      +'<td style="text-align:center">'+audItems.length+'</td>'
      +'<td style="text-align:center;color:var(--ok);font-weight:600">'+audSub+'</td>'
      +'<td style="text-align:center">'+audPct+'%</td>'
      +'<td style="font-size:11px;color:var(--muted)">'+(a.lastLogin||'—')+'</td>'
      +'</tr>';
  }
  
  return '<div>'
    + '<!-- KPI SECTION -->'
    + '<div class="stat-row" style="margin-bottom:1.5rem">'
    + '<div class="stat-card"><div class="lbl">📊 Total Items</div><div class="val">'+tot+'</div></div>'
    + '<div class="stat-card"><div class="lbl">✅ Submitted</div><div class="val" style="color:var(--ok)">'+sub+'</div><div style="font-size:11px;color:var(--muted);margin-top:4px">'+Math.round((sub/tot)*100)+'%</div></div>'
    + '<div class="stat-card"><div class="lbl">⏳ In Process</div><div class="val" style="color:var(--warn)">'+pro+'</div></div>'
    + '<div class="stat-card"><div class="lbl">⏸ Pending</div><div class="val" style="color:var(--muted)">'+pen+'</div></div>'
    + '<div class="stat-card"><div class="lbl">💰 Stock Value</div><div class="val" style="font-size:16px">₹'+val.toLocaleString()+'</div></div>'
    + '<div class="stat-card"><div class="lbl">🎯 Completed Value</div><div class="val" style="font-size:14px;color:var(--ok)">₹'+compVal.toLocaleString()+'</div></div>'
    + '</div>'
    
    + '<!-- DAILY STATUS UPDATE -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>📅 Daily Status Update - '+today()+'</b></div>'
    + '<div style="padding:1rem;background:#f8f6ff">'
    + '<div class="fr" style="gap:2rem">'
    + '<div><span style="font-size:12px;color:var(--muted)">TODAY\'S ENTRIES</span><div style="font-size:24px;font-weight:700;color:var(--pri)">'+todayItems.length+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">SUBMITTED</span><div style="font-size:24px;font-weight:700;color:var(--ok)">'+todaySub+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">PROCESSING</span><div style="font-size:24px;font-weight:700;color:var(--warn)">'+todayPro+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">PENDING</span><div style="font-size:24px;font-weight:700;color:#999">'+todayPen+'</div></div>'
    + '</div>'
    + '</div>'
    + '</div>'
    
    + '<!-- AUDIT SUMMARY BY LOCATION -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>📍 Audit Summary by Location</b></div>'
    + '<div class="tbl-wrap"><table>'
    + '<thead><tr><th>Location</th><th>Total</th><th>✅ Done</th><th>⏳ Process</th><th>⏸ Pending</th><th>Progress</th><th>%</th></tr></thead>'
    + '<tbody>'+locSummary+'</tbody>'
    + '</table></div>'
    + '</div>'
    
    + '<!-- AUDITOR PERFORMANCE -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>👥 Auditor Performance</b></div>'
    + '<div class="tbl-wrap"><table>'
    + '<thead><tr><th>Auditor</th><th>Username</th><th>Status</th><th>Items</th><th>Submitted</th><th>Progress</th><th>Last Active</th></tr></thead>'
    + '<tbody>'+auditorPerf+'</tbody>'
    + '</table></div>'
    + '</div>'
    
    + '<!-- TODAY\'S SUBMISSIONS -->'
    + '<div class="card">'
    + '<div class="card-hdr"><b>📝 Today\'s Submissions ('+td.length+' entries)</b>'
    + '<button class="btn btn-ok btn-sm" onclick="dlExcel()">⬇ Download Excel</button></div>'
    + '<div class="tbl-wrap">'+tbl(td,false,true)+'</div>'
    + '</div>'
    
    + '</div>';
}
  
  // Auditor Performance
  var auditorPerf = '';
  for(var i=0;i<AUDITORS.length;i++){
    var a=AUDITORS[i];
    var audItems=STOCK.filter(function(s){return s.aud===a.name;});
    if(audItems.length===0) continue;
    var audSub=0;
    for(var k=0;k<audItems.length;k++) if(audItems[k].st==='submitted') audSub++;
    var audPct = audItems.length > 0 ? Math.round((audSub / audItems.length) * 100) : 0;
    var isOn=!!ONLINE[a.username];
    auditorPerf+='<tr>'
      +'<td><b>'+a.name+'</b></td>'
      +'<td style="color:var(--acc);font-family:monospace">'+a.username+'</td>'
      +'<td><span class="badge '+(isOn?'b-ok':'b-pend')+'">'+(isOn?'🟢 Online':'🔴 Offline')+'</span></td>'
      +'<td style="text-align:center">'+audItems.length+'</td>'
      +'<td style="text-align:center;color:var(--ok);font-weight:600">'+audSub+'</td>'
      +'<td style="text-align:center">'+audPct+'%</td>'
      +'<td style="font-size:11px;color:var(--muted)">'+(a.lastLogin||'—')+'</td>'
      +'</tr>';
  }
  
  return '<div>'
    + '<!-- KPI SECTION -->'
    + '<div class="stat-row" style="margin-bottom:1.5rem">'
    + '<div class="stat-card"><div class="lbl">📊 Total Items</div><div class="val">'+tot+'</div></div>'
    + '<div class="stat-card"><div class="lbl">✅ Submitted</div><div class="val" style="color:var(--ok)">'+sub+'</div><div style="font-size:11px;color:var(--muted);margin-top:4px">'+Math.round((sub/tot)*100)+'%</div></div>'
    + '<div class="stat-card"><div class="lbl">⏳ In Process</div><div class="val" style="color:var(--warn)">'+pro+'</div></div>'
    + '<div class="stat-card"><div class="lbl">⏸ Pending</div><div class="val" style="color:var(--muted)">'+pen+'</div></div>'
    + '<div class="stat-card"><div class="lbl">💰 Stock Value</div><div class="val" style="font-size:16px">₹'+val.toLocaleString()+'</div></div>'
    + '<div class="stat-card"><div class="lbl">🎯 Completed Value</div><div class="val" style="font-size:14px;color:var(--ok)">₹'+compVal.toLocaleString()+'</div></div>'
    + '</div>'
    
    + '<!-- DAILY STATUS UPDATE -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>📅 Daily Status Update - '+today()+'</b></div>'
    + '<div style="padding:1rem;background:#f8f6ff">'
    + '<div class="fr" style="gap:2rem">'
    + '<div><span style="font-size:12px;color:var(--muted)">TODAY\'S ENTRIES</span><div style="font-size:24px;font-weight:700;color:var(--pri)">'+todayItems.length+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">SUBMITTED</span><div style="font-size:24px;font-weight:700;color:var(--ok)">'+todaySub+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">PROCESSING</span><div style="font-size:24px;font-weight:700;color:var(--warn)">'+todayPro+'</div></div>'
    + '<div><span style="font-size:12px;color:var(--muted)">PENDING</span><div style="font-size:24px;font-weight:700;color:#999">'+todayPen+'</div></div>'
    + '</div>'
    + '</div>'
    + '</div>'
    
    + '<!-- AUDIT SUMMARY BY LOCATION -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>📍 Audit Summary by Location</b></div>'
    + '<div class="tbl-wrap"><table>'
    + '<thead><tr><th>Location</th><th>Total</th><th>✅ Done</th><th>⏳ Process</th><th>⏸ Pending</th><th>Progress</th><th>%</th></tr></thead>'
    + '<tbody>'+locSummary+'</tbody>'
    + '</table></div>'
    + '</div>'
    
    + '<!-- AUDITOR PERFORMANCE -->'
    + '<div class="card" style="margin-bottom:1.2rem">'
    + '<div class="card-hdr"><b>👥 Auditor Performance</b></div>'
    + '<div class="tbl-wrap"><table>'
    + '<thead><tr><th>Auditor</th><th>Username</th><th>Status</th><th>Items</th><th>Submitted</th><th>Progress</th><th>Last Active</th></tr></thead>'
    + '<tbody>'+auditorPerf+'</tbody>'
    + '</table></div>'
    + '</div>'
    
    + '<!-- TODAY'S SUBMISSIONS -->'
    + '<div class="card">'
    + '<div class="card-hdr"><b>📝 Today\'s Submissions ('+td.length+' entries)</b>'
    + '<button class="btn btn-ok btn-sm" onclick="dlExcel()">⬇ Download Excel</button></div>'
    + '<div class="tbl-wrap">'+tbl(td,false,true)+'</div>'
    + '</div>'
    
    + '</div>';
}
    +'<div class="sbox" style="margin-bottom:.8rem;width:100%">&#128269; '
    +'<input id="stockGlobalSrch" placeholder="Search all items..." style="width:85%"'
    +' oninput="stockSearchAll(this.value)"></div>'
    +'<div id="stockAccBody">';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    if(!m||!m.id) continue;
    if(!Array.isArray(m.subs)) m.subs=[];
    var mid=m.id;
    var mItems=STOCK.filter(function(s){return s.mid===mid;});
    var mItemsFiltered=f?mItems.filter(function(s){
      return s.name.toLowerCase().indexOf(f.toLowerCase())!==-1
        ||s.sub.toLowerCase().indexOf(f.toLowerCase())!==-1
        ||(s.extra&&s.extra.material&&s.extra.material.toLowerCase().indexOf(f.toLowerCase())!==-1);
    }):mItems;
    var mDone=0; for(var k=0;k<mItemsFiltered.length;k++) if(mItemsFiltered[k].st==='submitted') mDone++;
    var subHtml='';
    for(var si=0;si<m.subs.length;si++){
      var smNm=sn(m.subs[si]);
      var sItems=mItemsFiltered.filter(function(s){return s.sub===smNm;});
      if(!sItems.length&&!f) continue;
      var sDone=0; for(var k2=0;k2<sItems.length;k2++) if(sItems[k2].st==='submitted') sDone++;
      var sPct=sItems.length?Math.round(sDone/sItems.length*100):0;
      var enc=encodeURIComponent(smNm);
      var tblId='stbl_'+mid+'_'+si;
      subHtml+='<div class="acc" style="margin-bottom:.3rem">'
        +'<div class="acc-hdr" onclick="togAcc(this)">'
        +'<div class="fr" style="gap:8px"><span class="arr">&#9654;</span><b style="font-size:12px">'+smNm+'</b>'
        +'<span class="badge b-pend" style="font-size:10px">'+sItems.length+' items</span>'
        +'<span class="badge b-ok" style="font-size:10px">'+sDone+' done</span>'
        +'<div style="background:#e0d4ff;border-radius:3px;height:5px;width:60px;overflow:hidden;display:inline-block;vertical-align:middle">'
        +'<div style="background:var(--pri2);height:100%;width:'+sPct+'%"></div></div>'
        +'</div>'
        +'<div class="fr" style="gap:4px" onclick="event.stopPropagation()">'
        +'<button class="btn btn-ok btn-sm" onclick="dlSubExcel('+mid+',decodeURIComponent(this.dataset.s))" data-s="'+enc+'">Excel</button>'
        +'</div></div>'
        +'<div class="acc-body">'
        +'<div style="padding:.4rem .5rem;background:#f8f6ff;border-bottom:1px solid var(--border)">'
        +'<div class="sbox" style="width:100%">&#128269; '
        +'<input placeholder="Search material..." style="width:85%"'
        +' data-t="'+tblId+'" oninput="filterStockRows(this,this.dataset.t)"></div>'
        +'</div>'
        +'<div class="tbl-wrap"><div id="'+tblId+'">'+tbl(sItems,true,true)+'</div></div>'
        +'</div></div>';
    }
    if(!subHtml) subHtml='<p style="padding:.8rem;color:var(--muted);font-size:12px">No items</p>';
    html+='<div class="acc" style="margin-bottom:.5rem">'
      +'<div class="acc-hdr" onclick="togAcc(this)" style="background:linear-gradient(90deg,var(--pri),var(--pri2));color:#fff;border-radius:10px">'
      +'<div class="fr" style="gap:8px"><span class="arr" style="color:#fff">&#9654;</span>'
      +'<b style="color:#fff">'+m.name+'</b>'
      +'<span style="background:rgba(255,255,255,.2);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+mItemsFiltered.length+' items</span>'
      +'<span style="background:rgba(6,214,160,.3);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+mDone+' done</span>'
      +'</div>'
      +'<button class="btn btn-sm" style="background:rgba(255,255,255,.2);color:#fff;border:none" onclick="event.stopPropagation();dlLocExcel('+mid+')">All Excel</button>'
      +'</div>'
      +'<div class="acc-body">'+subHtml+'</div>'
      +'</div>';
  }
  return html+'</div>';
}

function stockSearchAll(q){
  loadFromLocal();
  document.getElementById('mainContent').innerHTML=pgMStock(q);
}


function filterStockRows(input,containerId){
  var q=input.value.toLowerCase();
  var con=document.getElementById(containerId);
  if(!con) return;
  var rows=con.querySelectorAll('tbody tr');
  for(var i=0;i<rows.length;i++){
    var txt=rows[i].textContent.toLowerCase();
    rows[i].style.display=!q||txt.indexOf(q)!==-1?'':'none';
  }
}

function togAcc(hdr){
  var body=hdr.nextElementSibling;
  var arr=hdr.querySelector('.arr');
  if(!body) return;
  var op=body.classList.contains('open');
  body.classList.toggle('open',!op);
  if(arr) arr.classList.toggle('open',!op);
  hdr.classList.toggle('open',!op);
}

// ═══════════ MASTER: UPLOAD ═══════════
function pgMUpload(){
  return '<div style="max-width:620px">'
    +'<div class="upzone" onclick="document.getElementById(\'guf\').click()">'
    +'<div style="font-size:32px;margin-bottom:.4rem"></div>'
    +'<b style="color:var(--pri)">Click to Upload Excel File</b>'
    +'<p style="font-size:12px;color:var(--muted);margin-top:3px">Supports .xlsx, .xls format</p></div>'
    +'<input type="file" id="guf" accept=".xlsx,.xls" style="display:none" onchange="handleGUpload(event)">'
    +'<div id="gPrev" style="margin-top:1rem"></div></div>';
}

function handleGUpload(ev){
  var f=ev.target.files[0]; if(!f) return;
  var r=new FileReader();
  r.onload=function(e){
    try{
      var wb=XLSX.read(e.target.result,{type:'binary'});
      var ws=wb.Sheets[wb.SheetNames[0]];
      var data=XLSX.utils.sheet_to_json(ws,{header:1,defval:''});
      if(!data||data.length<2){alert('File appears empty!');return;}
      var hdrs=data[0].map(function(h){return String(h).trim();});
      // Calculate total stock value
      var hdrLow=hdrs.map(function(h){return h.toLowerCase();});
      var stockValIdx=hdrLow.indexOf('stock values');
      if(stockValIdx===-1) stockValIdx=hdrLow.indexOf('stock value');
      var totalVal=0,count=data.length-1;
      if(stockValIdx!==-1){
        for(var i=1;i<data.length;i++){
          var v=parseFloat(String(data[i][stockValIdx]).replace(/,/g,''))||0;
          totalVal+=v;
        }
      }
      var previewRows=data.slice(1,6).map(function(row){
        return '<tr>'+row.map(function(c){return '<td>'+c+'</td>';}).join('')+'</tr>';
      }).join('');
      var encoded=encodeURIComponent(JSON.stringify(data));
      document.getElementById('gPrev').innerHTML=
        '<div class="fr" style="margin-bottom:.8rem;gap:12px">'
        +'<div class="stat-card" style="flex:1"><div class="lbl">Line Items</div><div class="val" style="font-size:18px">'+count+'</div></div>'
        +(stockValIdx!==-1?'<div class="stat-card" style="flex:1"><div class="lbl">Total Stock Value</div><div class="val" style="font-size:16px">₹'+totalVal.toLocaleString()+'</div></div>':'')
        +'</div>'
        +'<div class="ex-wrap"><div class="ex-hdr"> <span>'+f.name+' — '+count+' rows, '+hdrs.length+' columns</span></div>'
        +'<div class="tbl-wrap"><table class="ex-tbl"><tr>'+hdrs.map(function(h){return '<th>'+h+'</th>';}).join('')+'</tr>'
        +previewRows+'</table></div></div>'
        +'<div class="fr" style="margin-top:.8rem;gap:8px">'
        +'<button class="btn btn-ok" onclick="saveGUpload(decodeURIComponent(this.dataset.d))" data-d="'+encoded+'">💾 Save to Database</button>'
        +'<button class="btn btn-ghost" onclick="document.getElementById(\'guf\').click()">Upload Different File</button>'
        +'</div>';
    }catch(err){alert('Error reading Excel: '+err.message);}
  };
  r.readAsBinaryString(f);
}

function saveGUpload(encoded){
  var data=JSON.parse(encoded);
  var hdrs=data[0].map(function(h){return String(h).trim().toLowerCase();});
  var added=0;
  for(var i=1;i<data.length;i++){
    var row={};
    hdrs.forEach(function(h,j){row[h]=data[i][j]!==undefined?String(data[i][j]).trim():'';});
    if(!row['material']&&!row['description']&&!row['item name']) continue;
    var sQty=parseFloat(row['unrestricted stock']||row['system qty']||row['qty']||0)||0;
    var mapSpc=parseFloat(row['map/spc']||row['rate']||0)||0;
    var stockVal=parseFloat(row['stock values']||row['stock value']||0)||sQty*mapSpc;
    STOCK.push({
      id:nextSID++,mid:parseInt(row['menuid']||row['menu id']||1)||1,
      sub:row['storage location']||row['sub menu']||row['sub location']||'',
      name:row['description']||row['item name']||('Item '+nextSID),
      sku:row['material']||row['sku']||('MAT'+nextSID),
      sQty:sQty,pQty:null,disc:null,rate:mapSpc,amt:stockVal,
      st:'pending',aud:'',date:'',time:'',
      extra:{material:row['material']||'',plant:row['plant']||'',storageBin:row['storage bin']||'',
        mapSpc:mapSpc,purGroup:row['pur.group']||'',purGroupDes:row['pur.group des']||'',
        saaTeam:'',remarks:row['remarks']||''}
    });
    added++;
  }
  saveToLocal();
  alert(added+' items saved!');
  go(PAGE);
}

// ═══════════ MASTER: LOCATION MANAGER ═══════════
function pgMLoc(){
  var html='<div class="fr" style="margin-bottom:.8rem">'
    +'<button class="btn btn-pri" onclick="addLocModal()">+ Add Location</button>'
    +'</div><div>';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    if(!m||!m.id) continue;
    if(!Array.isArray(m.subs)) m.subs=[];
    var mid=m.id, mname=m.name;
    var tot=0; for(var k=0;k<STOCK.length;k++) if(STOCK[k].mid===m.id) tot++;
    var subRows='';
    for(var si=0;si<m.subs.length;si++){
      var sm=m.subs[si]; if(!sm) continue;
      var nm=sn(sm),co=sc(sm),cnt=0;
      for(var k=0;k<STOCK.length;k++) if(STOCK[k].mid===m.id&&STOCK[k].sub===nm) cnt++;
      var enc=encodeURIComponent(nm);
      // Build column chips with lock buttons (master only)
      var colChips=co.map(function(col){
        var key='L'+m.id+'_'+nm+'_'+col;
        var locked=!!LOCKED_COLS[key];
        var safeCol=col.replace(/"/g,'&quot;');
        return '<span class="col-chip" style="'+(locked?'background:#ffeaea;color:var(--danger);border-color:#f0bebe':'')+'">'
          +col+' <button title="'+(locked?'Unlock':'Lock')+'" style="border:none;background:none;cursor:pointer;font-size:10px;padding:0 1px"'
          +' onclick="toggleLock('+m.id+','+si+',this.dataset.col)" data-col="'+safeCol+'">'
          +(locked?'&#128274;':'&#128275;')+'</button></span>';
      }).join('');;
      subRows+='<tr>'
        +'<td style="font-weight:600">'+nm+'</td>'
        +'<td><div class="col-chips">'+colChips+'</div></td>'
        +'<td style="text-align:center">'+cnt+'</td>'
        +'<td><div class="fr" style="gap:4px">'
        +'<button class="btn btn-ok btn-sm" onclick="openSubUpload('+m.id+','+si+')">Upload</button>'
        +'<button class="btn btn-ghost btn-sm" onclick="dlSubExcel('+m.id+',decodeURIComponent(this.dataset.sub))" data-sub="'+enc+'">Excel</button>'
        +'<button class="btn btn-ghost btn-sm" onclick="editSubCols('+m.id+','+si+')">Cols</button>'
        +'<button class="btn btn-ghost btn-sm" style="background:#faeeda;color:var(--warn);border-color:var(--warn)" onclick="lockAllCols('+m.id+',this.dataset.nm)" data-nm="'+nm+'">Lock All</button>'
        +'<button class="btn btn-ghost btn-sm" style="color:var(--ok)" onclick="unlockAllCols('+m.id+',this.dataset.nm)" data-nm="'+nm+'">Unlock All</button>'
        +'<button class="btn btn-ghost btn-sm" style="color:var(--danger)" onclick="delSub('+m.id+','+si+')">Del</button>'
        +'</div></td></tr>';
    }
    html+='<div class="acc" style="margin-bottom:.5rem">'
      +'<div class="acc-hdr" onclick="togAcc(this)" style="background:linear-gradient(90deg,var(--pri),var(--pri2));color:#fff;border-radius:10px">'
      +'<div class="fr" style="gap:8px"><span class="arr" style="color:#fff">▶</span>'
      +'<b style="color:#fff">'+m.name+'</b>'
      +'<span style="background:rgba(255,255,255,.2);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+m.subs.length+' sub locations</span>'
      +'<span style="background:rgba(6,214,160,.3);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+tot+' items</span>'
      +'</div>'
      +'<div class="fr" style="gap:4px" onclick="event.stopPropagation()">'
      +'<button class="btn btn-sm" style="background:rgba(255,255,255,.2);color:#fff;border:none" onclick="addSubModal('+m.id+')">+ Sub Location</button>'
      +'<button class="btn btn-sm" style="background:rgba(255,255,255,.15);color:#fff;border:none" onclick="editLocModal('+m.id+')">✏</button>'
      +'<button class="btn btn-sm" style="background:rgba(255,0,0,.2);color:#fff;border:none" onclick="delLoc('+m.id+')">Del</button>'
      +'</div></div>'
      +'<div class="acc-body">'
      +'<div class="tbl-wrap"><table><thead><tr><th>Sub Location</th><th>Excel Columns</th><th>Items</th><th>Actions</th></tr></thead><tbody>'+subRows+'</tbody></table></div>'
      +'</div></div>';
  }
  return html+'</div>';
}

// ═══════════ MASTER: USERS ═══════════
function pgMUsers(f){
  f=f||'';
  var list=f?AUDITORS.filter(function(a){return a.name.toLowerCase().indexOf(f.toLowerCase())!==-1||a.username.toLowerCase().indexOf(f.toLowerCase())!==-1;}):AUDITORS;
  var onCnt=0; for(var i=0;i<AUDITORS.length;i++) if(ONLINE[AUDITORS[i].username]) onCnt++;
  var rows='';
  for(var i=0;i<list.length;i++){
    var a=list[i],isOn=!!ONLINE[a.username],subs=0;
    for(var k=0;k<STOCK.length;k++) if(STOCK[k].aud===a.name) subs++;
    var aml=a.assignedMenuId?menuById(a.assignedMenuId):null; var loc=aml?aml.name:'All';
    rows+='<tr>'
      +'<td>'+a.id+'</td>'
      +'<td><span class="badge '+(isOn?'b-ok':'b-pend')+'">'+(isOn?'Online':'Offline')+'</span></td>'
      +'<td><b>'+a.name+'</b></td>'
      +'<td style="color:var(--acc);font-family:monospace">'+a.username+'</td>'
      +'<td style="font-family:monospace">'+(a.phone||'—')+'</td>'
      +'<td><span id="pw_'+a.id+'" style="letter-spacing:2px">••••••••</span>'
      +' <button onclick="togPwd('+a.id+')" style="border:none;background:none;cursor:pointer;font-size:11px;color:var(--acc)">show</button></td>'
      +'<td>'+loc+'</td>'
      +'<td><span class="badge b-info">'+subs+' items</span></td>'
      +'<td><div class="fr" style="gap:4px">'
      +'<button class="btn btn-pri btn-sm" onclick="editUserModal('+a.id+')">Edit</button>'
      +'<button class="btn btn-ghost btn-sm" style="color:var(--danger)" onclick="delUser('+a.id+')">Del</button>'
      +'</div></td></tr>';
  }
  return '<div class="stat-row" style="margin-bottom:.8rem">'
    +'<div class="stat-card"><div class="lbl">Total Users</div><div class="val">'+AUDITORS.length+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Online</div><div class="val" style="color:var(--ok)">'+onCnt+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Offline</div><div class="val" style="color:var(--muted)">'+(AUDITORS.length-onCnt)+'</div></div>'
    +'</div>'
    +'<div class="fr" style="margin-bottom:.8rem">'
    +'<button class="btn btn-pri" onclick="addUserModal()">+ Add User</button>'
    +'<button class="btn btn-ok" onclick="dlUsers()">⬇ Export</button></div>'
    +'<div class="card"><div class="card-hdr"><b>All Users ('+list.length+')</b>'
      +'<div class="sbox" style="width:100%">&#128269; <input placeholder="Search..." style="width:85%" oninput="reloadUsers(this.value)"></div>'
    +'</div><div class="tbl-wrap"><table>'
    +'<thead><tr><th>#</th><th>Status</th><th>Name</th><th>Username</th><th>Phone</th><th>Password</th><th>Assigned Location</th><th>Submissions</th><th>Actions</th></tr></thead>'
    +'<tbody>'+rows+'</tbody></table></div></div>';
}

function reloadUsers(q){loadFromLocal();document.getElementById('mainContent').innerHTML=pgMUsers(q);}
function reloadAuditors(q){loadFromLocal();document.getElementById('mainContent').innerHTML=pgMAuditors(q);}
function togPwd(id){
  var el=document.getElementById('pw_'+id); if(!el) return;
  var a=auditorById(id); if(!a) return;
  el.dataset.shown=el.dataset.shown==='1'?'0':'1';
  el.textContent=el.dataset.shown==='1'?a.password:'••••••••';
  el.style.letterSpacing=el.dataset.shown==='1'?'normal':'2px';
}

// ═══════════ MASTER: AUDITOR ACCOUNTS ═══════════
function pgMAuditors(f){
  f=f||'';
  var list=f?AUDITORS.filter(function(a){return a.name.toLowerCase().indexOf(f.toLowerCase())!==-1;}):AUDITORS;
  var rows='';
  for(var i=0;i<list.length;i++){
    var a=list[i],subs=0; for(var k=0;k<STOCK.length;k++) if(STOCK[k].aud===a.name) subs++;
    rows+='<tr><td>'+a.id+'</td><td><b>'+a.name+'</b></td>'
      +'<td style="color:var(--acc)">'+a.username+'</td>'
      +'<td>'+(a.phone||'—')+'</td>'
      +'<td>'+(a.location||'—')+'</td>'
      +'<td><span class="badge b-info">'+subs+'</span></td>'
      +'<td><div class="fr" style="gap:4px">'
      +'<button class="btn btn-pri btn-sm" onclick="editUserModal('+a.id+')">✏</button>'
      +'<button class="btn btn-ghost btn-sm" style="color:var(--danger)" onclick="delUser('+a.id+')">Del</button>'
      +'</div></td></tr>';
  }
  return '<div class="fr" style="margin-bottom:.8rem"><button class="btn btn-pri" onclick="addUserModal()">+ Add Auditor</button></div>'
    +'<div class="card"><div class="card-hdr"><b>Auditor Accounts ('+list.length+')</b>'
      +'<div class="sbox" style="width:100%">&#128269; <input placeholder="Search..." style="width:85%" oninput="reloadAuditors(this.value)"></div>'
    +'</div><div class="tbl-wrap"><table>'
    +'<thead><tr><th>#</th><th>Name</th><th>Username</th><th>Phone</th><th>Location</th><th>Submissions</th><th>Actions</th></tr></thead>'
    +'<tbody>'+rows+'</tbody></table></div></div>';
}

// ═══════════ MASTER: DAILY REPORTS ═══════════
function pgMReports(selDate,selLoc){
  selDate=selDate||today();
  selLoc=selLoc||'';
  var locBtns='<button class="btn '+(selLoc===''?'btn-pri':'btn-ghost')+' btn-sm" onclick="pgMReportsFilter(\''+selDate+'\',\'\')">All</button>';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    var act=selLoc===String(m.id);
    locBtns+='<button class="btn '+(act?'btn-pri':'btn-ghost')+' btn-sm" onclick="pgMReportsFilter(\''+selDate+'\',\''+m.id+'\')">'+m.name+'</button>';
  }
  var items=STOCK.filter(function(s){
    if(s.date!==selDate) return false;
    if(selLoc&&String(s.mid)!==String(selLoc)) return false;
    return true;
  });
  var rows='';
  for(var i=0;i<items.length;i++){
    var s=items[i],ex=s.extra||{},m2=menuById(s.mid);
    var dc=(s.disc||0)<0?'var(--danger)':(s.disc||0)>0?'green':'var(--muted)';
    rows+='<tr>'
      +'<td>'+(m2?m2.name:'—')+'</td><td>'+s.sub+'</td>'
      +'<td style="font-weight:600">'+(ex.material||s.sku)+'</td>'
      +'<td>'+s.name+'</td>'
      +'<td style="text-align:center">'+s.sQty+'</td>'
      +'<td style="text-align:center;background:#fffde7">'+(s.pQty!==null?s.pQty:'—')+'</td>'
      +'<td style="text-align:center;color:'+dc+';font-weight:600">'+(s.disc!==null?s.disc:'—')+'</td>'
      +'<td>'+badge(s.st)+'</td>'
      +'<td><b>'+(s.aud||'—')+'</b></td>'
      +'<td style="font-size:11px">'+(s.time||'—')+'</td>'
      +'</tr>';
  }
  var empty='<tr><td colspan="10" style="text-align:center;padding:1.5rem;color:var(--muted)">No data for this date/location</td></tr>';
  return '<div class="fr" style="margin-bottom:.8rem;flex-wrap:wrap">'
    +'<input type="date" id="rptDate" value="'+selDate+'" style="padding:6px 10px;border:1px solid var(--border);border-radius:7px;font-size:13px" onchange="pgMReportsFilter(this.value,\''+selLoc+'\')">'
    +'<button class="btn btn-ok" onclick="dlReportExcel()">⬇ Download Report</button>'
    +'</div>'
    +'<div class="fr" style="margin-bottom:.8rem;gap:6px">'+locBtns+'</div>'
    +'<div class="ex-wrap"><div class="ex-hdr"> <span>Daily Report — '+selDate+(selLoc?' — '+(menuById(parseInt(selLoc))||{name:''}).name:'')+'</span>'
    +'<span style="margin-left:auto;font-size:11px;opacity:.7">'+items.length+' entries</span></div>'
    +'<div class="tbl-wrap"><table class="ex-tbl"><tr>'
    +'<th>Location</th><th>Sub Location</th><th>Material</th><th>Description</th>'
    +'<th>Sys Qty</th><th>Phy Qty</th><th>Variance</th><th>Status</th><th>Auditor</th><th>Time</th>'
    +'</tr>'+(rows||empty)+'</table></div></div>';
}

function pgMReportsFilter(d,l){
  document.getElementById('mainContent').innerHTML=pgMReports(d,l);
}

function dlReportExcel(){
  var d=document.getElementById('rptDate')?document.getElementById('rptDate').value:today();
  var items=STOCK.filter(function(s){return s.date===d;});
  var rows=[['Location','Sub Location','Material','Description','Plant','Sys Qty','Phy Qty','Variance','MAP/SPC','Stock Value','Disc Value','SAA Team','Remarks','Date','Time','Status','Auditor']];
  for(var i=0;i<items.length;i++){
    var s=items[i],ex=s.extra||{},m=menuById(s.mid);
    rows.push([m?m.name:'',s.sub,ex.material||s.sku,s.name,ex.plant||'',s.sQty,s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',ex.mapSpc||s.rate,s.amt,s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'',ex.saaTeam||s.aud||'',ex.remarks||'',s.date,s.time,s.st,s.aud||'']);
  }
  if(typeof XLSX!=='undefined'){
    var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);
    ws['!cols']=rows[0].map(function(h){return{wch:Math.max(String(h).length+2,12)};});
    XLSX.utils.book_append_sheet(wb,ws,'Report');
    XLSX.writeFile(wb,'daily_report_'+d+'.xlsx');
  }
}

// ═══════════ MASTER: TOTAL REPORT ═══════════
function pgMTotal(){
  var gTot=STOCK.length,gDone=0,gPend=0;
  for(var i=0;i<STOCK.length;i++) if(STOCK[i].st==='submitted') gDone++; else gPend++;
  var html='<div class="fr" style="margin-bottom:.8rem"><button class="btn btn-ok" onclick="dlExcel()">⬇ Download Full Report</button></div>'
    +'<div class="stat-row">'
    +'<div class="stat-card"><div class="lbl">Total Items</div><div class="val">'+gTot+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Audited</div><div class="val" style="color:var(--ok)">'+gDone+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Remaining</div><div class="val" style="color:var(--danger)">'+gPend+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Completion</div><div class="val" style="color:var(--pri)">'+(gTot?Math.round(gDone/gTot*100):0)+'%</div></div>'
    +'</div>';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    if(!m||!m.id) continue;
    if(!Array.isArray(m.subs)) m.subs=[];
    var mItems=STOCK.filter(function(s){return s.mid===m.id;}),mDone=0;
    for(var k=0;k<mItems.length;k++) if(mItems[k].st==='submitted') mDone++;
    var mPct=mItems.length?Math.round(mDone/mItems.length*100):0;
    var subRows='';
    for(var si=0;si<m.subs.length;si++){
      var nm=sn(m.subs[si]);
      var sItems=mItems.filter(function(s){return s.sub===nm;}),sDone=0;
      for(var k=0;k<sItems.length;k++) if(sItems[k].st==='submitted') sDone++;
      var sPct=sItems.length?Math.round(sDone/sItems.length*100):0;
      var barCol=sPct===100?'var(--ok)':sPct>50?'var(--pri)':'var(--warn)';
      subRows+='<tr><td>'+nm+'</td><td style="text-align:center">'+sItems.length+'</td>'
        +'<td style="text-align:center;color:var(--ok)">'+sDone+'</td>'
        +'<td style="text-align:center;color:var(--danger)">'+(sItems.length-sDone)+'</td>'
        +'<td style="text-align:center">'+sPct+'%</td>'
        +'<td><div style="background:#eee;border-radius:4px;height:8px;width:100px;overflow:hidden"><div style="background:'+barCol+';height:100%;width:'+sPct+'%"></div></div></td>'
        +'</tr>';
    }
    if(!m.subs.length) subRows='<tr><td colspan="6" style="text-align:center;color:var(--muted);padding:.8rem">No sub locations</td></tr>';
    html+='<div class="card" style="margin-bottom:.8rem"><div class="card-hdr">'
      +'<b>'+m.name+'</b>'
      +'<div class="fr" style="gap:10px">'
      +'<span style="font-size:12px;color:var(--muted)">'+mDone+'/'+mItems.length+'</span>'
      +'<div style="background:#eee;border-radius:5px;height:10px;width:120px;overflow:hidden"><div style="background:'+(mPct===100?'var(--ok)':mPct>50?'var(--pri)':'var(--warn)')+';height:100%;width:'+mPct+'%"></div></div>'
      +'<b style="color:var(--pri)">'+mPct+'%</b>'
      +'</div></div>'
      +'<div class="tbl-wrap"><table><thead><tr><th>Sub Location</th><th>Total</th><th>Audited</th><th>Remaining</th><th>% Done</th><th>Progress</th></tr></thead>'
      +'<tbody>'+subRows+'</tbody></table></div></div>';
  }
  return html;
}

// ═══════════ MASTER: PROGRESS CHART ═══════════
function pgMChart(){
  var tot=STOCK.length,done=0,proc=0,pend=0;
  for(var i=0;i<STOCK.length;i++){if(STOCK[i].st==='submitted')done++;else if(STOCK[i].st==='process')proc++;else pend++;}
  var pct=tot?Math.round(done/tot*100):0;
  var storeCharts='';
  for(var mi=0;mi<MENUS.length;mi++){
    var m=MENUS[mi];
    if(!m||!m.id) continue;
    var mt=0,md=0,mp=0,mr=0;
    for(var k=0;k<STOCK.length;k++){if(STOCK[k].mid===m.id){mt++;if(STOCK[k].st==='submitted')md++;else if(STOCK[k].st==='process')mp++;else mr++;}}
    var mp2=mt?Math.round(md/mt*100):0;
    storeCharts+='<div style="text-align:center;min-width:130px">'
      +'<div style="position:relative;width:100px;height:100px;margin:0 auto">'
      +'<canvas id="sc'+m.id+'" width="100" height="100"></canvas>'
      +'<div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);font-size:16px;font-weight:700;color:var(--pri)">'+mp2+'%</div>'
      +'</div>'
      +'<div style="font-size:12px;font-weight:600;margin-top:.4rem">'+m.name+'</div>'
      +'<div style="font-size:11px;color:var(--muted)">'+md+'/'+mt+'</div>'
      +'<script>(function(){'
      +'var c=document.getElementById("sc'+m.id+'");if(!c)return;'
      +'var ctx=c.getContext("2d");'
      +'var segs=[{v:'+md+',col:"#06d6a0"},{v:'+mp+',col:"#f4a261"},{v:'+mr+',col:"#dde3ef"}];'
      +'var tot='+mt+';if(!tot){ctx.beginPath();ctx.arc(50,50,40,0,2*Math.PI);ctx.fillStyle="#eee";ctx.fill();ctx.beginPath();ctx.arc(50,50,26,0,2*Math.PI);ctx.fillStyle="#fff";ctx.fill();return;}'
      +'var start=-Math.PI/2;'
      +'for(var i=0;i<segs.length;i++){if(!segs[i].v)continue;var ang=(segs[i].v/tot)*2*Math.PI;ctx.beginPath();ctx.moveTo(50,50);ctx.arc(50,50,45,start,start+ang);ctx.closePath();ctx.fillStyle=segs[i].col;ctx.fill();start+=ang;}'
      +'ctx.beginPath();ctx.arc(50,50,29,0,2*Math.PI);ctx.fillStyle="#fff";ctx.fill();'
      +'})();<\/script>'
      +'</div>';
  }
  return '<div style="max-width:800px">'
    +'<div class="card" style="margin-bottom:1rem"><div class="card-hdr"><b>Overall Audit Progress</b></div>'
    +'<div style="display:flex;align-items:center;justify-content:center;gap:2rem;flex-wrap:wrap;padding:1.5rem">'
    +'<div style="position:relative;width:180px;height:180px;flex-shrink:0">'
    +'<canvas id="mainDonut" width="180" height="180"></canvas>'
    +'<div style="position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);text-align:center">'
    +'<div style="font-size:32px;font-weight:700;color:var(--pri)">'+pct+'%</div>'
    +'<div style="font-size:11px;color:var(--muted)">Completed</div>'
    +'</div></div>'
    +'<div style="display:flex;flex-direction:column;gap:.7rem;min-width:200px">'
    +'<div class="fr"><div style="width:12px;height:12px;border-radius:50%;background:#06d6a0;flex-shrink:0"></div><div><b>Submitted:</b> '+done+' ('+pct+'%)</div></div>'
    +'<div class="fr"><div style="width:12px;height:12px;border-radius:50%;background:#f4a261;flex-shrink:0"></div><div><b>In Process:</b> '+proc+'</div></div>'
    +'<div class="fr"><div style="width:12px;height:12px;border-radius:50%;background:#dde3ef;flex-shrink:0"></div><div><b>Pending:</b> '+pend+'</div></div>'
    +'<div style="border-top:1px solid var(--border);padding-top:.5rem"><b>Total:</b> '+tot+' items | Remaining: <b style="color:var(--danger)">'+(tot-done)+'</b></div>'
    +'</div></div>'
    +'<script>(function(){'
    +'var c=document.getElementById("mainDonut");if(!c)return;'
    +'var ctx=c.getContext("2d");'
    +'var segs=[{v:'+done+',col:"#06d6a0"},{v:'+proc+',col:"#f4a261"},{v:'+pend+',col:"#dde3ef"}];'
    +'var tot='+tot+';if(!tot){ctx.beginPath();ctx.arc(90,90,70,0,2*Math.PI);ctx.fillStyle="#eee";ctx.fill();return;}'
    +'var start=-Math.PI/2;'
    +'for(var i=0;i<segs.length;i++){if(!segs[i].v)continue;var ang=(segs[i].v/tot)*2*Math.PI;ctx.beginPath();ctx.moveTo(90,90);ctx.arc(90,90,80,start,start+ang);ctx.closePath();ctx.fillStyle=segs[i].col;ctx.fill();start+=ang;}'
    +'ctx.beginPath();ctx.arc(90,90,52,0,2*Math.PI);ctx.fillStyle="#fff";ctx.fill();'
    +'})();<\/script>'
    +'</div>'
    +'<div class="card"><div class="card-hdr"><b>Per Location Progress</b></div>'
    +'<div style="display:flex;gap:1.5rem;flex-wrap:wrap;justify-content:center;padding:1rem">'+storeCharts+'</div></div>'
    +'<button class="btn btn-pri" style="width:100%;margin-top:.8rem" onclick="go(\'mTotal\')">Vieww Full Total Report</button>'
    +'</div>';
}

// ═══════════ AUDITOR: DASHBOARD ═══════════
function pgADash(){
  var mine=STOCK.filter(function(s){return s.aud===CU.name;}),sub=0,pro=0;
  for(var i=0;i<mine.length;i++){if(mine[i].st==='submitted')sub++;else if(mine[i].st==='process')pro++;}
  var pen=0; for(var i=0;i<STOCK.length;i++) if(STOCK[i].st==='pending') pen++;
  return '<div class="stat-row">'
    +'<div class="stat-card"><div class="lbl">My Submissions</div><div class="val" style="color:var(--ok)">'+sub+'</div></div>'
    +'<div class="stat-card"><div class="lbl">In Process</div><div class="val" style="color:var(--warn)">'+pro+'</div></div>'
    +'<div class="stat-card"><div class="lbl">Pending Items</div><div class="val" style="color:var(--muted)">'+pen+'</div></div>'
    +'</div>'
    +'<div class="card"><div class="card-hdr"><b>Recent Activity</b>'
    +'<button class="btn btn-pri btn-sm" onclick="go(\'aLoc\')">+ Enter Stock</button>'
    +'</div><div class="tbl-wrap">'+tbl(mine.slice(-5),false,false)+'</div></div>';
}

// ═══════════ AUDITOR: LOCATION ═══════════
function pgALoc(){
  var menuList=CU.assignedMenuId?MENUS.filter(function(m){return m.id===CU.assignedMenuId;}):MENUS;
  var note=CU.assignedMenuId?'<div style="background:var(--b-info,#e6f1fb);border:1px solid #b5d4f4;border-radius:8px;padding:.6rem 1rem;margin-bottom:.8rem;font-size:12px;color:#0C447C"> You are assigned to: <b>'+(menuById(CU.assignedMenuId)||{name:'Unknown'}).name+'</b></div>':'';
  var h='<h3 style="font-size:15px;color:var(--pri);margin-bottom:.5rem">Select Location</h3>'+note+'<div>';
  for(var mi=0;mi<menuList.length;mi++){
    var m=menuList[mi];
    if(!m||!m.id) continue;
    if(!Array.isArray(m.subs)) m.subs=[];
    var tPen=0,tDone=0;
    for(var k=0;k<STOCK.length;k++){if(STOCK[k].mid===m.id){if(STOCK[k].st==='pending')tPen++;else if(STOCK[k].st==='submitted')tDone++;}}
    var cards='';
    for(var si=0;si<m.subs.length;si++){
      var sm=m.subs[si]; if(!sm) continue;
      var nm=sn(sm),pen=0,done2=0;
      for(var k=0;k<STOCK.length;k++){if(STOCK[k].mid===m.id&&STOCK[k].sub===nm){if(STOCK[k].st==='pending')pen++;else if(STOCK[k].st==='submitted')done2++;}}
      var enc=encodeURIComponent(nm);
      cards+='<div style="background:var(--bg);border:1px solid var(--border);border-radius:10px;padding:.8rem 1rem;display:flex;align-items:center;justify-content:space-between;cursor:pointer;margin-bottom:.4rem;transition:background .15s" '
        +'onmouseover="this.style.background=\'#ede7ff\'" onmouseout="this.style.background=\'var(--bg)\'" '
        +'onclick="openSubEntry('+m.id+',decodeURIComponent(\''+enc+'\'))">'
        +'<div><div style="font-size:13px;font-weight:600">'+nm+'</div>'
        +'<div style="font-size:11px;color:var(--muted);margin-top:2px">'+(pen+done2)+' total items</div></div>'
        +'<div class="fr" style="gap:6px">'
        +(pen>0?'<span class="badge b-warn">'+pen+' pending</span>':'')
        +(done2>0?'<span class="badge b-ok">'+done2+' done</span>':'')
        +'<span style="font-size:18px;color:var(--pri)">›</span></div></div>';
    }
    if(!cards) cards='<p style="font-size:12px;color:var(--muted);padding:.5rem">No sub locations yet</p>';
    h+='<div class="acc" style="margin-bottom:.5rem">'
      +'<div class="acc-hdr" onclick="togAcc(this)" style="background:linear-gradient(90deg,var(--pri),var(--pri2));color:#fff;border-radius:10px">'
      +'<div class="fr" style="gap:8px"><span class="arr" style="color:#fff">▶</span>'
      +'<b style="color:#fff">'+m.name+'</b>'
      +'<span style="background:rgba(255,255,255,.2);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+m.subs.length+' sub locations</span>'
      +(tPen>0?'<span style="background:rgba(244,162,97,.4);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+tPen+' pending</span>':'')
      +(tDone>0?'<span style="background:rgba(6,214,160,.3);color:#fff;padding:2px 8px;border-radius:20px;font-size:11px">'+tDone+' done</span>':'')
      +'</div><span style="font-size:11px;color:rgba(255,255,255,.6)">Click to expand</span>'
      +'</div>'
      +'<div class="acc-body" style="padding:.6rem">'+cards+'</div>'
      +'</div>';
  }
  return h+'</div>';
}

function openSubEntry(mid,subName){
  loadFromLocal();
  if(!menuById(mid)){alert('Location not found');go('aLoc');return;}
  PAGE='aStock';
  document.getElementById('pageTitle').textContent=subName+' — Stock Entry';
  document.getElementById('mainContent').innerHTML=subEntryPage(mid,subName);
}

function subEntryPage(mid,subName){
  var m=menuById(mid);
  if(m&&!Array.isArray(m.subs)) m.subs=[];
  var sm=null; if(m) for(var i=0;i<m.subs.length;i++) if(sn(m.subs[i])===subName){sm=m.subs[i];break;}
  var cols=sm?sc(sm):ECOLS;
  var items=STOCK.filter(function(s){return s.mid===mid&&s.sub===subName;});
  // Search bar
      +'<div class="sbox" style="width:100%">&#128269; <input placeholder="Search..." style="width:85%" oninput="reloadAuditors(this.value)"></div>'
    +'<input id="subSrch" placeholder="Search material, description..." style="width:80%" oninput="filterSubTable(this.value)">'
    +'</div>';
  var thCells='<th>#</th>'+cols.map(function(c){return '<th>'+c+'</th>';}).join('')+'<th>Status</th><th>Action</th>';
  var rows='';
  for(var i=0;i<items.length;i++){
    var s=items[i],ex=s.extra||{};
    var tds='';
    for(var j=0;j<cols.length;j++){
      var c=cols[j].toLowerCase().trim();
      if(c==='physical quantity'){
        // Check if locked by master
        var m2=menuById(mid),siIdx=-1;
        if(m2) for(var q=0;q<m2.subs.length;q++) if(sn(m2.subs[q])===subName){siIdx=q;break;}
        var phyLocked=siIdx>=0&&isLocked(mid,siIdx,cols[j]);
        if(phyLocked){
          tds+='<td style="text-align:center;background:#ffeaea;color:var(--danger)" title="Locked by master">Locked: '+(s.pQty!==null?s.pQty:'—')+'</td>';
        } else {
          tds+='<td class="editable" contenteditable="true" oninput="upQty('+s.id+',this.textContent.trim())" style="min-width:80px;text-align:center">'+(s.pQty!==null?s.pQty:'')+'</td>';
        }
      } else if(c==='quantity variance'){
        var qvc=(s.disc||0)<0?'var(--danger)':(s.disc||0)>0?'green':'var(--muted)';
        tds+='<td id="qv'+s.id+'" style="text-align:center;color:'+qvc+';font-weight:700">'+(s.disc!==null?s.disc:'—')+'</td>';
      } else if(c==='discrepancy value'){
        var dv=s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)):null;
        tds+='<td id="dv'+s.id+'" style="text-align:right;color:'+(dv!==null&&dv<0?'var(--danger)':dv>0?'green':'var(--muted)')+'">'+(dv!==null?dv.toFixed(2):'—')+'</td>';
      } else if(c==='saa team'){
        tds+='<td class="editable" contenteditable="true" onblur="upExtra('+s.id+',\'saaTeam\',this.textContent.trim())" style="min-width:100px;background:#fffde7;cursor:text" title="Click to enter">'+(ex.saaTeam||s.aud||'')+'</td>';
      } else if(c==='remarks'){
        tds+='<td class="editable" contenteditable="true" onblur="upExtra('+s.id+',\'remarks\',this.textContent.trim())" style="min-width:120px;background:#fffde7;cursor:text" title="Click to enter">'+(ex.remarks||'')+'</td>';
      } else if(c==='date'){
        tds+='<td id="dt'+s.id+'" style="text-align:center;min-width:80px">'+(s.date||'—')+'</td>';
      } else if(c==='time'){
        tds+='<td id="tm'+s.id+'" style="text-align:center">'+(s.time||'—')+'</td>';
      } else if(c==='sl.no'){
        tds+='<td style="text-align:center;color:var(--muted)">'+s.id+'</td>';
      } else if(c==='material'){
        tds+='<td style="font-weight:600">'+(ex.material||s.sku||'—')+'</td>';
      } else if(c==='description'){
        tds+='<td>'+s.name+'</td>';
      } else if(c==='plant'){
        tds+='<td>'+(ex.plant||'—')+'</td>';
      } else if(c==='storage location'){
        tds+='<td>'+s.sub+'</td>';
      } else if(c==='unrestricted stock'){
        tds+='<td style="text-align:center">'+s.sQty+'</td>';
      } else if(c==='storage bin'){
        tds+='<td>'+(ex.storageBin||'—')+'</td>';
      } else if(c==='map/spc'){
        tds+='<td style="text-align:right">'+(ex.mapSpc||s.rate||'—')+'</td>';
      } else if(c==='stock values'){
        tds+='<td style="text-align:right">'+s.amt.toLocaleString()+'</td>';
      } else {
        tds+='<td>—</td>';
      }
    }
    var enc2=encodeURIComponent(subName);
    var act=(s.st==='pending'||s.st==='process')
      ?'<td><div class="fr" style="gap:4px">'
        +'<button class="btn btn-warn btn-sm" onclick="setPro('+s.id+')">Process</button>'
        +'<button class="btn btn-sub btn-sm" onclick="submitItem('+s.id+','+mid+',decodeURIComponent(\''+enc2+'\'))">Submit</button>'
        +'</div></td>'
      :'<td><span class="badge b-ok">Done</span></td>';
    rows+='<tr id="row'+s.id+'" style="transition:background .3s"><td>'+s.id+'</td>'+tds+'<td>'+badge(s.st)+'</td>'+act+'</tr>';
  }
  var empty=items.length===0?'<tr><td colspan="'+(cols.length+3)+'" style="text-align:center;padding:1.5rem;color:var(--muted)">No items — master needs to upload data for this sub location</td></tr>':'';
  return '<div class="fr" style="margin-bottom:.8rem">'
    +'<button class="btn btn-ghost" onclick="go(\'aLoc\')">← Back</button>'
    +'<span style="font-size:13px;color:var(--muted)">'+(m?m.name:'')+'  ›  <b style="color:var(--pri)">'+subName+'</b></span>'
    +'</div>'
    +'<div class="ex-wrap"><div class="ex-hdr"> <span>'+subName+' — Stock Entry (yellow cells = enter physical qty)</span></div>'
    +'<div style="padding:.5rem .8rem;background:#f0f9f0;border-bottom:1px solid #b8c9a3">'+searchBar+'</div>'
    +'<div class="tbl-wrap" id="subTableWrap"><table class="ex-tbl" id="subTable"><tr>'+thCells+'</tr>'+rows+empty+'</table></div>'
    +'</div>';
}

function filterSubTable(q){
  var rows=document.querySelectorAll('#subTable tr');
  for(var i=1;i<rows.length;i++){
    var txt=rows[i].textContent.toLowerCase();
    rows[i].style.display=!q||txt.indexOf(q.toLowerCase())!==-1?'':'none';
  }
}

function upQty(id,val){
  var s=stockById(id); if(!s) return;
  var q=parseFloat(val); if(isNaN(q)||val==='') return;
  s.pQty=q; s.disc=q-s.sQty; s.aud=CU.name;
  s.date=today(); s.time=nowTime();
  if(!s.extra) s.extra={};
  if(!s.extra.saaTeam) s.extra.saaTeam=CU.name;
  var qv=document.getElementById('qv'+id);
  if(qv){qv.textContent=s.disc;qv.style.color=s.disc<0?'var(--danger)':s.disc>0?'green':'var(--muted)';}
  var mapSpc=parseFloat((s.extra&&s.extra.mapSpc)||s.rate)||0;
  var discVal=s.disc*mapSpc;
  var dv=document.getElementById('dv'+id);
  if(dv){dv.textContent=discVal.toFixed(2);dv.style.color=discVal<0?'var(--danger)':discVal>0?'green':'var(--muted)';}
  var dt=document.getElementById('dt'+id); if(dt) dt.textContent=s.date;
  var tm=document.getElementById('tm'+id); if(tm) tm.textContent=s.time;
  var row=document.getElementById('row'+id);
  if(row) row.style.background=s.disc===0?'#f0fff8':s.disc<0?'#fff5f5':'#f5fff0';
  saveToLocal();
}

function upExtra(id,field,val){
  var s=stockById(id); if(!s) return;
  if(!s.extra) s.extra={};
  s.extra[field]=val;
  saveToLocal();
}

function setPro(id){
  var s=stockById(id); if(!s) return;
  s.st='process'; s.aud=CU.name; s.date=today(); s.time=nowTime();
  saveToLocal(); go(PAGE);
}

function submitItem(id,mid,subName){
  var s=stockById(id); if(!s) return;
  if(s.pQty===null){alert('Please enter physical quantity first!');return;}
  s.st='submitted'; s.aud=CU.name; s.date=today(); s.time=nowTime();
  if(!s.extra) s.extra={}; if(!s.extra.saaTeam) s.extra.saaTeam=CU.name;
  saveToLocal();
  // Flash green row briefly
  var row=document.getElementById('row'+id);
  if(row){row.style.background='#c8f7e0';setTimeout(function(){if(document.getElementById('row'+id))document.getElementById('mainContent').innerHTML=subEntryPage(mid,subName);},400);}
  else document.getElementById('mainContent').innerHTML=subEntryPage(mid,subName);
}

function pgAHistory(){
  var mine=STOCK.filter(function(s){return s.aud===CU.name;});
  return '<div class="fr" style="margin-bottom:.8rem"><button class="btn btn-ok" onclick="dlMyReport()">⬇ My Report</button></div>'
    +'<div class="card"><div class="card-hdr"><b>My Submissions ('+mine.length+')</b></div>'
    +'<div class="tbl-wrap">'+tbl(mine,false,false)+'</div></div>';
}

// ═══════════ STOCK CRUD ═══════════
function addStkModal(){
  var opts=MENUS.map(function(m){return '<option value="'+m.id+'">'+m.name+'</option>';}).join('');
  modal('Add Stock Item',
    fg('Item Name','<input id="ns_n" placeholder="Item name">')+
    fg('Material/SKU','<input id="ns_s" placeholder="Material code">')+
    fg('Location','<select id="ns_m">'+opts+'</select>')+
    fg('Sub Location','<input id="ns_sm" placeholder="Sub location">')+
    fg('System Qty','<input type="number" id="ns_q" placeholder="0">')+
    fg('MAP/SPC Rate','<input type="number" id="ns_r" placeholder="0">'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveStkAdd()">Add</button>');
}

function saveStkAdd(){
  var n=document.getElementById('ns_n').value,s=document.getElementById('ns_s').value;
  if(!n||!s){alert('Name and Material required');return;}
  var q=parseInt(document.getElementById('ns_q').value)||0;
  var r=parseFloat(document.getElementById('ns_r').value)||0;
  STOCK.push({id:nextSID++,mid:parseInt(document.getElementById('ns_m').value),sub:document.getElementById('ns_sm').value,name:n,sku:s,sQty:q,pQty:null,disc:null,rate:r,amt:q*r,st:'pending',aud:'',date:'',time:'',extra:{material:s,plant:'',storageBin:'',mapSpc:r,purGroup:'',purGroupDes:'',saaTeam:'',remarks:''}});
  saveToLocal(); closeModal(); go(PAGE);
}

function editStk(id){
  var s=stockById(id); if(!s) return;
  var opts=MENUS.map(function(m){return '<option value="'+m.id+'"'+(m.id===s.mid?' selected':'')+'>'+m.name+'</option>';}).join('');
  var stOpts=['pending','process','submitted'].map(function(v){return '<option value="'+v+'"'+(v===s.st?' selected':'')+'>'+v+'</option>';}).join('');
  modal('Edit Stock Item',
    fg('Item Name','<input id="ei_n" value="'+s.name+'">')+
    fg('Material','<input id="ei_s" value="'+s.sku+'">')+
    fg('Location','<select id="ei_m">'+opts+'</select>')+
    fg('Sub Location','<input id="ei_sm" value="'+s.sub+'">')+
    fg('System Qty','<input type="number" id="ei_q" value="'+s.sQty+'">')+
    fg('Rate','<input type="number" id="ei_r" value="'+s.rate+'">')+
    fg('Status','<select id="ei_st">'+stOpts+'</select>'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveStkEdit('+id+')">Save</button>');
}

function saveStkEdit(id){
  var s=stockById(id);
  s.name=document.getElementById('ei_n').value; s.sku=document.getElementById('ei_s').value;
  s.mid=parseInt(document.getElementById('ei_m').value); s.sub=document.getElementById('ei_sm').value;
  s.sQty=parseInt(document.getElementById('ei_q').value)||0; s.rate=parseFloat(document.getElementById('ei_r').value)||0;
  s.amt=s.sQty*s.rate; s.st=document.getElementById('ei_st').value;
  if(s.extra) s.extra.material=s.sku;
  saveToLocal(); closeModal(); go(PAGE);
}

function delStk(id){
  if(!confirm('Delete this item?')) return;
  for(var i=0;i<STOCK.length;i++) if(STOCK[i].id===id){STOCK.splice(i,1);break;}
  saveToLocal(); go(PAGE);
}

// ═══════════ LOCATION CRUD ═══════════
function addLocModal(){
  modal('Add Location',fg('Location Name','<input id="nl_n" placeholder="e.g. New Store">'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveLocAdd()">Add</button>');
}
function saveLocAdd(){var n=document.getElementById('nl_n').value.trim();if(!n)return;MENUS.push({id:nextMID++,name:n,subs:[]});saveToLocal();closeModal();go(PAGE);}
function editLocModal(id){
  var m=menuById(id); if(!m){alert('Location not found');return;}
  modal('Edit Location',fg('Location Name','<input id="el_n" value="'+m.name+'">'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveLocEdit('+id+')">Save</button>');
}
function saveLocEdit(id){var m=menuById(id);if(!m)return;m.name=document.getElementById('el_n').value.trim();saveToLocal();closeModal();go(PAGE);}
function delLoc(id){if(!confirm('Delete this location?'))return;for(var i=0;i<MENUS.length;i++) if(MENUS[i].id===id){MENUS.splice(i,1);break;}saveToLocal();go(PAGE);}

function addSubModal(mid){
  if(!menuById(mid)){alert('Location not found');return;}
  modal('Add Sub Location',fg('Sub Location Name','<input id="ns_nm" placeholder="Sub location name">'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveSubAdd('+mid+')">Add</button>');
}
function saveSubAdd(mid){
  var n=document.getElementById('ns_nm').value.trim(); if(!n) return;
  var m=menuById(mid); if(!m)return;
  m.subs.push({name:n,cols:ECOLS.slice()});
  // Lock all columns by default - auditors can only edit unlocked ones
  for(var i=0;i<ECOLS.length;i++) LOCKED_COLS['L'+mid+'_'+n+'_'+ECOLS[i]]=true;
  // Unlock only Physical Quantity, SAA Team, Remarks by default
  var editableCols=['Physical Quantity','SAA Team','Remarks'];
  for(var i=0;i<editableCols.length;i++) delete LOCKED_COLS['L'+mid+'_'+n+'_'+editableCols[i]];
  saveToLocal(); closeModal(); go(PAGE);
}
function delSub(mid,idx){var m=menuById(mid);if(!m)return;if(!confirm('Delete sub location "'+sn(m.subs[idx])+'"?'))return;m.subs.splice(idx,1);saveToLocal();go(PAGE);}

function lockAllCols(mid,subName){
  var m=menuById(mid); if(!m) return;
  var sm=null; for(var i=0;i<m.subs.length;i++) if(sn(m.subs[i])===subName){sm=m.subs[i];break;}
  var cols=sm?sc(sm):ECOLS;
  for(var i=0;i<cols.length;i++) LOCKED_COLS['L'+mid+'_'+subName+'_'+cols[i]]=true;
  saveToLocal(); go(PAGE);
}

function unlockAllCols(mid,subName){
  var m=menuById(mid); if(!m) return;
  var sm=null; for(var i=0;i<m.subs.length;i++) if(sn(m.subs[i])===subName){sm=m.subs[i];break;}
  var cols=sm?sc(sm):ECOLS;
  for(var i=0;i<cols.length;i++) delete LOCKED_COLS['L'+mid+'_'+subName+'_'+cols[i]];
  saveToLocal(); go(PAGE);
}

function toggleLockByName(mid,subName,col){
  var key='L'+mid+'_'+subName+'_'+col;
  LOCKED_COLS[key]=!LOCKED_COLS[key];
  if(!LOCKED_COLS[key]) delete LOCKED_COLS[key]; // clean up false entries
  saveToLocal();
  go(PAGE);
}

function isLockedByName(mid,subName,col){
  return !!LOCKED_COLS['L'+mid+'_'+subName+'_'+col];
}

function toggleLock(mid,idx,col){
  var m=menuById(mid); if(!m||!m.subs[idx]) return;
  var subName=sn(m.subs[idx]);
  toggleLockByName(mid,subName,col);
}

function isLocked(mid,idx,col){
  var m=menuById(mid); if(!m||!m.subs[idx]) return false;
  return isLockedByName(mid,sn(m.subs[idx]),col);
}

function editSubCols(mid,idx){
  var m=menuById(mid); if(!m||!m.subs||!m.subs[idx]){alert('Sub location not found');return;} var sm=m.subs[idx],cols=sc(sm);
  modal('Edit Columns — '+sn(sm),
    fg('Columns (comma separated)','<textarea id="ec_c" style="height:80px">'+cols.join(', ')+'</textarea>'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveSubCols('+mid+','+idx+')">Save</button>');
}
function saveSubCols(mid,idx){
  var m=menuById(mid); if(!m)return; var raw=document.getElementById('ec_c').value;
  var cols=raw.split(',').map(function(c){return c.trim();}).filter(Boolean);
  if(typeof m.subs[idx]==='object') m.subs[idx].cols=cols;
  else m.subs[idx]={name:m.subs[idx],cols:cols};
  saveToLocal(); closeModal(); go(PAGE);
}

function openSubUpload(mid,idx){
  var m=menuById(mid); if(!m||!m.subs||m.subs[idx]===undefined){alert('Sub location not found');return;} var nm=sn(m.subs[idx]),fid='sf_'+mid+'_'+idx;
  modal('Upload Excel — '+nm,
    '<div class="upzone" onclick="document.getElementById(\''+fid+'\').click()">'
    +'<div style="font-size:28px"></div>'
    +'<b style="color:var(--pri)">Click to Upload Excel</b>'
    +'<p style="font-size:11px;color:var(--muted)">.xlsx, .xls</p></div>'
    +'<input type="file" id="'+fid+'" accept=".xlsx,.xls" style="display:none" onchange="handleSubUpload(event,'+mid+','+idx+')">'
    +'<div id="sup_'+fid+'"></div>',
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button>');
}

function handleSubUpload(ev,mid,idx){
  var f=ev.target.files[0]; if(!f) return;
  var fid='sf_'+mid+'_'+idx,r=new FileReader();
  r.onload=function(e){
    try{
      var wb=XLSX.read(e.target.result,{type:'binary'});
      var ws=wb.Sheets[wb.SheetNames[0]];
      var data=XLSX.utils.sheet_to_json(ws,{header:1,defval:''});
      if(!data||data.length<2){alert('File empty!');return;}
      var hdrs=data[0].map(function(h){return String(h).trim();});
      var hdrLow=hdrs.map(function(h){return h.toLowerCase();});
      var svIdx=hdrLow.indexOf('stock values'); if(svIdx===-1) svIdx=hdrLow.indexOf('stock value');
      var totalVal=0,count=data.length-1;
      if(svIdx!==-1) for(var i=1;i<data.length;i++) totalVal+=parseFloat(String(data[i][svIdx]).replace(/,/g,''))||0;
      var previewRows=data.slice(1,4).map(function(row){return '<tr>'+row.map(function(c){return '<td>'+c+'</td>';}).join('')+'</tr>';}).join('');
      var encoded=encodeURIComponent(JSON.stringify(data));
      var prev=document.getElementById('sup_'+fid);
      if(prev) prev.innerHTML=
        '<div class="fr" style="margin:.6rem 0;gap:10px">'
        +'<div class="stat-card" style="flex:1;padding:.6rem .8rem"><div class="lbl">Line Items</div><div class="val" style="font-size:18px">'+count+'</div></div>'
        +(svIdx!==-1?'<div class="stat-card" style="flex:1;padding:.6rem .8rem"><div class="lbl">Total Stock Value</div><div class="val" style="font-size:14px">₹'+totalVal.toLocaleString()+'</div></div>':'')
        +'</div>'
        +'<div class="ex-wrap" style="margin-bottom:.6rem"><div class="ex-hdr"> <span>'+f.name+' — '+count+' rows</span></div>'
        +'<div class="tbl-wrap"><table class="ex-tbl"><tr>'+hdrs.map(function(h){return '<th>'+h+'</th>';}).join('')+'</tr>'+previewRows+'</table></div></div>'
        +'<button class="btn btn-ok" style="width:100%" onclick="saveSubExcel('+mid+','+idx+',decodeURIComponent(this.dataset.d))" data-d="'+encoded+'">💾 Save to Stock</button>';
    }catch(err){alert('Error: '+err.message);}
  };
  r.readAsBinaryString(f);
}

function saveSubExcel(mid,idx,encoded){
  var m=menuById(mid); if(!m||!m.subs||m.subs[idx]===undefined)return; var nm=sn(m.subs[idx]);
  var data=JSON.parse(encoded);
  var hdrs=data[0].map(function(h){return String(h).trim().toLowerCase();}),added=0;
  for(var i=1;i<data.length;i++){
    var row={};
    hdrs.forEach(function(h,j){row[h]=data[i][j]!==undefined?String(data[i][j]).trim():'';});
    if(!row['material']&&!row['description']&&!row['item name']) continue;
    var sQty=parseFloat(row['unrestricted stock']||row['system qty']||row['qty']||0)||0;
    var mapSpc=parseFloat(row['map/spc']||row['rate']||0)||0;
    var stockVal=parseFloat(row['stock values']||row['stock value']||0)||sQty*mapSpc;
    STOCK.push({id:nextSID++,mid:mid,sub:nm,name:row['description']||row['item name']||('Item '+nextSID),sku:row['material']||row['sku']||('MAT'+nextSID),sQty:sQty,pQty:null,disc:null,rate:mapSpc,amt:stockVal,st:'pending',aud:'',date:'',time:'',extra:{material:row['material']||'',plant:row['plant']||'',storageBin:row['storage bin']||'',mapSpc:mapSpc,purGroup:row['pur.group']||'',purGroupDes:row['pur.group des']||'',saaTeam:'',remarks:row['remarks']||''}});
    added++;
  }
  // Lock all cols except editable ones after upload
  var editableCols2=['Physical Quantity','SAA Team','Remarks'];
  for(var ci=0;ci<ECOLS.length;ci++){
    var ck='L'+mid+'_'+nm+'_'+ECOLS[ci];
    if(editableCols2.indexOf(ECOLS[ci])===-1) LOCKED_COLS[ck]=true;
    else delete LOCKED_COLS[ck];
  }
  saveToLocal();
  closeModal(); alert(added+' items added to '+nm); go(PAGE);
}

// ═══════════ USER CRUD ═══════════
function addUserModal(){
  var opts='<option value="">-- All Locations --</option>'+MENUS.map(function(m){return '<option value="'+m.id+'">'+m.name+'</option>';}).join('');
  modal('Add New User',
    fg('Full Name','<input id="nu_n" placeholder="Full name">')+
    fg('Username','<input id="nu_u" placeholder="e.g. auditor41">')+
    fg('Password','<input id="nu_p" placeholder="e.g. Audit@41">')+
    fg('Phone (for OTP)','<input id="nu_ph" type="tel" placeholder="Phone number">')+
    fg('Assign Location','<select id="nu_mid">'+opts+'</select>'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveUserAdd()">Add User</button>');
}
function saveUserAdd(){
  var n=document.getElementById('nu_n').value.trim(),u=document.getElementById('nu_u').value.trim(),p=document.getElementById('nu_p').value.trim();
  if(!n||!u||!p){alert('Name, username and password required');return;}
  for(var i=0;i<AUDITORS.length;i++) if(AUDITORS[i].username===u){alert('Username exists!');return;}
  var mid=document.getElementById('nu_mid').value;
  AUDITORS.push({id:nextAID++,username:u,password:p,name:n,phone:document.getElementById('nu_ph').value.trim(),location:'',assignedMenuId:mid?parseInt(mid):null,lastLogin:''});
  saveToLocal(); closeModal(); go(PAGE);
}

function editUserModal(id){
  var a=auditorById(id); if(!a) return;
  var opts='<option value="">-- All Locations --</option>'+MENUS.map(function(m){return '<option value="'+m.id+'"'+(a.assignedMenuId===m.id?' selected':'')+'>'+m.name+'</option>';}).join('');
  modal('Edit User — '+a.name,
    fg('Full Name','<input id="eu_n" value="'+a.name+'">')+
    fg('Username','<input id="eu_u" value="'+a.username+'">')+
    fg('Password','<input id="eu_p" value="'+a.password+'">')+
    fg('Phone','<input id="eu_ph" type="tel" value="'+(a.phone||'')+'">')+
    fg('Assign Location','<select id="eu_mid">'+opts+'</select>'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveUserEdit('+id+')">Save</button>');
}
function saveUserEdit(id){
  var a=auditorById(id),nu=document.getElementById('eu_u').value.trim();
  for(var i=0;i<AUDITORS.length;i++) if(AUDITORS[i].username===nu&&AUDITORS[i].id!==id){alert('Username taken!');return;}
  a.name=document.getElementById('eu_n').value.trim(); a.username=nu;
  a.password=document.getElementById('eu_p').value.trim();
  a.phone=document.getElementById('eu_ph').value.trim();
  var mid=document.getElementById('eu_mid').value;
  a.assignedMenuId=mid?parseInt(mid):null;
  saveToLocal(); closeModal(); go(PAGE);
}
function delUser(id){
  var a=auditorById(id); if(!a) return;
  if(!confirm('Delete "'+a.name+'"?')) return;
  for(var i=0;i<AUDITORS.length;i++) if(AUDITORS[i].id===id){AUDITORS.splice(i,1);break;}
  saveToLocal(); go(PAGE);
}

function quickAssign(auditorId){
  var a=auditorById(auditorId); if(!a) return;
  var opts='<option value="">-- All Locations --</option>'+MENUS.filter(function(m){return m&&m.id;}).map(function(m){return '<option value="'+m.id+'"'+(a.assignedMenuId===m.id?' selected':'')+'>'+m.name+'</option>';}).join('');
  modal('Quick Assign — '+a.name,fg('Assign Location','<select id="qa_mid">'+opts+'</select>'),
    '<button class="btn btn-ghost" onclick="closeModal()">Cancel</button><button class="btn btn-pri" onclick="saveQuickAssign('+auditorId+')">Assign</button>');
}
function saveQuickAssign(id){
  var a=auditorById(id); if(!a) return;
  var mid=document.getElementById('qa_mid').value;
  a.assignedMenuId=mid?parseInt(mid):null;
  saveToLocal(); closeModal(); go(PAGE);
  alert(a.name+' assigned to: '+(mid?(menuById(parseInt(mid))||{name:'All'}).name:'All Locations'));
}

// ═══════════ DOWNLOAD ═══════════
// Smart download modal — shows options
function showDownloadModal(){
  var updated=STOCK.filter(function(s){return s.pQty!==null;});
  var submitted=STOCK.filter(function(s){return s.st==='submitted';});
  var today_items=STOCK.filter(function(s){return s.date===today();});
  modal('Download Data',
    '<div style="display:flex;flex-direction:column;gap:.6rem">'
    +'<div style="background:var(--ok-bg);border:1px solid #9fe1cb;border-radius:8px;padding:.8rem 1rem">'
    +'<div style="font-weight:700;color:var(--ok);margin-bottom:4px">&#9989; Submitted Only ('+submitted.length+' items)</div>'
    +'<div style="font-size:12px;color:var(--muted)">Only entries auditors have submitted</div>'
    +'<button class="btn btn-ok" style="margin-top:.5rem;width:100%" onclick="dlFiltered(&quot;submitted&quot;);closeModal()">&#11015; Download Submitted</button>'
    +'</div>'
    +'<div style="background:#e6f1fb;border:1px solid #b5d4f4;border-radius:8px;padding:.8rem 1rem">'
    +'<div style="font-weight:700;color:#0C447C;margin-bottom:4px">&#128221; All Updated ('+updated.length+' items)</div>'
    +'<div style="font-size:12px;color:var(--muted)">All items where auditors entered physical quantity</div>'
    +'<button class="btn" style="margin-top:.5rem;width:100%;background:#0C447C;color:#fff" onclick="dlFiltered(&quot;updated&quot;);closeModal()">&#11015; Download All Updated</button>'
    +'</div>'
    +'<div style="background:var(--warn-bg);border:1px solid #fac775;border-radius:8px;padding:.8rem 1rem">'
    +'<div style="font-weight:700;color:var(--warn);margin-bottom:4px">&#128197; Today Only ('+today_items.length+' items)</div>'
    +'<div style="font-size:12px;color:var(--muted)">Only entries updated today</div>'
    +'<button class="btn" style="margin-top:.5rem;width:100%;background:var(--warn);color:#fff" onclick="dlFiltered(&quot;today&quot;);closeModal()">&#11015; Download Today</button>'
    +'</div>'
    +'<div style="background:var(--bg);border:1px solid var(--border);border-radius:8px;padding:.8rem 1rem">'
    +'<div style="font-weight:700;color:var(--text);margin-bottom:4px">&#128196; Complete Report ('+STOCK.length+' items)</div>'
    +'<div style="font-size:12px;color:var(--muted)">All items including pending</div>'
    +'<button class="btn btn-ghost" style="margin-top:.5rem;width:100%" onclick="dlFiltered(&quot;all&quot;);closeModal()">&#11015; Download Full</button>'
    +'</div>'
    +'<div style="background:var(--bg);border:1px solid var(--border);border-radius:8px;padding:.8rem 1rem">'
    +'<div style="font-weight:700;color:var(--text);margin-bottom:4px">&#128197; By Date Range</div>'
    +'<div class="fr" style="gap:8px;margin-top:.4rem">'
    +'<div style="flex:1"><label style="font-size:11px;color:var(--muted)">From</label><input type="date" id="dl_from" value="'+today()+'" style="width:100%;padding:6px 8px;border:1px solid var(--border);border-radius:6px;font-size:12px"></div>'
    +'<div style="flex:1"><label style="font-size:11px;color:var(--muted)">To</label><input type="date" id="dl_to" value="'+today()+'" style="width:100%;padding:6px 8px;border:1px solid var(--border);border-radius:6px;font-size:12px"></div>'
    +'</div>'
    +'<button class="btn btn-ghost" style="margin-top:.5rem;width:100%" onclick="dlDateRange();closeModal()">&#11015; Download Date Range</button>'
    +'</div>'
    +'</div>',
    '<button class="btn btn-ghost" onclick="closeModal()">Close</button>');
}

function dlFiltered(type){
  var items;
  if(type==='submitted') items=STOCK.filter(function(s){return s.st==='submitted';});
  else if(type==='updated') items=STOCK.filter(function(s){return s.pQty!==null;});
  else if(type==='today') items=STOCK.filter(function(s){return s.date===today();});
  else items=STOCK;
  _doDownload(items,'stock_audit_'+type+'_'+today()+'.xlsx');
}

function dlDateRange(){
  var from=document.getElementById('dl_from').value;
  var to=document.getElementById('dl_to').value;
  if(!from||!to){alert('Select date range');return;}
  var items=STOCK.filter(function(s){return s.date>=from&&s.date<=to&&s.pQty!==null;});
  if(!items.length){alert('No data in this date range');return;}
  _doDownload(items,'stock_audit_'+from+'_to_'+to+'.xlsx');
}

function _doDownload(items,filename){
  var rows=[['Location','Sub Location','Material','Description','Plant','Sys Qty','Phy Qty','Variance','MAP/SPC','Stock Value','Disc Value','SAA Team','Remarks','Date','Time','Status','Auditor']];
  for(var i=0;i<items.length;i++){
    var s=items[i],ex=s.extra||{},m=menuById(s.mid);
    var discVal=s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'';
    rows.push([m?m.name:'',s.sub,ex.material||s.sku,s.name,ex.plant||'',s.sQty,s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',ex.mapSpc||s.rate,s.amt,discVal,ex.saaTeam||s.aud||'',ex.remarks||'',s.date||'',s.time||'',s.st,s.aud||'']);
  }
  if(typeof XLSX!=='undefined'){
    var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);
    ws['!cols']=rows[0].map(function(h){return{wch:Math.max(String(h).length+2,12)};});
    XLSX.utils.book_append_sheet(wb,ws,'Stock Audit');
    XLSX.writeFile(wb,filename);
  }
}


function dlExcel(){
  var rows=[['Location','Sub Location','Material','Description','Plant','Sys Qty','Phy Qty','Variance','MAP/SPC','Stock Value','Disc Value','SAA Team','Remarks','Date','Time','Status','Auditor']];
  for(var i=0;i<STOCK.length;i++){
    var s=STOCK[i],ex=s.extra||{},m=menuById(s.mid);
    rows.push([m?m.name:'',s.sub,ex.material||s.sku,s.name,ex.plant||'',s.sQty,s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',ex.mapSpc||s.rate,s.amt,s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'',ex.saaTeam||s.aud||'',ex.remarks||'',s.date||'',s.time||'',s.st,s.aud||'']);
  }
  if(typeof XLSX!=='undefined'){
    var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);
    ws['!cols']=rows[0].map(function(h){return{wch:Math.max(String(h).length+2,12)};});
    XLSX.utils.book_append_sheet(wb,ws,'Stock Audit');
    XLSX.writeFile(wb,'stock_audit_report.xlsx');
  }
}

function dlSubExcel(mid,subName){
  var items=STOCK.filter(function(s){return s.mid===mid&&s.sub===subName;});
  var rows=[['Sl.No','Material','Description','Plant','Storage Location','Unrestricted Stock','Storage Bin','MAP/SPC','Stock Values','Pur.Group','Pur.Group Des','Physical Quantity','Quantity Variance','Discrepancy Value','SAA Team','Remarks','DATE','TIME','Status','Auditor']];
  for(var i=0;i<items.length;i++){var s=items[i],ex=s.extra||{};rows.push([s.id,ex.material||s.sku,s.name,ex.plant||'',s.sub,s.sQty,ex.storageBin||'',ex.mapSpc||s.rate,s.amt,ex.purGroup||'',ex.purGroupDes||'',s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'',ex.saaTeam||s.aud||'',ex.remarks||'',s.date||'',s.time||'',s.st,s.aud||'']);}
  if(typeof XLSX!=='undefined'){var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);ws['!cols']=rows[0].map(function(h){return{wch:Math.max(String(h).length+2,12)};});XLSX.utils.book_append_sheet(wb,ws,subName.substring(0,31));XLSX.writeFile(wb,subName+'_audit.xlsx');}
}

function dlLocExcel(mid){
  var m=menuById(mid),items=STOCK.filter(function(s){return s.mid===parseInt(mid)||s.mid===mid;});
  var rows=[['Sl.No','Material','Description','Plant','Storage Location','Unrestricted Stock','Storage Bin','MAP/SPC','Stock Values','Physical Quantity','Quantity Variance','Discrepancy Value','SAA Team','Remarks','DATE','TIME','Status','Auditor']];
  for(var i=0;i<items.length;i++){var s=items[i],ex=s.extra||{};rows.push([s.id,ex.material||s.sku,s.name,ex.plant||'',s.sub,s.sQty,ex.storageBin||'',ex.mapSpc||s.rate,s.amt,s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'',ex.saaTeam||s.aud||'',ex.remarks||'',s.date||'',s.time||'',s.st,s.aud||'']);}
  if(typeof XLSX!=='undefined'){var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);ws['!cols']=rows[0].map(function(h){return{wch:Math.max(String(h).length+2,12)};});XLSX.utils.book_append_sheet(wb,ws,(m?m.name:'Location').substring(0,31));XLSX.writeFile(wb,(m?m.name:'location')+'_audit.xlsx');}
}

function dlMyReport(){
  var mine=STOCK.filter(function(s){return s.aud===CU.name;});
  var rows=[['Material','Description','Sub Location','Sys Qty','Phy Qty','Variance','MAP/SPC','Stock Value','Disc Value','SAA Team','Remarks','Date','Time','Status']];
  for(var i=0;i<mine.length;i++){var s=mine[i],ex=s.extra||{};rows.push([ex.material||s.sku,s.name,s.sub,s.sQty,s.pQty!==null?s.pQty:'',s.disc!==null?s.disc:'',ex.mapSpc||s.rate,s.amt,s.disc!==null?(s.disc*(parseFloat(ex.mapSpc||s.rate)||0)).toFixed(2):'',ex.saaTeam||s.aud||'',ex.remarks||'',s.date||'',s.time||'',s.st]);}
  if(typeof XLSX!=='undefined'){var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);XLSX.utils.book_append_sheet(wb,ws,'My Report');XLSX.writeFile(wb,CU.name+'_report.xlsx');}
}

function dlUsers(){
  var rows=[['ID','Name','Username','Password','Phone','Location','Assigned Location','Submissions']];
  for(var i=0;i<AUDITORS.length;i++){var a=AUDITORS[i],s=0;for(var k=0;k<STOCK.length;k++) if(STOCK[k].aud===a.name) s++;var loc=a.assignedMenuId?(menuById(a.assignedMenuId)||{name:'All'}).name:'All';rows.push([a.id,a.name,a.username,a.password,a.phone||'',a.location||'',loc,s]);}
  if(typeof XLSX!=='undefined'){var wb=XLSX.utils.book_new(),ws=XLSX.utils.aoa_to_sheet(rows);XLSX.utils.book_append_sheet(wb,ws,'Users');XLSX.writeFile(wb,'auditor_users.xlsx');}
}

// ── Init on page load ──
function startApp(){
  if(window._appStarted) return;
  window._appStarted = true;
  initFirebase();
  // Check if user was already logged in
  try {
    var savedCU = localStorage.getItem('sav_cu');
    if(savedCU){
      CU = JSON.parse(savedCU);
      if(CU && CU.name && CU.role){
        launch();
        return;
      }
    }
  } catch(e){ localStorage.removeItem('sav_cu'); }
  switchRole('auditor');
}

// startApp() is called after Firebase SDKs load (see bottom of file)
// Fallback: if Firebase not used, start on load
window.addEventListener('load', function(){
  if(!FB_READY && !window._appStarted){
    startApp();
  }
});

</script>
<!-- Firebase SDKs - load LAST so they are available when startApp() runs -->
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-database-compat.js"></script>
<script>
// This runs AFTER Firebase SDKs are loaded
startApp();
</script>
</body>
</html>
