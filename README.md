# for you
Index.html
<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>for you ♡</title>

<link href="https://fonts.googleapis.com/css2?family=Mali:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
*{
  box-sizing:border-box;
  -webkit-tap-highlight-color:transparent;
}

html,body{
  font-family:'Mali',sans-serif;
}

body{
  margin:0;
  min-height:100vh;
  overflow:hidden;
  display:flex;
  justify-content:center;
  align-items:center;

  background:
    radial-gradient(circle at 20% 20%,#ffd9ec 0%,transparent 30%),
    radial-gradient(circle at 80% 80%,#f6c8e2 0%,transparent 30%),
    linear-gradient(135deg,#fff5fa,#ffdbea);

  color:#6d4055;
}

/* บังคับฟอนต์ทุกอย่าง */
button,
input,
textarea,
select,
div,
span,
p{
  font-family:'Mali',sans-serif;
}

/* หัวใจลอย */
.heart{
  position:fixed;
  bottom:-30px;
  font-size:18px;
  opacity:.45;
  animation:floatHeart linear infinite;
  pointer-events:none;
}

@keyframes floatHeart{
  0%{
    transform:translateY(0) rotate(0deg);
    opacity:0;
  }

  15%{
    opacity:.55;
  }

  100%{
    transform:translateY(-110vh) rotate(25deg);
    opacity:0;
  }
}

/* ดาว */
.sparkle{
  position:fixed;
  color:#fff;
  font-size:18px;
  opacity:.7;
  animation:sparkle 2.5s ease-in-out infinite;
  pointer-events:none;
}

@keyframes sparkle{
  0%,100%{
    transform:scale(.7);
    opacity:.25;
  }

  50%{
    transform:scale(1.2);
    opacity:.9;
  }
}

/* กล่องหลัก */
.card{
  position:relative;
  width:min(88vw,370px);
  height:470px;
  padding:30px 25px;

  display:flex;
  flex-direction:column;
  align-items:center;
  justify-content:center;

  text-align:center;

  background:
    linear-gradient(
      145deg,
      rgba(255,255,255,.82),
      rgba(255,235,246,.78)
    );

  border:1px solid rgba(255,255,255,.9);
  border-radius:32px;

  box-shadow:
    0 20px 55px rgba(170,80,125,.18),
    inset 0 0 30px rgba(255,255,255,.7);

  backdrop-filter:blur(12px);

  animation:cardFloat 4s ease-in-out infinite;
}

@keyframes cardFloat{
  0%,100%{
    transform:translateY(0);
  }

  50%{
    transform:translateY(-7px);
  }
}

/* มุม */
.corner{
  position:absolute;
  color:#e89abc;
  font-size:20px;
}

.c1{top:15px;left:18px}
.c2{top:15px;right:18px}
.c3{bottom:15px;left:18px}
.c4{bottom:15px;right:18px}

/* หัวข้อเล็ก */
.mini{
  font-size:11px;
  letter-spacing:1.5px;
  color:#d88baa;
  margin-bottom:10px;
  min-height:18px;
}

/* emoji */
.emoji-wrap{
  position:relative;
  margin-bottom:18px;
}

.emoji-wrap::before{
  content:"";

  position:absolute;

  width:90px;
  height:90px;

  border-radius:50%;

  background:#ffd9ea;

  filter:blur(15px);

  left:50%;
  top:50%;

  transform:translate(-50%,-50%);

  z-index:-1;
}

.emoji{
  font-size:70px;
  line-height:1;

  animation:
    emojiFloat 2.8s ease-in-out infinite;
}

@keyframes emojiFloat{
  0%,100%{
    transform:translateY(0) rotate(-2deg);
  }

  50%{
    transform:translateY(-6px) rotate(2deg);
  }
}

/* ข้อความสารภาพ */
.message{
  width:100%;
  max-width:300px;
  max-height:270px;

  overflow:hidden;

  padding:15px 17px;

  border-radius:20px;

  background:rgba(255,255,255,.65);

  border:1px solid rgba(240,160,195,.22);

  font-size:13.5px;
  line-height:1.8;

  color:#684455;

  margin-bottom:18px;
}

/* ปุ่ม */
button{
  border:none;
  outline:none;
  cursor:pointer;

  font-size:13px;
  font-weight:600;

  color:white;

  padding:11px 22px;

  border-radius:999px;

  background:
    linear-gradient(
      135deg,
      #f29abe,
      #df76a5
    );

  box-shadow:
    0 8px 18px rgba(216,105,151,.25);

  transition:.25s;

  position:relative;
  overflow:hidden;
}

button:hover{
  transform:translateY(-3px);

  box-shadow:
    0 12px 22px rgba(216,105,151,.32);
}

button:active{
  transform:scale(.95);
}

/* แสงบนปุ่ม */
button::after{
  content:"";

  position:absolute;

  top:0;
  left:-100%;

  width:60%;
  height:100%;

  background:
    linear-gradient(
      90deg,
      transparent,
      rgba(255,255,255,.5),
      transparent
    );

  transform:skewX(-20deg);

  animation:buttonShine 3s infinite;
}

@keyframes buttonShine{
  0%{
    left:-100%;
  }

  35%,100%{
    left:130%;
  }
}

/* ตัวเลือก */
.choices{
  width:100%;
  max-width:285px;

  margin:2px 0 15px;

  display:flex;
  flex-direction:column;

  gap:9px;

  text-align:left;
}

.choice{
  display:flex;
  align-items:center;

  gap:9px;

  padding:8px 10px;

  border-radius:14px;

  background:rgba(255,255,255,.55);

  border:1px solid rgba(228,145,180,.2);

  font-size:12px;

  color:#71495b;

  cursor:pointer;

  transition:.2s;
}

.choice:hover{
  background:rgba(255,255,255,.85);
  transform:translateX(3px);
}

/* checkbox */
.checkbox{
  width:20px;
  height:20px;

  flex-shrink:0;

  border-radius:50%;

  border:2px solid #e59ab9;

  display:flex;

  align-items:center;
  justify-content:center;

  color:white;

  font-size:12px;
  font-weight:bold;

  transition:.25s;
}

.choice.checked .checkbox{
  background:#e68bb0;

  border-color:#e68bb0;

  box-shadow:
    0 0 10px rgba(230,139,176,.45);
}

.choice.checked{
  background:rgba(255,221,235,.7);
}

/* คำเตือนกลางจอ */
.warning{
  position:absolute;

  left:50%;
  top:50%;

  transform:
    translate(-50%,-50%)
    scale(.85);

  padding:10px 20px;

  border-radius:999px;

  background:rgba(255,174,205,.95);

  color:white;

  font-size:15px;
  font-weight:600;

  white-space:nowrap;

  opacity:0;

  pointer-events:none;

  box-shadow:
    0 8px 25px rgba(220,110,155,.25);
}

.warning.show{
  animation:
    warningPop .9s ease forwards;
}

@keyframes warningPop{

  0%{
    opacity:0;

    transform:
      translate(-50%,-50%)
      scale(.75);
  }

  20%{
    opacity:1;

    transform:
      translate(-50%,-50%)
      scale(1.05);
  }

  45%{
    opacity:1;

    transform:
      translate(-50%,-50%)
      scale(1);
  }

  75%{
    opacity:1;
  }

  100%{
    opacity:0;

    transform:
      translate(-50%,-50%)
      scale(.95);
  }
}

/* จำนวนครั้งลูบหัว */
.pet-count{
  font-size:11px;

  color:#c886a2;

  margin-top:8px;

  opacity:.8;
}

/* เปลี่ยนหน้า */
.fade{
  animation:
    fadePage .45s ease;
}

@keyframes fadePage{

  from{
    opacity:0;

    transform:
      scale(.94)
      translateY(8px);
  }

  to{
    opacity:1;

    transform:
      scale(1)
      translateY(0);
  }
}

/* หน้าก่อนสารภาพ */
.ready-screen{
  position:absolute;

  inset:0;

  display:flex;

  align-items:center;
  justify-content:center;

  flex-direction:column;

  text-align:center;

  pointer-events:none;
}

.ready-text{
  font-size:17px;

  font-weight:600;

  color:#77475c;

  opacity:0;

  animation:
    readyText 2.8s ease forwards;
}

@keyframes readyText{

  0%{
    opacity:0;

    transform:
      translateY(8px)
      scale(.96);
  }

  22%{
    opacity:1;

    transform:
      translateY(0)
      scale(1);
  }

  65%{
    opacity:1;

    transform:
      translateY(0)
      scale(1);
  }

  100%{
    opacity:0;

    transform:
      translateY(-5px)
      scale(.98);
  }
}

.countdown{
  font-size:52px;

  font-weight:600;

  color:#df82a8;

  opacity:0;

  transform:scale(.8);
}

.countdown.show{
  animation:
    countPop .75s ease forwards;
}

@keyframes countPop{

  0%{
    opacity:0;
    transform:scale(.75);
  }

  35%{
    opacity:1;
    transform:scale(1.08);
  }

  70%{
    opacity:1;
    transform:scale(1);
  }

  100%{
    opacity:0;
    transform:scale(1.12);
  }
}
</style>
</head>

<body>

<!-- หัวใจลอย -->
<div class="heart" style="left:8%;animation-duration:9s;">♡</div>
<div class="heart" style="left:22%;animation-duration:12s;animation-delay:2s;">♥</div>
<div class="heart" style="left:43%;animation-duration:10s;animation-delay:4s;">♡</div>
<div class="heart" style="left:65%;animation-duration:13s;animation-delay:1s;">♥</div>
<div class="heart" style="left:82%;animation-duration:11s;animation-delay:3s;">♡</div>

<!-- ดาว -->
<div class="sparkle" style="top:13%;left:12%;">✦</div>
<div class="sparkle" style="top:22%;right:13%;animation-delay:.8s;">✧</div>
<div class="sparkle" style="bottom:17%;left:10%;animation-delay:1.3s;">✦</div>
<div class="sparkle" style="bottom:25%;right:11%;animation-delay:.4s;">✧</div>

<!-- การ์ด -->
<div class="card" id="card">

  <div class="corner c1">♡</div>
  <div class="corner c2">✦</div>
  <div class="corner c3">✧</div>
  <div class="corner c4">♡</div>

  <div id="content"></div>

</div>

<script>

const content=
  document.getElementById("content");

let petCount=0;

let selected=[
  false,
  false,
  false,
  false
];

/* คำเตือน */
let warningIndex=0;

const warningTexts=[
  "กดสิเว้ยย",
  "จะดื้อไม่กดครบอีก!",
  "งั้นอยู่แบบนี่แหละ!",
  "แล้วแต่! เหอะ"
];


/* =========================
   เปลี่ยนหน้า
========================= */

function render(html){

  content.classList.remove("fade");

  void content.offsetWidth;

  content.innerHTML=html;

  content.classList.add("fade");
}


/* =========================
   เอฟเฟกต์หัวใจ
========================= */

function heartBurst(){

  for(let i=0;i<8;i++){

    const h=
      document.createElement("div");

    h.textContent=
      Math.random()>.5
      ? "♡"
      : "♥";

    h.style.position="fixed";

    h.style.left="50%";
    h.style.top="50%";

    h.style.fontSize=
      (12+Math.random()*14)+"px";

    h.style.color="#e98caf";

    h.style.pointerEvents="none";

    h.style.zIndex="20";

    document.body.appendChild(h);

    const x=
      (Math.random()-.5)*180;

    const y=
      (Math.random()-.5)*180;

    h.animate(
      [
        {
          transform:
            "translate(-50%,-50%) scale(.5)",

          opacity:1
        },

        {
          transform:
            `translate(
              calc(-50% + ${x}px),
              calc(-50% + ${y}px)
            ) scale(1.3)`,

          opacity:0
        }
      ],
      {
        duration:800,
        easing:"ease-out"
      }
    );

    setTimeout(()=>{
      h.remove();
    },800);
  }
}


/* =========================
   หน้าแรก
========================= */

function page1(){

  render(`

    <div class="mini">
      FOR YOU ♡
    </div>

    <div class="emoji-wrap">
      <div class="emoji">
        💗
      </div>
    </div>

    <button onclick="page2()">
      กดดูนะ ต้องกด
    </button>

  `);

}


/* =========================
   หน้าสอง
========================= */

function page2(){

  render(`

    <div class="mini">
      HEY YOU... ♡
    </div>

    <div class="emoji-wrap">
      <div class="emoji">
        🐱
      </div>
    </div>

    <div style="
      font-size:13px;
      color:#7b5062;
      margin-bottom:18px;
    ">
      มีอะไรจะให้ดูหน่อย
    </div>

    <div style="
      display:flex;
      flex-direction:column;
      gap:10px;
    ">

      <button onclick="surePage()">
        กดดูต่อไปไหม
      </button>

      <button onclick="pageAngry()">
        ไม่เอาไม่กดหรอก แบร่
      </button>

    </div>

  `);

}


/* =========================
   ด่านแน่ใจ
========================= */

function surePage(){

  heartBurst();

  selected=[
    false,
    false,
    false,
    false
  ];

  render(`

    <div class="mini">
      WAIT A SECOND... ♡
    </div>

    <div class="emoji-wrap">
      <div class="emoji">
        😼
      </div>
    </div>

    <div style="
      font-size:15px;
      font-weight:600;
      color:#744457;
      margin-bottom:14px;
    ">
      แน่ใจหรอ
    </div>

    <div class="choices">

      <div
        class="choice"
        onclick="toggleChoice(0,this)"
      >
        <div class="checkbox"></div>
        <div>ทำใจรึยัง</div>
      </div>

      <div
        class="choice"
        onclick="toggleChoice(1,this)"
      >
        <div class="checkbox"></div>
        <div>ต้องบอกด้วยนะตอนดูเสร็จ</div>
      </div>

      <div
        class="choice"
        onclick="toggleChoice(2,this)"
      >
        <div class="checkbox"></div>
        <div>ละคิดถึงริคไหม</div>
      </div>

      <div
        class="choice"
        onclick="toggleChoice(3,this)"
      >
        <div class="checkbox"></div>
        <div>ลองเห่าบ๊อกแบ๊กสามที</div>
      </div>

    </div>

    <div
      class="warning"
      id="warning"
    ></div>

    <button onclick="checkChoices()">
      แน่ใจ!
    </button>

  `);

}


/* =========================
   ติ๊กตัวเลือก
========================= */

function toggleChoice(index,element){

  selected[index]=
    !selected[index];

  element.classList.toggle(
    "checked",
    selected[index]
  );

  const box=
    element.querySelector(".checkbox");

  box.innerHTML=
    selected[index]
    ? "✓"
    : "";
}


/* =========================
   ตรวจตัวเลือก
========================= */

function checkChoices(){

  const allChecked=
    selected.every(v=>v);

  if(!allChecked){

    const warning=
      document.getElementById("warning");

    warning.textContent=
      warningTexts[warningIndex];

    warningIndex++;

    if(
      warningIndex>=
      warningTexts.length
    ){
      warningIndex=0;
    }

    warning.classList.remove("show");

    void warning.offsetWidth;

    warning.classList.add("show");

    heartBurst();

    return;
  }

  heartBurst();

  petPage();
}


/* =========================
   หน้าลูบหัวแมว
========================= */

function petPage(){

  petCount=0;

  render(`

    <div class="mini">
      GOOD BOY... ♡
    </div>

    <div class="emoji-wrap">

      <div
        class="emoji"
        id="cat"
      >
        🐱
      </div>

    </div>

    <div style="
      font-size:14px;
      font-weight:600;
      color:#744457;
      margin-bottom:8px;
    ">
      ลูบๆหัวแมวริค
    </div>

    <div
      class="pet-count"
      id="petCount"
    >
      กดตรงแมวสิ ♡
    </div>

  `);

  document
    .getElementById("cat")
    .onclick=petCat;
}


/* =========================
   ลูบหัวแมว
========================= */

function petCat(){

  petCount++;

  heartBurst();

  const cat=
    document.getElementById("cat");

  const count=
    document.getElementById("petCount");

  cat.animate(
    [
      {
        transform:
          "scale(1) rotate(0deg)"
      },

      {
        transform:
          "scale(1.12) rotate(-5deg)"
      },

      {
        transform:
          "scale(1) rotate(5deg)"
      },

      {
        transform:
          "scale(1)"
      }
    ],
    {
      duration:350
    }
  );

  if(petCount<5){

    count.textContent=
      `ลูบไปแล้ว ${petCount}/5 ครั้ง ♡`;

  }else{

    count.textContent=
      "โอเค... ยอมแล้วก็ได้ ♡";

    setTimeout(()=>{

      readyToConfess();

    },700);
  }
}


/* =========================
   ฉากก่อนสารภาพ
========================= */

function readyToConfess(){

  content.innerHTML=`

    <div class="ready-screen">

      <div
        class="ready-text"
        id="readyText"
      >
        โอเคงั้นพร้อมนะ
      </div>

      <div
        class="countdown"
        id="countdown"
      ></div>

    </div>

  `;

  const countdown=
    document.getElementById("countdown");

  setTimeout(()=>{

    let number=3;

    function nextNumber(){

      countdown.textContent=
        number;

      countdown.classList.remove(
        "show"
      );

      void countdown.offsetWidth;

      countdown.classList.add(
        "show"
      );

      if(number===1){

        setTimeout(()=>{

          confessionPage();

        },750);

      }else{

        number--;

        setTimeout(
          nextNumber,
          750
        );
      }
    }

    nextNumber();

  },2800);
}


/* =========================
   หน้าสารภาพ
========================= */

function confessionPage(){

  heartBurst();

  render(`

    <div class="mini">
      SOMETHING I WANNA SAY ♡
    </div>

    <div class="emoji-wrap">

      <div class="emoji">
        🐱
      </div>

    </div>

    <div class="message">

      ริคชอบเต๋านะ ชอบมาก ๆ เต๋าไม่รู้จะดูออกไหม ที่ผ่านมาริครอเต๋า รอคุย บอกฝันดีเต๋า ให้กำลังใจ คิดถึงเต๋า ริคโครตอยากมีเต๋าอยู่ด้วย เต๋าทำให้ริคอินความรักไม่เคยเป็นแบบนี่ ถึงจะดูเร็ว แต่ริคชอบมาก ๆ ริคจะค่อย ๆ เป็น ค่อย ๆ ไปนะ ริคไม่อยากให้เต๋าอึดอัด ริคอยากสารภาพให่เต๋าหมดเลยครับ อยากให้เต๋ารู้ ทุก ๆ วัน ริคตื่นเต้นแชทเต๋าอินเลิฟมาก ๆ ต่างจากที่ผ่านมาริคคบกับใครก็ไม่อินเลิฟเท่าแบบนี่เลย วันไหนแย่หรือเหนื่อยนึกถึงคุยกับเต๋า ริคก็โครตมีความสุขเลยครับ จากแฟนเดย์ริคคิดว่าคงน่าเบื่อเหมือนเดิม ๆ แต่รอบนี่มันไม่ได้น่าเบื่อเลย เต๋าเหมือนคนเปลี่ยนโลกของริคเป็นอีกแบบเลยครับ 555 ริคชอบเต๋านะ

    </div>

  `);
}


/* =========================
   หน้าปุ่มไม่เอา
========================= */

function pageAngry(){

  render(`

    <div class="mini">
      อ้าว... 😾
    </div>

    <div class="emoji-wrap">

      <div class="emoji">
        😾
      </div>

    </div>

    <div style="
      font-size:13px;
      margin-bottom:18px;
      color:#75485b;
    ">
      กล้าปฏิเสธแมวริคเหรอ
    </div>

    <div style="
      display:flex;
      flex-direction:column;
      gap:10px;
      align-items:center;
    ">

      <button
        id="yesBtn"
        onclick="pageLast()"
      >
        กดเหอะ!
      </button>

      <button
        id="noBtn"
        onclick="makeYesBigger()"
      >
        ไม่เอาอ่ะ!
      </button>

    </div>

  `);
}


/* =========================
   เล่นกับปุ่ม
========================= */

function makeYesBigger(){

  const yes=
    document.getElementById("yesBtn");

  const no=
    document.getElementById("noBtn");

  let size=
    parseFloat(
      getComputedStyle(yes).fontSize
    );

  yes.style.fontSize=
    (size+3)+"px";

  yes.style.padding=
    "14px 28px";

  no.style.transform=
    "scale(.75)";

  no.style.opacity=".65";

  heartBurst();
}


/* =========================
   หน้าบังคับ
========================= */

function pageLast(){

  heartBurst();

  render(`

    <div class="mini">
      LAST WARNING ♡
    </div>

    <div class="emoji-wrap">

      <div class="emoji">
        😼
      </div>

    </div>

    <div style="
      font-size:13px;
      line-height:1.8;
      color:#714658;
      margin-bottom:18px;
    ">

      บอกให้กดก็กด<br>
      จะโดนหอมแก้มเลย<br>
      กดอ่านดูนะเจ้าหมามึนตัวนี่

    </div>

    <button onclick="readyToConfess()">
      ต้องกด
    </button>

  `);
}


/* =========================
   เริ่มต้น
========================= */

page1();

</script>

</body>
</html>
