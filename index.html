// ===== المستوى العلمي والسلوكي (يعمل مع script.js بدون تعديله) =====
// المستوى العلمي = اختبار 1 + اختبار 2 + المذكرة + المهمة 1 + المهمة 2 (من 65)
// المستوى السلوكي = المشاركة + السلوك (من 20)
const LV_ACAD = { cols: [8, 9, 5, 6, 7], max: 65, icon: "🎓", title: "المستوى العلمي" };
const LV_BEH = { cols: [3, 4], max: 20, icon: "🤝", title: "المستوى السلوكي" };
const QUALITY_COL = 2, QUALITY_MAX = 15;

// ===== إعدادات زيارة الجودة والاحتفال =====
const QUALITY_OPEN = false;   // false = شكر وتهنئة بعد الزيارة | true = دعوة "شارك واحصل على 15 درجة"
const HONOR_NAME_WORDS = 3;   // عدد كلمات الاسم في لوحة الشرف (0 = الاسم كاملًا)
const SCHOOL_NAME = "مدرسة البلاد القديم الابتدائية الإعدادية";
const PRINCIPAL = "محمد ابراهيم";

// المستويات: l4 متميز، l3 جيد جدًا، l2 جيد، l1 يحتاج دعمًا
const LV_TEXT = {
  acad: {
    4: ["متميز", "مستوى علمي رفيع، بارك الله فيه ووفقه."],
    3: ["جيد جدًا", "مستوى علمي جيد جدًا وقريب من التميز."],
    2: ["جيد", "مستوى علمي جيد يحتاج مزيدًا من المتابعة."],
    1: ["يحتاج دعمًا", "نتعاون معًا لرفع مستواه العلمي بإذن الله."],
  },
  beh: {
    4: ["متميز", "سلوك راقٍ وانضباط مشرّف داخل الصف."],
    3: ["جيد جدًا", "سلوك جيد جدًا والتزام واضح بالتعليمات."],
    2: ["جيد", "سلوك جيد مع حاجة لمزيد من الانضباط."],
    1: ["يحتاج توجيهًا", "نتعاون معًا لتعزيز الانضباط الصفي بإذن الله."],
  },
};

function lvLevel(p) { return p >= 90 ? 4 : p >= 75 ? 3 : p >= 60 ? 2 : 1; }

// ميدالية متحركة بلون يناسب المستوى
function lvMedal(icon, lvl) {
  const spark = lvl >= 3 ? `<g fill="#fff"><text class="tw" x="6" y="30" font-size="14">✦</text><text class="tw" x="64" y="24" font-size="11" style="animation-delay:.6s">✦</text>${lvl === 4 ? '<text class="tw" x="68" y="64" font-size="12" style="animation-delay:1.1s">✦</text>' : ""}</g>` : "";
  const crown = lvl === 4 ? `<path class="tw" d="M28 34l4-9 8 6 8-6 4 9z" fill="#FFD43B" style="animation-duration:2.4s"/>` : "";
  return `<svg viewBox="0 0 80 90"><path d="M26 0h12l8 32H34z" fill="rgba(255,255,255,.6)"/><path d="M54 0H42l-8 32h12z" fill="rgba(255,255,255,.38)"/>
    <g class="mb"><circle cx="40" cy="58" r="28" fill="#fff"/><circle cx="40" cy="58" r="23" fill="none" stroke="var(--l1)" stroke-width="4"/><text x="40" y="69" text-anchor="middle" font-size="27">${icon}</text></g>${crown}${spark}</svg>`;
}

function lvCard(def, key, r, delay) {
  const sum = def.cols.reduce((s, c) => s + (/\d/.test(clean(r[c])) ? (num(r[c]) || 0) : 0), 0);
  const pct = Math.min(100, Math.round(sum / def.max * 100));
  const lvl = lvLevel(pct), t = LV_TEXT[key][lvl];
  return `<div class="lv l${lvl}" style="animation-delay:${delay}s">
    <div class="lvi">${lvMedal(def.icon, lvl)}</div>
    <div class="lvt"><small>${def.title}</small><b>${t[0]}</b>
      <div class="lvbar"><i data-w="${pct}"></i></div>
      <em>${pct}%</em><p>${t[1]}</p></div></div>`;
}

// ===== زيارة الجودة =====
function qScore(r) {
  const raw = clean(r[QUALITY_COL]);
  return /\d/.test(raw) ? (num(raw) || 0) : 0;
}

// قصاصات احتفال تتساقط على الشاشة
function confettiRain(ms) {
  try {
    if (window.matchMedia && matchMedia("(prefers-reduced-motion: reduce)").matches) return;
    const colors = ["#FFD43B", "#CE1126", "#fff", "#22d3ee", "#a3e635", "#f472b6", "#fb923c"];
    const box = document.createElement("div"); box.className = "rain";
    let h = "";
    for (let i = 0; i < 70; i++) {
      h += `<i style="left:${Math.random() * 100}%;background:${colors[i % colors.length]};--dx:${Math.round(Math.random() * 160 - 80)}px;animation-duration:${3 + Math.random() * 3}s;animation-delay:${Math.random() * 1.8}s"></i>`;
    }
    box.innerHTML = h;
    document.body.appendChild(box);
    setTimeout(() => box.remove(), ms || 8000);
  } catch (e) {}
}

// شهادة شكر وتقدير
function certHTML(name, score) {
  return `<div class="cert">
    <svg class="seal" viewBox="0 0 80 90"><path d="M26 0h12l8 32H34z" fill="#CE1126"/><path d="M54 0H42l-8 32h12z" fill="#8f0c1d"/><circle cx="40" cy="58" r="28" fill="#F5B700"/><circle cx="40" cy="58" r="22" fill="none" stroke="#fff" stroke-width="3"/><text x="40" y="68" text-anchor="middle" font-size="26">🏅</text></svg>
    <h3 class="cs1">شهادة شكر وتقدير</h3>
    <p class="cs2">تتقدم ${esc(SCHOOL_NAME)} بالشكر والتهنئة للطالب</p>
    <div class="cn">${esc(name)}</div>
    <p class="cm">على مشاركته الفاعلة وتفاعله المميز في زيارة الجودة،<br>وحصوله على <strong>${esc(fmt(score))}</strong> من ${QUALITY_MAX} درجة.<br>بارك الله في جهده ووفقه لمزيد من التميز 🌟</p>
    <div class="sig"><div>🏫 إدارة المدرسة</div><div>مدير المدرسة<small>${esc(PRINCIPAL)}</small></div></div>
  </div>`;
}

function openCert(name, score) {
  openReport(`<div class="t1"><div class="rwrap" style="background:#fff">
    <button class="rclose" data-close aria-label="إغلاق">✕</button>
    ${certHTML(name, score)}
    <div class="racts" style="padding-bottom:14px"><button data-print>🖨️ طباعة الشهادة</button><button class="gray" data-close>إغلاق</button></div>
  </div></div>`, { confetti: false });
}

// بطاقة زيارة الجودة داخل نتيجة الطالب
function qualityCard(r) {
  const n = qScore(r);
  const name = clean(r[1]) || ("طالب رقم " + clean(r[0]));
  if (n > 0) {
    return `<div class="qs thanks"><div class="qsi bounce">🏅</div><div><b>شكرًا ${clean(r[1]) ? esc(clean(r[1]).split(" ")[0]) + " " : ""}على مشاركتك المميزة في زيارة الجودة! 🎉</b>
      <p>مجهودك وتفاعلك محل فخر لنا، وحصلت على <strong>${esc(fmt(n))}</strong> من ${QUALITY_MAX} درجة. بارك الله في جهدك.</p>
      <button class="cbtn" id="certbtn">🎓 عرض شهادة الشكر وطباعتها</button></div></div>`;
  }
  if (!QUALITY_OPEN) {
    return `<div class="qs ok" style="background:linear-gradient(135deg,#eff6ff,#dbeafe);border-color:#93c5fd;color:#1e3a8a"><div class="qsi">🌱</div><div><b>لم تُسجَّل لك مشاركة في زيارة الجودة هذه المرة</b>
      <p>نتطلع لمشاركتك وتفاعلك في الزيارات القادمة، فكل مشاركة تصنع فرقًا وتضيف لك درجات.</p></div></div>`;
  }
  const total = FIELDS.reduce((s, f) => s + (/\d/.test(clean(r[f.col])) ? (num(r[f.col]) || 0) : 0), 0);
  const after = Math.min(TOTAL_MAX, total + QUALITY_MAX);
  return `<div class="qs no"><div class="qsi bounce">⭐</div><div><b>لا تفوّت درجات زيارة الجودة!</b>
    <p>شارك وتفاعل لتحصل على <strong>${QUALITY_MAX} درجة إضافية</strong>. مجموعك الآن ${esc(fmt(total))} من ${TOTAL_MAX}، ويصبح <strong>${esc(fmt(after))}</strong> بعد المشاركة والتفاعل.</p>
    <span class="qbadge">+${QUALITY_MAX} درجة</span></div></div>`;
}

// ===== لوحة الشرف =====
function shortName(n) {
  const w = clean(n).split(" ");
  return HONOR_NAME_WORDS > 0 ? w.slice(0, HONOR_NAME_WORDS).join(" ") : w.join(" ");
}
function countUp(el, to, suffix) {
  const t0 = performance.now(), dur = 1400;
  (function step(t) {
    const k = Math.min(1, (t - t0) / dur);
    el.textContent = Math.round(to * (1 - Math.pow(1 - k, 3))) + (suffix || "");
    if (k < 1) requestAnimationFrame(step);
  })(t0);
}
async function loadHonor() {
  const grid = document.getElementById("hGrid");
  if (!grid) return;
  try {
    const data = await loadData();
    const students = data.filter(r => normalize(r[0]).length >= 6);
    const part = students.filter(r => qScore(r) > 0);
    const pct = students.length ? Math.round(part.length / students.length * 100) : 0;
    countUp(document.getElementById("hN"), part.length);
    countUp(document.getElementById("hT"), students.length);
    countUp(document.getElementById("hP"), pct, "%");
    setTimeout(() => (document.getElementById("hB").style.width = pct + "%"), 200);
    grid.innerHTML = part.length
      ? part.map((r, i) => `<span class="hc" style="animation-delay:${Math.min(i * 0.05, 2)}s"><i>⭐</i>${esc(shortName(clean(r[1]) || "طالب رقم " + clean(r[0])))}</span>`).join("")
      : '<span class="hload">ستظهر هنا أسماء الطلاب المشاركين بإذن الله.</span>';
  } catch (e) {
    grid.innerHTML = '<span class="hload">تعذر تحميل لوحة الشرف حاليًا.</span>';
  }
}

// ===== ربط العرض بنتيجة الطالب =====
const _origShow = show;
show = function (r) {
  _origShow(r);
  try {
    const box = document.getElementById("student");
    const body = box.querySelector(".body");
    if (body) body.insertAdjacentHTML("afterbegin", qualityCard(r));
    const tiles = box.querySelector(".tiles");
    if (tiles) tiles.insertAdjacentHTML("beforebegin", `<div class="lvs">${lvCard(LV_ACAD, "acad", r, 0)}${lvCard(LV_BEH, "beh", r, 0.15)}</div>`);
    const cb = box.querySelector("#certbtn");
    if (cb) {
      const n = qScore(r), name = clean(r[1]) || ("طالب رقم " + clean(r[0]));
      cb.onclick = () => openCert(name, n);
      confettiRain(6000); // احتفال بمشاركة الطالب
    }
    requestAnimationFrame(() => requestAnimationFrame(() => {
      box.querySelectorAll(".lvbar i").forEach(b => (b.style.width = b.dataset.w + "%"));
    }));
  } catch (e) { /* لا يؤثر على عرض الدرجات */ }
};

// ===== احتفال الصفحة + لوحة الشرف =====
document.getElementById("again").addEventListener("click", () => confettiRain(8000));
try {
  if (!sessionStorage.getItem("celebrated")) { confettiRain(8000); sessionStorage.setItem("celebrated", "1"); }
} catch (e) { confettiRain(8000); }
loadHonor();
