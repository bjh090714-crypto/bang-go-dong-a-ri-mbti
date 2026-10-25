<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>방어진고 영화진로탐사대 · 나와 닮은 캐릭터 MBTI</title>
<style>
:root{--bg:#fff7ed;--card:#ffffff;--text:#2b1d12;--sub:#7a6a5c;--accent:#e4572e;--accent2:#f5b700;--line:#f0dfcc;--chip:#fdebd6;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#17110c;--card:#241a12;--text:#fbeede;--sub:#bda78f;--accent:#ff7a4d;--accent2:#ffcf3d;--line:#3a2b1e;--chip:#33241a;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#17110c;--card:#241a12;--text:#fbeede;--sub:#bda78f;--accent:#ff7a4d;--accent2:#ffcf3d;--line:#3a2b1e;--chip:#33241a;color-scheme:dark}
*{box-sizing:border-box}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--text);font-family:"Pretendard","Noto Sans KR","Apple SD Gothic Neo","Malgun Gothic",sans-serif;min-height:100vh;display:flex;justify-content:center;padding:20px 14px}
.wrap{width:100%;max-width:560px}
.card{background:var(--card);border:1px solid var(--line);border-radius:22px;padding:28px 22px;box-shadow:0 8px 30px rgba(120,70,20,.10)}
.screen{display:none}.screen.on{display:block;animation:in .35s ease}
@keyframes in{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}
h1{font-size:28px;line-height:1.3;margin:6px 0 10px}
h2{font-size:20px;line-height:1.45;margin:18px 0 18px}
p{color:var(--sub);line-height:1.65;margin:0 0 14px}
.big{font-size:64px;text-align:center;margin:6px 0}
.tag{display:inline-block;background:var(--chip);color:var(--accent);font-weight:700;border-radius:99px;padding:5px 12px;font-size:13px}
.btn{display:block;width:100%;border:0;border-radius:14px;padding:16px;font-size:16px;font-weight:700;cursor:pointer;font-family:inherit;background:var(--accent);color:#fff;margin-top:10px}
.btn.ghost{background:var(--chip);color:var(--text)}
.btn:active{transform:scale(.98)}
.opt{display:block;width:100%;text-align:left;background:var(--bg);color:var(--text);border:2px solid var(--line);border-radius:14px;padding:16px;font-size:15.5px;line-height:1.5;margin-bottom:10px;cursor:pointer;font-family:inherit}
.opt:hover,.opt:focus-visible{border-color:var(--accent);outline:none}
.bar{height:8px;background:var(--chip);border-radius:99px;overflow:hidden}
.bar i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--accent),var(--accent2));transition:width .3s}
.meta{display:flex;justify-content:space-between;font-size:13px;color:var(--sub);margin-bottom:8px}
.res{text-align:center}
.mbti{font-size:46px;font-weight:900;letter-spacing:4px;color:var(--accent);margin:4px 0}
.cname{font-size:26px;font-weight:800;margin:4px 0}
.movie{color:var(--sub);font-size:14px;margin-bottom:14px}
.quote{background:var(--chip);border-radius:14px;padding:14px;font-size:15px;line-height:1.6;text-align:left;margin:10px 0}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
.mini{background:var(--bg);border:1px solid var(--line);border-radius:14px;padding:12px;text-align:center}
.mini b{display:block;color:var(--accent);font-size:15px}
.mini span{font-size:30px;display:block}
.mini small{color:var(--sub);font-size:12px}
.mini.me{border-color:var(--accent);border-width:2px}
.foot{text-align:center;font-size:12px;color:var(--sub);margin-top:14px}
</style>
</head>
<body>
<div class="wrap">
<div class="card">

<section id="s-start" class="screen on">
  <div class="big">🎬</div>
  <div style="text-align:center"><span class="tag">방어진고 영화진로탐사대</span></div>
  <h1 style="text-align:center">나와 닮은<br>영화·애니 캐릭터는?</h1>
  <p style="text-align:center">12개의 질문으로 알아보는 MBTI 검사!<br>나와 같은 MBTI를 가진 영화·애니메이션 캐릭터를 만나보세요.</p>
  <button class="btn" id="btn-start">검사 시작하기</button>
  <button class="btn ghost" id="btn-all">16명의 캐릭터 미리보기</button>
</section>

<section id="s-q" class="screen">
  <div class="meta"><span id="q-num">1 / 12</span><span id="q-axis"></span></div>
  <div class="bar"><i id="bar"></i></div>
  <h2 id="q-text"></h2>
  <div id="q-opts"></div>
</section>

<section id="s-res" class="screen res">
  <span class="tag">나의 MBTI는</span>
  <div class="mbti" id="r-mbti"></div>
  <div class="big" id="r-emoji"></div>
  <div class="cname" id="r-name"></div>
  <div class="movie" id="r-movie"></div>
  <div class="quote" id="r-desc"></div>
  <p id="r-trait" style="margin-top:6px"></p>
  <button class="btn" id="btn-retry">다시 검사하기</button>
  <button class="btn ghost" id="btn-all2">16명의 캐릭터 전체 보기</button>
  <div class="foot">※ 캐릭터별 MBTI는 팬들 사이의 해석을 바탕으로 한 재미용 결과예요.<br>방어진고 영화진로탐사대</div>
</section>

<section id="s-all" class="screen">
  <h1 style="font-size:22px">영화·애니 캐릭터 MBTI 도감</h1>
  <div class="grid" id="all-grid"></div>
  <button class="btn" id="btn-back">돌아가기</button>
</section>

</div>
</div>

<script>
var Q=[
["EI","주말에 약속이 하나도 없다면?","심심해서 누구라도 불러낸다","집에서 혼자 쉬는 게 최고다","E","I"],
["EI","처음 보는 사람들과 있을 때 나는?","먼저 말을 걸며 분위기를 띄운다","누가 말을 걸어주길 기다린다","E","I"],
["EI","에너지가 충전되는 순간은?","사람들과 신나게 떠들 때","조용히 혼자만의 시간을 보낼 때","E","I"],
["SN","영화나 애니를 볼 때 더 눈에 들어오는 건?","연기·연출·작화 같은 눈에 보이는 디테일","숨은 의미와 떡밥, 결말 해석","S","N"],
["SN","친구에게 무언가를 설명할 때 나는?","구체적인 사례와 경험을 들어 말한다","비유와 큰 그림으로 설명한다","S","N"],
["SN","볼 영화나 애니를 고를 때는?","평점과 후기를 보고 검증된 작품을 고른다","소재가 끌리면 정보 없이도 일단 본다","S","N"],
["TF","친구가 고민을 털어놓으면?","현실적인 해결책부터 알려준다","일단 공감하고 같이 속상해한다","T","F"],
["TF","영화나 애니를 보고 나서 나는?","개연성 허점이 먼저 보인다","인물의 감정에 이입해 눈물이 난다","T","F"],
["TF","중요한 결정을 할 때 더 중요한 건?","논리와 효율","사람들의 마음과 분위기","T","F"],
["JP","여행을 갈 때 나는?","시간대별 계획표를 짜 간다","발길 닿는 대로 즉흥으로 다닌다","J","P"],
["JP","과제나 시험 준비는?","미리미리 계획대로 진행한다","마감 직전에 몰입해서 해낸다","J","P"],
["JP","내 책상이나 방은?","물건 자리가 정해져 있고 깔끔하다","나만 아는 질서 속의 자유로운 상태다","J","P"]
];
var C={
INTJ:["🔮","닥터 스트레인지","닥터 스트레인지","1400만 개의 미래를 내다보며 최선의 길을 계산하는 전략가! 목표를 위해서라면 가장 냉철한 선택도 마다하지 않아요.","계획적 · 독립적 · 통찰력"],
INTP:["🍰","L(엘)","데스노트","단서 하나로 끝까지 추리하는 천재 탐구자. 달달한 간식과 함께 머릿속 가설을 굴리는 걸 좋아해요.","호기심 · 분석적 · 독창적"],
ENTJ:["🪽","에르빈 스미스","진격의 거인","확실한 비전으로 사람들을 이끌고 결단을 내리는 지휘관. 목표를 위해 큰 책임도 기꺼이 짊어져요.","리더십 · 결단력 · 추진력"],
ENTP:["🦾","토니 스타크","아이언맨","말발과 재치, 천재적인 아이디어로 불가능을 가능하게 만드는 토론왕. 위기에도 농담이 먼저 나와요.","재치 · 도전적 · 창의적"],
INFJ:["❄️","엘사","겨울왕국","속마음을 깊이 간직하다가 소중한 사람을 위해 큰 결심을 하는 신념가. 겉은 차분해도 마음은 누구보다 따뜻해요.","통찰 · 신념 · 깊은 마음"],
INFP:["🥹","치이카와","치이카와","여리고 순수하지만 소중한 친구들을 위해 용기를 내는 마음 따뜻한 몽상가. 감동도 눈물도 많아요.","순수함 · 이상주의 · 따뜻함"],
ENFJ:["🔔","도라에몽","도라에몽","친구가 곤란할 때마다 먼저 나서서 도와주는 든든한 조력자. 모두가 행복하길 바라는 마음이 커요.","공감 · 포용력 · 친화력"],
ENFP:["🏴‍☠️","잭 스패로우","캐리비안의 해적","자유로운 영혼에 넘치는 매력! 예측 불가한 행동으로 어느새 위기도 기회로 바꿔요.","자유로움 · 열정 · 매력"],
ISTJ:["📚","헤르미온느 그레인저","해리 포터","규칙과 계획을 중시하고 준비성이 철저한 모범생. 위기 때마다 지식과 책임감으로 팀을 구해요.","책임감 · 원칙 · 신뢰"],
ISFJ:["🛡️","캡틴 아메리카","어벤져스","자신보다 동료를 먼저 챙기는 성실한 수호자. 맡은 일은 끝까지 지켜내요.","헌신 · 배려 · 성실"],
ESTJ:["🌑","다스 베이더","스타워즈","강한 추진력과 확실한 질서로 조직을 움직이는 관리자 스타일. 목표를 향해 일사불란하게 밀어붙여요.","체계적 · 단호함 · 추진력"],
ESFJ:["🐱","하치와레","치이카와","친구들을 살뜰히 챙기고 늘 씩씩하게 앞장서는 다정한 분위기 메이커. 함께하는 시간을 제일 소중히 여겨요.","다정함 · 사교적 · 헌신"],
ISTP:["🔫","존 윅","존 윅","말수는 적지만 필요할 땐 완벽하게 해내는 실전형 프로. 군더더기 없이 문제를 해결해요.","침착함 · 실용적 · 냉정함"],
ISFP:["🌱","월-E","월-E","말은 적어도 마음은 누구보다 따뜻한 감성가. 작은 것에서 아름다움을 찾아내요.","감성적 · 온화함 · 순수함"],
ESTP:["🍸","제임스 본드","007 시리즈","위기 앞에서도 여유로운 행동파. 일단 부딪히고 임기응변으로 돌파해요.","대담함 · 임기응변 · 에너지"],
ESFP:["🐼","포","쿵푸팬더","어디서든 분위기를 띄우는 긍정 에너자이저! 즐기다 보니 어느새 용의 전사가 되어 있어요.","유쾌함 · 낙천적 · 친화력"]
};
var idx=0,ans=[];
function $(i){return document.getElementById(i)}
function show(id){document.querySelectorAll(".screen").forEach(function(s){s.classList.remove("on")});$(id).classList.add("on");window.scrollTo(0,0)}
function render(){
  var q=Q[idx];
  $("q-num").textContent=(idx+1)+" / "+Q.length;
  $("q-axis").textContent={EI:"에너지",SN:"인식",TF:"판단",JP:"생활"}[q[0]];
  $("bar").style.width=(idx/Q.length*100)+"%";
  $("q-text").textContent=q[1];
  var box=$("q-opts");box.innerHTML="";
  [[q[2],q[4]],[q[3],q[5]]].forEach(function(o){
    var b=document.createElement("button");b.className="opt";b.textContent=o[0];
    b.onclick=function(){pick(o[1])};box.appendChild(b);
  });
}
function pick(l){
  ans.push(l);idx++;
  if(idx>=Q.length){result()}else{render()}
}
function result(){
  var n={};ans.forEach(function(l){n[l]=(n[l]||0)+1});
  var t="";
  t+=(n.E||0)>(n.I||0)?"E":"I";
  t+=(n.S||0)>(n.N||0)?"S":"N";
  t+=(n.T||0)>(n.F||0)?"T":"F";
  t+=(n.J||0)>(n.P||0)?"J":"P";
  var c=C[t];
  $("r-mbti").textContent=t;$("r-emoji").textContent=c[0];
  $("r-name").textContent=c[1];$("r-movie").textContent="🎞️ "+c[2];
  $("r-desc").textContent=c[3];$("r-trait").textContent="#"+c[4].split(" · ").join(" #");
  $("bar").style.width="100%";
  show("s-res");
}
function start(){idx=0;ans=[];render();show("s-q")}
var back="s-start";
function showAll(from,me){
  back=from;var g=$("all-grid");g.innerHTML="";
  Object.keys(C).forEach(function(k){
    var d=document.createElement("div");d.className="mini"+(me===k?" me":"");
    d.innerHTML="<span>"+C[k][0]+"</span><b>"+k+"</b>"+C[k][1]+"<br><small>"+C[k][2]+"</small>";
    g.appendChild(d);
  });
  show("s-all");
}
$("btn-start").onclick=start;
$("btn-retry").onclick=start;
$("btn-all").onclick=function(){showAll("s-start")};
$("btn-all2").onclick=function(){showAll("s-res",$("r-mbti").textContent)};
$("btn-back").onclick=function(){show(back)};
</script>
</body>
</html>
