<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Word Master">
<title>Word Master</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=DM+Sans:wght@300;400;500;600&display=swap');

  :root {
    --bg: #0f0f13;
    --surface: #1a1a22;
    --surface2: #22222e;
    --accent: #7c6aff;
    --accent2: #ff6a8a;
    --accent3: #6affcf;
    --text: #f0eeff;
    --text2: #9090aa;
    --border: rgba(124,106,255,0.15);
    --card-h: min(62vw, 420px);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; -webkit-tap-highlight-color: transparent; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100dvh;
    overflow-x: hidden;
  }

  /* === TOP NAV === */
  .topnav {
    display: flex; align-items: center; justify-content: space-between;
    padding: 16px 20px 12px;
    position: sticky; top: 0; z-index: 100;
    background: linear-gradient(to bottom, var(--bg) 80%, transparent);
  }
  .app-title {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    background: linear-gradient(135deg, var(--accent), var(--accent2));
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }
  .stats-pill {
    font-size: 12px; color: var(--text2);
    background: var(--surface2); border-radius: 20px;
    padding: 5px 12px; border: 1px solid var(--border);
  }
  .stats-pill span { color: var(--accent3); font-weight: 600; }

  /* === MODE TABS === */
  .mode-tabs {
    display: flex; gap: 8px; padding: 0 20px 16px;
    overflow-x: auto; scrollbar-width: none;
  }
  .mode-tabs::-webkit-scrollbar { display: none; }
  .mode-tab {
    flex-shrink: 0;
    padding: 8px 16px; border-radius: 20px;
    font-size: 13px; font-weight: 500;
    border: 1px solid var(--border);
    background: var(--surface2); color: var(--text2);
    cursor: pointer; transition: all .2s;
  }
  .mode-tab.active {
    background: var(--accent); color: #fff; border-color: var(--accent);
  }

  /* === CARD AREA === */
  .card-section { padding: 0 20px; }

  .progress-bar-wrap { margin-bottom: 12px; }
  .progress-bar-bg {
    height: 4px; background: var(--surface2); border-radius: 4px; overflow: hidden;
  }
  .progress-bar-fill {
    height: 100%; background: linear-gradient(90deg, var(--accent), var(--accent2));
    border-radius: 4px; transition: width .3s ease;
  }
  .progress-label {
    display: flex; justify-content: space-between;
    font-size: 11px; color: var(--text2); margin-top: 4px;
  }

  /* Sort pills */
  .sort-row {
    display: flex; gap: 8px; margin-bottom: 14px;
    overflow-x: auto; scrollbar-width: none;
  }
  .sort-row::-webkit-scrollbar { display: none; }
  .sort-pill {
    flex-shrink: 0;
    font-size: 11px; padding: 5px 12px; border-radius: 20px;
    border: 1px solid var(--border); background: var(--surface2); color: var(--text2);
    cursor: pointer; transition: all .2s;
  }
  .sort-pill.active { border-color: var(--accent3); color: var(--accent3); }

  /* === FLASHCARD === */
  .card-outer {
    perspective: 1200px;
    height: var(--card-h);
    margin-bottom: 16px;
    cursor: pointer;
    user-select: none;
  }
  .card-inner {
    width: 100%; height: 100%;
    position: relative;
    transform-style: preserve-3d;
    transition: transform .5s cubic-bezier(.4,0,.2,1);
    border-radius: 20px;
  }
  .card-inner.flipped { transform: rotateY(180deg); }

  .card-face {
    position: absolute; width: 100%; height: 100%;
    backface-visibility: hidden;
    -webkit-backface-visibility: hidden;
    border-radius: 20px;
    display: flex; flex-direction: column;
    align-items: center; justify-content: center;
    padding: 28px 24px;
    border: 1px solid var(--border);
  }
  .card-front {
    background: linear-gradient(145deg, #1e1b3a 0%, #181826 100%);
  }
  .card-back {
    background: linear-gradient(145deg, #1a2a1e 0%, #181826 100%);
    transform: rotateY(180deg);
    justify-content: flex-start; overflow-y: auto;
    scrollbar-width: none;
  }
  .card-back::-webkit-scrollbar { display: none; }

  .card-face-label {
    font-size: 10px; letter-spacing: 2px; text-transform: uppercase;
    color: var(--text2); margin-bottom: 16px; align-self: flex-start;
  }
  .card-word {
    font-family: 'Playfair Display', serif;
    font-size: clamp(20px, 5vw, 30px);
    text-align: center; line-height: 1.3;
    color: var(--text);
    margin-bottom: 12px;
  }
  .card-example {
    font-size: 13px; color: var(--text2); text-align: center;
    font-style: italic; line-height: 1.6;
    max-height: 80px; overflow: hidden;
  }
  .speak-btn {
    margin-top: 16px;
    background: rgba(124,106,255,0.15); border: 1px solid var(--accent);
    border-radius: 50%; width: 44px; height: 44px;
    display: flex; align-items: center; justify-content: center;
    color: var(--accent); font-size: 18px; cursor: pointer;
    transition: all .2s;
  }
  .speak-btn:active { background: var(--accent); color: #fff; transform: scale(.95); }

  /* back face rows */
  .back-row {
    width: 100%; margin-bottom: 14px;
  }
  .back-row-label {
    font-size: 10px; letter-spacing: 1.5px; text-transform: uppercase;
    color: var(--text2); margin-bottom: 4px;
  }
  .back-row-val {
    font-size: 14px; color: var(--text); line-height: 1.5;
  }
  .back-row-val.big {
    font-size: 20px; font-family: 'Playfair Display', serif; color: var(--accent3);
  }
  .tag { display: inline-block; background: var(--surface2); border-radius: 8px; padding: 2px 8px; margin: 2px; font-size: 12px; color: var(--text2); }

  .tap-hint {
    position: absolute; bottom: 14px; right: 18px;
    font-size: 11px; color: var(--text2); opacity: .6;
  }

  /* === CARD COUNTER === */
  .card-counter { text-align: center; font-size: 12px; color: var(--text2); margin-bottom: 12px; }

  /* === ACTION BTNS === */
  .action-row {
    display: flex; gap: 12px; margin-bottom: 20px;
  }
  .action-btn {
    flex: 1; padding: 14px;
    border-radius: 14px; border: none;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px; font-weight: 600;
    cursor: pointer; transition: all .2s;
    display: flex; align-items: center; justify-content: center; gap: 6px;
  }
  .btn-wrong { background: rgba(255,106,138,0.15); color: var(--accent2); border: 1px solid rgba(255,106,138,0.3); }
  .btn-correct { background: rgba(106,255,207,0.15); color: var(--accent3); border: 1px solid rgba(106,255,207,0.3); }
  .btn-wrong:active { background: var(--accent2); color: #fff; }
  .btn-correct:active { background: var(--accent3); color: #222; }

  .nav-row {
    display: flex; gap: 12px;
  }
  .nav-btn {
    flex: 1; padding: 12px;
    border-radius: 12px; border: 1px solid var(--border);
    background: var(--surface2); color: var(--text2);
    font-family: 'DM Sans', sans-serif;
    font-size: 14px; cursor: pointer; transition: all .2s;
  }
  .nav-btn:active { background: var(--surface); color: var(--text); }

  /* === LIST VIEW === */
  .list-section { padding: 0 20px; }
  .search-wrap { margin-bottom: 14px; }
  .search-input {
    width: 100%; background: var(--surface2); border: 1px solid var(--border);
    border-radius: 12px; padding: 11px 16px;
    color: var(--text); font-family: 'DM Sans', sans-serif; font-size: 14px;
    outline: none;
  }
  .search-input::placeholder { color: var(--text2); }
  .search-input:focus { border-color: var(--accent); }

  .word-list { display: flex; flex-direction: column; gap: 8px; max-height: 65vh; overflow-y: auto; scrollbar-width: thin; scrollbar-color: var(--surface2) transparent; }
  .word-item {
    background: var(--surface2); border-radius: 12px; border: 1px solid var(--border);
    padding: 12px 16px; display: flex; align-items: center; justify-content: space-between;
    cursor: pointer; transition: all .2s;
  }
  .word-item:active { background: var(--surface); border-color: var(--accent); }
  .word-item-left .wi-word { font-size: 15px; font-weight: 500; margin-bottom: 3px; }
  .word-item-left .wi-meaning { font-size: 12px; color: var(--text2); }
  .word-item-right {
    display: flex; flex-direction: column; align-items: flex-end; gap: 4px;
  }
  .wi-views { font-size: 11px; color: var(--text2); }
  .wi-correct { font-size: 11px; }
  .wi-correct.good { color: var(--accent3); }
  .wi-correct.bad { color: var(--accent2); }
  .wi-correct.none { color: var(--text2); }

  /* === STATS VIEW === */
  .stats-section { padding: 0 20px; }
  .stat-card {
    background: var(--surface2); border-radius: 16px; border: 1px solid var(--border);
    padding: 20px; margin-bottom: 12px;
  }
  .stat-card-title { font-size: 12px; letter-spacing: 1.5px; text-transform: uppercase; color: var(--text2); margin-bottom: 8px; }
  .stat-card-val { font-family: 'Playfair Display', serif; font-size: 36px; }
  .stat-card-val .unit { font-family: 'DM Sans', sans-serif; font-size: 14px; color: var(--text2); margin-left: 4px; }

  .donut-wrap { display: flex; align-items: center; gap: 20px; }
  canvas#donut { width: 80px !important; height: 80px !important; flex-shrink: 0; }
  .donut-legend { flex: 1; }
  .legend-row { display: flex; align-items: center; gap: 8px; margin-bottom: 6px; font-size: 13px; }
  .legend-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }

  /* hidden */
  .view { display: none; }
  .view.active { display: block; }

  /* bottom nav */
  .bottom-nav {
    position: fixed; bottom: 0; left: 0; right: 0;
    background: var(--bg);
    border-top: 1px solid var(--border);
    display: flex; z-index: 100;
    padding-bottom: env(safe-area-inset-bottom);
  }
  .bnav-item {
    flex: 1; display: flex; flex-direction: column; align-items: center;
    padding: 10px 0 8px; cursor: pointer; transition: all .2s;
    color: var(--text2); font-size: 10px; gap: 3px;
  }
  .bnav-item .icon { font-size: 20px; }
  .bnav-item.active { color: var(--accent); }

  .main-content { padding-bottom: calc(70px + env(safe-area-inset-bottom)); }

  /* toast */
  .toast {
    position: fixed; bottom: 90px; left: 50%; transform: translateX(-50%) translateY(20px);
    background: var(--surface2); border: 1px solid var(--border); border-radius: 12px;
    padding: 10px 20px; font-size: 13px; color: var(--text);
    opacity: 0; transition: all .3s; pointer-events: none; z-index: 200;
    white-space: nowrap;
  }
  .toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }

  /* Swipe animation */
  @keyframes swipeLeft { to { transform: translateX(-120%) rotate(-15deg); opacity: 0; } }
  @keyframes swipeRight { to { transform: translateX(120%) rotate(15deg); opacity: 0; } }
  .swiping-left .card-outer { animation: swipeLeft .3s forwards; }
  .swiping-right .card-outer { animation: swipeRight .3s forwards; }
</style>
</head>
<body>

<div class="topnav">
  <div class="app-title">Word Master</div>
  <div class="stats-pill" id="headerStats"><span id="hCorrect">0</span> / <span id="hTotal">770</span></div>
</div>

<div class="main-content">

<!-- ===== STUDY VIEW ===== -->
<div class="view active" id="view-study">
  <div class="mode-tabs">
    <div class="mode-tab active" onclick="setMode('random')" id="tab-random">🔀 ランダム</div>
    <div class="mode-tab" onclick="setMode('unseen')" id="tab-unseen">👁 未閲覧</div>
    <div class="mode-tab" onclick="setMode('wrong')" id="tab-wrong">❌ 不正解</div>
    <div class="mode-tab" onclick="setMode('correct')" id="tab-correct">✅ 正解済</div>
  </div>

  <div class="card-section">
    <div class="progress-bar-wrap">
      <div class="progress-bar-bg"><div class="progress-bar-fill" id="progressFill" style="width:0%"></div></div>
      <div class="progress-label"><span id="progressLeft">セッション開始</span><span id="progressRight">0%</span></div>
    </div>

    <div class="sort-row">
      <div class="sort-pill active" onclick="setSortMode('random')" id="sort-random">🔀 ランダム</div>
      <div class="sort-pill" onclick="setSortMode('views')" id="sort-views">👁 閲覧回数順</div>
      <div class="sort-pill" onclick="setSortMode('accuracy')" id="sort-accuracy">📊 正解率順</div>
    </div>

    <div class="card-counter" id="cardCounter">1 / 770</div>

    <div class="card-outer" id="cardOuter" onclick="flipCard()">
      <div class="card-inner" id="cardInner">
        <!-- FRONT -->
        <div class="card-face card-front">
          <div class="card-face-label">FACE 1 — WORD</div>
          <div class="card-word" id="cf-word">Loading...</div>
          <div class="card-example" id="cf-example"></div>
          <div class="speak-btn" onclick="speakWord(event)" title="読み上げ">🔊</div>
          <div class="tap-hint">タップして裏返す</div>
        </div>
        <!-- BACK -->
        <div class="card-face card-back" id="cardBack">
          <div class="card-face-label" style="margin-bottom:12px">FACE 2 — MEANING</div>
          <div class="back-row">
            <div class="back-row-label">English Meaning</div>
            <div class="back-row-val big" id="cb-meaning">—</div>
          </div>
          <div class="back-row">
            <div class="back-row-label">日本語</div>
            <div class="back-row-val" id="cb-japanese">—</div>
          </div>
          <div class="back-row">
            <div class="back-row-label">Example</div>
            <div class="back-row-val" id="cb-example" style="font-style:italic;color:var(--text2);font-size:13px;">—</div>
          </div>
          <div class="back-row">
            <div class="back-row-label">FACE 3 — FORMS & SYNONYMS</div>
            <div class="back-row-val" id="cb-forms">—</div>
          </div>
          <div style="height:20px;flex-shrink:0"></div>
        </div>
      </div>
    </div>

    <div class="action-row" id="actionRow" style="display:none">
      <button class="action-btn btn-wrong" onclick="markAnswer(false)">❌ 不正解</button>
      <button class="action-btn btn-correct" onclick="markAnswer(true)">✅ 正解</button>
    </div>

    <div class="nav-row">
      <button class="nav-btn" onclick="prevCard()">← 前へ</button>
      <button class="nav-btn" onclick="nextCard()">次へ →</button>
    </div>
  </div>
</div>

<!-- ===== LIST VIEW ===== -->
<div class="view" id="view-list">
  <div class="list-section">
    <div class="search-wrap">
      <input class="search-input" id="searchInput" type="search" placeholder="🔍 単語を検索..." oninput="filterList()">
    </div>
    <div class="word-list" id="wordList"></div>
  </div>
</div>

<!-- ===== STATS VIEW ===== -->
<div class="view" id="view-stats">
  <div class="stats-section">
    <div class="stat-card">
      <div class="stat-card-title">総単語数</div>
      <div class="stat-card-val" id="stat-total">770<span class="unit">語</span></div>
    </div>
    <div class="stat-card">
      <div class="stat-card-title">閲覧済み</div>
      <div class="stat-card-val" id="stat-viewed">0<span class="unit">語</span></div>
    </div>
    <div class="stat-card">
      <div class="stat-card-title">正答率</div>
      <div class="donut-wrap">
        <canvas id="donut" width="80" height="80"></canvas>
        <div class="donut-legend">
          <div class="legend-row"><div class="legend-dot" style="background:var(--accent3)"></div><span id="leg-correct">正解: 0語</span></div>
          <div class="legend-row"><div class="legend-dot" style="background:var(--accent2)"></div><span id="leg-wrong">不正解: 0語</span></div>
          <div class="legend-row"><div class="legend-dot" style="background:var(--surface2)"></div><span id="leg-unseen">未学習: 770語</span></div>
        </div>
      </div>
    </div>
    <div class="stat-card">
      <div class="stat-card-title">セッション</div>
      <div class="stat-card-val" id="stat-session">0<span class="unit">回答</span></div>
    </div>
    <button onclick="resetProgress()" style="width:100%;padding:14px;border-radius:14px;border:1px solid rgba(255,106,138,.3);background:rgba(255,106,138,.08);color:var(--accent2);font-family:'DM Sans',sans-serif;font-size:14px;cursor:pointer;font-weight:600;margin-bottom:20px;">
      🗑 進捗をリセット
    </button>
  </div>
</div>

</div><!-- /main-content -->

<!-- Bottom Nav -->
<div class="bottom-nav">
  <div class="bnav-item active" onclick="switchView('study')" id="bnav-study">
    <div class="icon">📚</div><span>学習</span>
  </div>
  <div class="bnav-item" onclick="switchView('list')" id="bnav-list">
    <div class="icon">📋</div><span>一覧</span>
  </div>
  <div class="bnav-item" onclick="switchView('stats')" id="bnav-stats">
    <div class="icon">📊</div><span>統計</span>
  </div>
</div>

<div class="toast" id="toast"></div>

<script>
// ============================================================
// DATA — 770 words embedded
// ============================================================
const RAW = [{"word":"~years ahead of me","example":"","meaning":"having more experience or progress by a number of years","synonyms":"far more experienced","antonyms":"behind","verbForm":"—","nounForm":"—","japanese":""},{"word":"a possible solution","example":"A possible solution to this problem is to increase communication","meaning":"an option that might solve a problem","synonyms":"potential answer","antonyms":"no solution","verbForm":"solve","nounForm":"solution","japanese":"可能な解決策"},{"word":"accidentally","example":"I accidentally deleted the range of the sheet","meaning":"in a way that is not planned or intended","synonyms":"unintentionally","antonyms":"intentionally","verbForm":"—","nounForm":"accident","japanese":""},{"word":"accumulate","example":"","meaning":"to gradually collect or gather over time","synonyms":"gather, build up","antonyms":"reduce","verbForm":"accumulate","nounForm":"accumulation","japanese":""},{"word":"acquisition","example":"then you will acquire the language unconsciously","meaning":"the act of getting or obtaining something","synonyms":"purchase, gain","antonyms":"loss","verbForm":"acquire","nounForm":"acquisition","japanese":"習得"},{"word":"accuse","example":"","meaning":"to say someone did something wrong or illegal","synonyms":"blame","antonyms":"defend","verbForm":"accuse","nounForm":"accusation","japanese":""},{"word":"adapt to","example":"She adapted to her new work","meaning":"to change in order to fit new conditions","synonyms":"adjust","antonyms":"resist","verbForm":"adapt","nounForm":"adaptation","japanese":"適応する"},{"word":"address","example":"We need to address the issues in our project","meaning":"to deal with or discuss a problem","synonyms":"handle, tackle","antonyms":"ignore","verbForm":"address","nounForm":"address","japanese":"対処する"},{"word":"adjust your message","example":"We need to adjust our message based on who we're speaking to","meaning":"to change how you communicate depending on the situation","synonyms":"modify","antonyms":"keep unchanged","verbForm":"adjust","nounForm":"adjustment","japanese":"speak to"},{"word":"advance farthest","example":"We tried to predict which children would advance farthest in competition","meaning":"to move forward more than others","synonyms":"progress most","antonyms":"fall behind","verbForm":"advance","nounForm":"advancement","japanese":"進む"},{"word":"adversity","example":"Regardless of the adversity","meaning":"difficulties or hardships","synonyms":"hardship","antonyms":"prosperity","verbForm":"—","nounForm":"adversity","japanese":"逆境"},{"word":"after ~ing / before ~ing","example":"","meaning":"used to show timing of actions","synonyms":"—","antonyms":"—","verbForm":"—","nounForm":"—","japanese":""},{"word":"ahead of time","example":"We finished the project ahead of time","meaning":"earlier than expected or scheduled","synonyms":"in advance","antonyms":"late","verbForm":"—","nounForm":"—","japanese":"予定より早く、事前に"},{"word":"aim to","example":"I aim to become fluent in English within a year","meaning":"to intend or plan to do something","synonyms":"intend","antonyms":"neglect","verbForm":"aim","nounForm":"aim","japanese":""},{"word":"align","example":"The left eye of the patient and the right eye of the examiner are aligned","meaning":"to arrange in a straight line or agree","synonyms":"coordinate","antonyms":"misalign","verbForm":"align","nounForm":"alignment","japanese":""},{"word":"all at once","example":"","meaning":"suddenly or at the same time","synonyms":"suddenly","antonyms":"gradually","verbForm":"—","nounForm":"—","japanese":""},{"word":"all over the world","example":"My job is to talk to people from all walks of life, all over the world","meaning":"in every part of the world","synonyms":"worldwide","antonyms":"locally","verbForm":"—","nounForm":"—","japanese":"世界中で"},{"word":"all walks of life","example":"My job is to talk to people from all walks of life, all over the world","meaning":"people from all backgrounds","synonyms":"all kinds of people","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"あらゆる職業や生活環境の人々"},{"word":"alleviate tensions","example":"Why didn't Barack Obama's presidency alleviate racial tensions in our country?","meaning":"to reduce stress or conflict","synonyms":"ease, relieve","antonyms":"worsen","verbForm":"alleviate","nounForm":"alleviation","japanese":"緊張を和らげる"},{"word":"allow A to do","example":"You're not allowed to talk during the exam","meaning":"to permit someone to do something","synonyms":"permit","antonyms":"forbid","verbForm":"allow","nounForm":"allowance","japanese":""},{"word":"and stuff","example":"We've got to do editing and stuff","meaning":"informal way to refer to similar things","synonyms":"and so on","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～とか"},{"word":"appear to be","example":"The results appear to be within the normal range","meaning":"to seem or look like something","synonyms":"seem","antonyms":"be certain","verbForm":"appear","nounForm":"appearance","japanese":""},{"word":"apply","example":"Apply this rule to the case / She applied for admission to law school","meaning":"to request or use","synonyms":"request, use","antonyms":"withdraw","verbForm":"apply","nounForm":"application","japanese":"応用する、適用する / 申し込む"},{"word":"approach","example":"He carefully approached the wild animal / We need a new approach","meaning":"a way of dealing with something","synonyms":"method","antonyms":"avoidance","verbForm":"approach","nounForm":"approach","japanese":"近づく、取り組む"},{"word":"arrogance","example":"There is a difference between arrogance","meaning":"having an overly high opinion of oneself","synonyms":"pride","antonyms":"humility","verbForm":"—","nounForm":"arrogance","japanese":"傲慢"},{"word":"as a result","example":"He studied hard; as a result, he passed the exam","meaning":"because of something","synonyms":"therefore","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"結果として"},{"word":"as dumb as a post","example":"I am about as dumb as a post when it comes to numbers","meaning":"extremely stupid (informal)","synonyms":"very foolish","antonyms":"intelligent","verbForm":"—","nounForm":"—","japanese":"木のように愚かだ"},{"word":"as far as I remember","example":"As far as I remember, he didn't say anything about that","meaning":"based on what I recall","synonyms":"to my knowledge","antonyms":"—","verbForm":"remember","nounForm":"memory","japanese":"覚えている限りでは"},{"word":"as hell","example":"It was hot as hell during the summer","meaning":"very (informal emphasis)","synonyms":"extremely","antonyms":"slightly","verbForm":"—","nounForm":"—","japanese":"非常に"},{"word":"as quickly as possible","example":"They were determined to end the war as quickly as possible","meaning":"as fast as you can","synonyms":"immediately","antonyms":"slowly","verbForm":"—","nounForm":"—","japanese":"as soon as possible"},{"word":"as to","example":"I want to make a decision as to which university I want to attend","meaning":"concerning or about","synonyms":"regarding","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～に関して / フォーマルな表現"},{"word":"ask for help","example":"This little girl asked me for help","meaning":"to request assistance","synonyms":"seek help","antonyms":"refuse help","verbForm":"ask","nounForm":"request","japanese":"助けを求める"},{"word":"aspect","example":"You've only considered one aspect of this problem","meaning":"a part or feature of something","synonyms":"element","antonyms":"whole","verbForm":"—","nounForm":"aspect","japanese":"面、様相、局面"},{"word":"aspire (to do something)","example":"","meaning":"to strongly hope to achieve something","synonyms":"aim","antonyms":"give up","verbForm":"aspire","nounForm":"aspiration","japanese":""},{"word":"assume","example":"Let's assume that they're coming and make plans on that basis","meaning":"to think something is true without proof","synonyms":"suppose","antonyms":"know","verbForm":"assume","nounForm":"assumption","japanese":""},{"word":"astound","example":"You will be astounded at how good you are","meaning":"to surprise greatly","synonyms":"amaze","antonyms":"bore","verbForm":"astound","nounForm":"astonishment","japanese":"驚かせる"},{"word":"at a young age","example":"Many successful entrepreneurs start their businesses at a young age","meaning":"when someone is young","synonyms":"early in life","antonyms":"late in life","verbForm":"—","nounForm":"age","japanese":"若い頃に、若い年齢で"},{"word":"at all","example":"","meaning":"used for emphasis in negatives or questions","synonyms":"—","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"ちょっとでも / (否) 全く～ない"},{"word":"at risk","example":"Kids at risk for dropping out","meaning":"in danger of harm","synonyms":"in danger","antonyms":"safe","verbForm":"—","nounForm":"risk","japanese":"危険にさらされて"},{"word":"at the end of the day","example":"At the end of the day, this is not that important","meaning":"ultimately; after considering everything","synonyms":"finally","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"Eventually / in the end / after all"},{"word":"at your own pace","example":"You should do things at your own pace","meaning":"at a speed comfortable for you","synonyms":"freely","antonyms":"rushed","verbForm":"—","nounForm":"pace","japanese":"自分のペースで"},{"word":"attempt","example":"He attempted a joke, but no one laughed","meaning":"to try to do something","synonyms":"try","antonyms":"avoid","verbForm":"attempt","nounForm":"attempt","japanese":""},{"word":"authentic","example":"I believe that Bible story is authentic","meaning":"real and genuine","synonyms":"genuine","antonyms":"fake","verbForm":"authenticate","nounForm":"authenticity","japanese":""},{"word":"authority","example":"The doctors have too much authority — I can't do anything without their approval","meaning":"power or right to control or decide","synonyms":"control","antonyms":"subordination","verbForm":"authorize","nounForm":"authority","japanese":""},{"word":"avoid","example":"I always avoid taking the train during rush hour","meaning":"to stay away from something","synonyms":"evade","antonyms":"face","verbForm":"avoid","nounForm":"avoidance","japanese":"避ける"},{"word":"back to square one","example":"We have to go back to square one","meaning":"to start again from the beginning","synonyms":"restart","antonyms":"finish","verbForm":"—","nounForm":"—","japanese":""},{"word":"balance","example":"I struggle to balance work and family commitments","meaning":"a state where things are equal or stable","synonyms":"equilibrium","antonyms":"imbalance","verbForm":"balance","nounForm":"balance","japanese":""},{"word":"basically","example":"Basically, they want a lot more information about the project","meaning":"in a simple or general way","synonyms":"essentially","antonyms":"specifically","verbForm":"—","nounForm":"basis","japanese":""},{"word":"be disappointed that","example":"","meaning":"to feel sad because something did not meet expectations","synonyms":"feel let down","antonyms":"be satisfied","verbForm":"disappoint","nounForm":"disappointment","japanese":""},{"word":"be fond of","example":"","meaning":"to like something or someone","synonyms":"like","antonyms":"dislike","verbForm":"—","nounForm":"fondness","japanese":""},{"word":"be gritty about","example":"We need to be gritty about getting our kids grittier","meaning":"to show determination in a situation","synonyms":"be determined","antonyms":"give up","verbForm":"—","nounForm":"grit","japanese":"根気強く取り組む"},{"word":"be interested in","example":"She is interested in learning French","meaning":"to want to know or learn about something","synonyms":"be curious about","antonyms":"uninterested","verbForm":"—","nounForm":"interest","japanese":"～に興味がある"},{"word":"be into","example":"I'm really into you / I'm into watching TV","meaning":"to be very interested in","synonyms":"be keen on","antonyms":"dislike","verbForm":"—","nounForm":"interest","japanese":"～にハマっている"},{"word":"be jealous of A","example":"I'm jealous of them because they had a privileged upbringing","meaning":"to feel envy toward someone","synonyms":"envy","antonyms":"admire","verbForm":"—","nounForm":"jealousy","japanese":"Aを羨ましく思う / 嫉妬する"},{"word":"be passionate about A","example":"I'm passionate about boxing","meaning":"to have strong feelings about something","synonyms":"be enthusiastic","antonyms":"indifferent","verbForm":"—","nounForm":"passion","japanese":""},{"word":"be patient (with)","example":"It takes time to become a good English speaker. You just have to be patient","meaning":"to stay calm and tolerant","synonyms":"be tolerant","antonyms":"be impatient","verbForm":"—","nounForm":"patience","japanese":"我慢する / 耐える"},{"word":"be responsible for","example":"I think it's important to be responsible for your work","meaning":"to be in charge of something","synonyms":"be accountable","antonyms":"irresponsible","verbForm":"—","nounForm":"responsibility","japanese":""},{"word":"be seen as human beings","example":"I tried to make people see them as human beings","meaning":"to be recognized as people with dignity","synonyms":"be regarded as human","antonyms":"dehumanize","verbForm":"see","nounForm":"perception","japanese":"人間として見られる"},{"word":"before and after","example":"Let's be humanists, before and after everything else","meaning":"showing change over time","synonyms":"prior and subsequent","antonyms":"—","verbForm":"—","nounForm":"—","japanese":""},{"word":"begin by","example":"","meaning":"to start with something","synonyms":"start with","antonyms":"finish with","verbForm":"begin","nounForm":"beginning","japanese":""},{"word":"believe in yourself","example":"No one believes in you unless you believe in you","meaning":"to have confidence in oneself","synonyms":"trust yourself","antonyms":"doubt yourself","verbForm":"believe","nounForm":"belief","japanese":"自分を信じる"},{"word":"believe it or not","example":"She slapped his face in front of everyone, believe it or not","meaning":"used to express surprise","synonyms":"surprisingly","antonyms":"—","verbForm":"believe","nounForm":"belief","japanese":"信じられないだろうけど"},{"word":"beyond a shadow of a doubt","example":"It was clear beyond a shadow of a doubt that she was the right choice","meaning":"completely certain","synonyms":"undoubtedly","antonyms":"uncertain","verbForm":"—","nounForm":"doubt","japanese":"疑いの余地なく"},{"word":"beyond belief","example":"Her recovery was beyond belief","meaning":"extremely surprising","synonyms":"unbelievable","antonyms":"believable","verbForm":"—","nounForm":"belief","japanese":"信じられないほど"},{"word":"beyond comprehension","example":"The complexity of the issue was beyond comprehension","meaning":"impossible to understand","synonyms":"incomprehensible","antonyms":"understandable","verbForm":"—","nounForm":"comprehension","japanese":"理解を超えている"},{"word":"beyond control","example":"The situation quickly spiraled beyond control","meaning":"cannot be managed","synonyms":"uncontrollable","antonyms":"controllable","verbForm":"control","nounForm":"control","japanese":"制御不能の"},{"word":"beyond imagination","example":"The beauty of the place was beyond imagination","meaning":"extremely surprising","synonyms":"unimaginable","antonyms":"imaginable","verbForm":"imagine","nounForm":"imagination","japanese":"想像を超えている"},{"word":"beyond recognition","example":"The building had changed beyond recognition after the renovation","meaning":"changed so much it cannot be recognized","synonyms":"unrecognizable","antonyms":"recognizable","verbForm":"recognize","nounForm":"recognition","japanese":"認識できないほど"},{"word":"beyond repair","example":"The damage was beyond repair","meaning":"cannot be fixed","synonyms":"irreparable","antonyms":"repairable","verbForm":"repair","nounForm":"repair","japanese":"修復不能の"},{"word":"beyond the pale","example":"His actions were beyond the pale","meaning":"unacceptable or inappropriate","synonyms":"intolerable","antonyms":"acceptable","verbForm":"—","nounForm":"—","japanese":"常識を超えている"},{"word":"beyond words","example":"The experience was beyond words","meaning":"too strong for words","synonyms":"indescribable","antonyms":"expressible","verbForm":"—","nounForm":"—","japanese":"言葉では表現できないほど"},{"word":"boost","example":"I tried really hard to fit in at the new school","meaning":"to increase or improve","synonyms":"enhance","antonyms":"reduce","verbForm":"boost","nounForm":"boost","japanese":"高める / 促進する"},{"word":"brain soaking","example":"Listen a lot — I call it brain soaking","meaning":"passive absorption of information","synonyms":"passive learning","antonyms":"active learning","verbForm":"soak","nounForm":"—","japanese":"脳浸透"},{"word":"break down","example":"Break down the skill into smaller pieces","meaning":"to divide or stop functioning","synonyms":"analyze","antonyms":"function","verbForm":"break down","nounForm":"breakdown","japanese":"細分化する"},{"word":"brush it off","example":"I tried to brush it off, but it still bothered me","meaning":"to ignore something trivial","synonyms":"dismiss","antonyms":"take seriously","verbForm":"brush off","nounForm":"—","japanese":"気にしない"},{"word":"build connection","example":"I've been struggling to build connections with others","meaning":"to form relationships","synonyms":"connect","antonyms":"isolate","verbForm":"build","nounForm":"connection","japanese":""},{"word":"build over time","example":"You build it over time","meaning":"to gradually develop","synonyms":"grow","antonyms":"decline","verbForm":"build","nounForm":"buildup","japanese":"時間をかけて築く"},{"word":"bump into","example":"I bumped into your younger brother at the store","meaning":"to meet unexpectedly","synonyms":"run into","antonyms":"avoid","verbForm":"bump into","nounForm":"—","japanese":"ぶつかる / 偶然会う"},{"word":"burst the bubble","example":"The only way is to burst the bubble","meaning":"to destroy a false belief","synonyms":"disillusion","antonyms":"encourage","verbForm":"burst","nounForm":"—","japanese":"バブルを壊す"},{"word":"by accident / by chance","example":"","meaning":"not planned","synonyms":"accidentally","antonyms":"intentionally","verbForm":"—","nounForm":"accident","japanese":""},{"word":"by mistake","example":"I believe that this email was sent by mistake","meaning":"done wrongly","synonyms":"incorrectly","antonyms":"correctly","verbForm":"—","nounForm":"mistake","japanese":"誤って / 間違えて"},{"word":"call","example":"I'll call you later tonight","meaning":"to phone or name","synonyms":"phone","antonyms":"ignore","verbForm":"call","nounForm":"call","japanese":"電話する"},{"word":"can't accept","example":"I can't accept that I failed the exam","meaning":"unable to agree","synonyms":"reject","antonyms":"accept","verbForm":"accept","nounForm":"acceptance","japanese":"耐えられない / 我慢できない"},{"word":"can't believe","example":"I can't believe that I couldn't perform when it counted","meaning":"to feel surprised","synonyms":"astonished","antonyms":"expect","verbForm":"believe","nounForm":"belief","japanese":"信じられない"},{"word":"can't stand","example":"I can't stand working these crazy hours anymore","meaning":"to strongly dislike","synonyms":"hate","antonyms":"like","verbForm":"stand","nounForm":"—","japanese":"我慢できない（強い嫌悪感）"},{"word":"cannot be underestimated","example":"The importance of putting myself in other people's shoes cannot be underestimated","meaning":"very important","synonyms":"significant","antonyms":"trivial","verbForm":"underestimate","nounForm":"underestimation","japanese":"過小評価できない"},{"word":"capture the attention","example":"It's always challenging to capture the audience's attention right from the start","meaning":"to attract focus","synonyms":"grab attention","antonyms":"bore","verbForm":"capture","nounForm":"attention","japanese":""},{"word":"carry on","example":"Sorry to interrupt, please carry on","meaning":"to continue","synonyms":"continue","antonyms":"stop","verbForm":"carry on","nounForm":"continuation","japanese":""},{"word":"catchy","example":"How about creating a catchy new slogan for the rebrand?","meaning":"easy to remember","synonyms":"memorable","antonyms":"forgettable","verbForm":"—","nounForm":"catchiness","japanese":""},{"word":"celebrate those imperfections","example":"Let's celebrate those imperfections that make us special","meaning":"to accept flaws positively","synonyms":"embrace flaws","antonyms":"reject","verbForm":"celebrate","nounForm":"celebration","japanese":"私たちを特別にしているその不完全さを祝おう"},{"word":"censor","example":"Censorship was growing","meaning":"to remove inappropriate content","synonyms":"suppress","antonyms":"allow","verbForm":"censor","nounForm":"censorship","japanese":"検閲"},{"word":"characteristic","example":"One characteristic emerged as a significant predictor of success","meaning":"a typical feature","synonyms":"trait","antonyms":"anomaly","verbForm":"characterize","nounForm":"characteristic","japanese":"特徴"},{"word":"choose the path","example":"He chose that path simply because he had no other choice","meaning":"to make a decision","synonyms":"decide","antonyms":"hesitate","verbForm":"choose","nounForm":"choice","japanese":""},{"word":"clear","example":"I'm not at all clear about what I want to do with my life","meaning":"easy to understand","synonyms":"obvious","antonyms":"unclear","verbForm":"clear","nounForm":"clarity","japanese":""},{"word":"clueless","example":"I was clueless","meaning":"having no understanding","synonyms":"ignorant","antonyms":"informed","verbForm":"—","nounForm":"—","japanese":""},{"word":"come across","example":"I came across this book at the bookstore","meaning":"to seem or find by chance","synonyms":"appear","antonyms":"miss","verbForm":"come across","nounForm":"—","japanese":"偶然出会う"},{"word":"come full circle","example":"It felt like everything had come full circle when I returned home","meaning":"to return to starting point","synonyms":"return","antonyms":"diverge","verbForm":"—","nounForm":"—","japanese":"一巡して元に戻る"},{"word":"come to terms with","example":"I began to come to terms with how these experiences were changing me","meaning":"to accept reality","synonyms":"accept","antonyms":"deny","verbForm":"come","nounForm":"terms","japanese":"受け入れる"},{"word":"come up to me","example":"My dad came up to me and said…","meaning":"to approach someone","synonyms":"approach","antonyms":"avoid","verbForm":"come","nounForm":"—","japanese":"近づいてきた、話しかけてきた"},{"word":"comparatively","example":"Comparatively speaking, this machine is easy to use","meaning":"relatively","synonyms":"relatively","antonyms":"absolutely","verbForm":"—","nounForm":"comparison","japanese":"比較的に"},{"word":"compatible","example":"We found we just weren't compatible","meaning":"able to work together","synonyms":"consistent","antonyms":"incompatible","verbForm":"—","nounForm":"compatibility","japanese":""},{"word":"compulsory","example":"","meaning":"required by law or rule","synonyms":"mandatory","antonyms":"optional","verbForm":"compel","nounForm":"compulsion","japanese":""},{"word":"compose","example":"","meaning":"to create or calm oneself","synonyms":"create","antonyms":"destroy","verbForm":"compose","nounForm":"composition","japanese":"構成する / 作曲する / 気を落ち着ける"},{"word":"compromise","example":"He won't compromise on anything","meaning":"to settle by mutual concession","synonyms":"settle","antonyms":"refuse","verbForm":"compromise","nounForm":"compromise","japanese":"妥協する / 譲歩する"},{"word":"conceit","example":"There is a difference between conceit","meaning":"excessive pride","synonyms":"arrogance","antonyms":"humility","verbForm":"—","nounForm":"conceit","japanese":"自惚れ"},{"word":"concerning","example":"I received an email concerning your application","meaning":"about or worrying","synonyms":"regarding","antonyms":"—","verbForm":"concern","nounForm":"concern","japanese":"～に関して"},{"word":"concise","example":"The fewer words you use, the more concise your message can be","meaning":"brief and clear","synonyms":"succinct","antonyms":"verbose","verbForm":"—","nounForm":"conciseness","japanese":""},{"word":"connect with nature","example":"I went to Ha Giang, and enjoyed connecting with nature","meaning":"to feel close to nature","synonyms":"bond with nature","antonyms":"disconnect","verbForm":"connect","nounForm":"connection","japanese":"自然と触れ合う"},{"word":"consist of","example":"","meaning":"to be made of","synonyms":"be composed of","antonyms":"exclude","verbForm":"consist","nounForm":"—","japanese":""},{"word":"contradict","example":"His actions contradict his words","meaning":"to say the opposite","synonyms":"oppose","antonyms":"agree","verbForm":"contradict","nounForm":"contradiction","japanese":"矛盾する"},{"word":"count on","example":"You can count on me","meaning":"to rely on","synonyms":"depend on","antonyms":"doubt","verbForm":"count","nounForm":"—","japanese":"頼る、任せる"},{"word":"courage","example":"It takes courage to show respect","meaning":"ability to face fear","synonyms":"bravery","antonyms":"fear","verbForm":"encourage","nounForm":"courage","japanese":"勇気"},{"word":"criteria","example":"We need to establish clear criteria for evaluation","meaning":"standards for judgment","synonyms":"standards","antonyms":"—","verbForm":"—","nounForm":"criterion","japanese":"基準"},{"word":"daydreaming","example":"I remember daydreaming on the plane about the American high school experience","meaning":"thinking about pleasant things","synonyms":"fantasizing","antonyms":"focusing","verbForm":"daydream","nounForm":"daydream","japanese":"空想にふける"},{"word":"deal with","example":"It's just something that I have to deal with","meaning":"to handle a situation","synonyms":"manage","antonyms":"ignore","verbForm":"deal","nounForm":"deal","japanese":"～を対処する / 処理する"},{"word":"decline","example":"She politely declined my invitation","meaning":"to decrease or refuse","synonyms":"decrease","antonyms":"increase","verbForm":"decline","nounForm":"decline","japanese":"丁寧だけどきっぱり"},{"word":"deconstruct","example":"The first is to deconstruct the skill","meaning":"to break into parts","synonyms":"analyze","antonyms":"construct","verbForm":"deconstruct","nounForm":"deconstruction","japanese":"分解する"},{"word":"deliberate","example":"If you put 20 hours of focused deliberate practice into that thing","meaning":"careful and intentional","synonyms":"intentional","antonyms":"accidental","verbForm":"deliberate","nounForm":"deliberation","japanese":"故意の、意図的な"},{"word":"deliberately","example":"He deliberately ignored my message","meaning":"on purpose","synonyms":"intentionally","antonyms":"accidentally","verbForm":"—","nounForm":"deliberation","japanese":"慎重に、わざと"},{"word":"demanding","example":"I left a very demanding job in management consulting","meaning":"requiring effort","synonyms":"challenging","antonyms":"easy","verbForm":"demand","nounForm":"demand","japanese":"(あまりにも)多くを要求する、過酷な"},{"word":"denigrate","example":"You shouldn't denigrate people just because they have different beliefs","meaning":"to criticize unfairly","synonyms":"belittle","antonyms":"praise","verbForm":"denigrate","nounForm":"denigration","japanese":""},{"word":"depart","example":"Next week I'm gonna depart from Japan","meaning":"to leave","synonyms":"leave","antonyms":"arrive","verbForm":"depart","nounForm":"departure","japanese":"出発する（Formal）"},{"word":"despite","example":"Despite repeated assurances that the product is safe, many people have stopped buying it","meaning":"without being affected by","synonyms":"in spite of","antonyms":"because of","verbForm":"—","nounForm":"—","japanese":""},{"word":"deteriorate","example":"The political situation in the region has deteriorated rapidly","meaning":"to become worse","synonyms":"worsen","antonyms":"improve","verbForm":"deteriorate","nounForm":"deterioration","japanese":""},{"word":"detour","example":"We had to take a detour due to road construction","meaning":"a longer route","synonyms":"diversion","antonyms":"direct route","verbForm":"detour","nounForm":"detour","japanese":"回り道、迂回する"},{"word":"develop","example":"Just get straight to the point","meaning":"to grow or improve","synonyms":"grow","antonyms":"decline","verbForm":"develop","nounForm":"development","japanese":"発展させる / 成長する"},{"word":"diligent","example":"Leo is very diligent in his work","meaning":"hardworking","synonyms":"industrious","antonyms":"lazy","verbForm":"—","nounForm":"diligence","japanese":""},{"word":"disconcerting","example":"And this was really disconcerting to me","meaning":"causing discomfort","synonyms":"unsettling","antonyms":"comforting","verbForm":"—","nounForm":"—","japanese":"不安を感じさせる"},{"word":"distinguish","example":"It's hard to distinguish between real and fake news nowadays","meaning":"to recognize differences","synonyms":"differentiate","antonyms":"confuse","verbForm":"distinguish","nounForm":"distinction","japanese":"区別する、見分ける"},{"word":"distract","example":"The notifications really distract me when I'm studying","meaning":"to take attention away","synonyms":"divert","antonyms":"focus","verbForm":"distract","nounForm":"distraction","japanese":"気を散らす"},{"word":"dive in","example":"Getting curious about something and diving in","meaning":"to start quickly","synonyms":"start","antonyms":"hesitate","verbForm":"dive","nounForm":"—","japanese":"深く潜る、夢中になる"},{"word":"dive into","example":"I want to dive into this topic to better understand the underlying issues","meaning":"to deeply engage","synonyms":"immerse","antonyms":"avoid","verbForm":"dive","nounForm":"—","japanese":"深く掘り下げる"},{"word":"divide","example":"Let's divide the tasks among the team","meaning":"to separate","synonyms":"split","antonyms":"combine","verbForm":"divide","nounForm":"division","japanese":"分割（物理的なものを割る）"},{"word":"Don't get me wrong","example":"Don't get me wrong I think it's a good idea but we can improve it","meaning":"to clarify intention","synonyms":"—","antonyms":"—","verbForm":"get","nounForm":"—","japanese":"誤解しないで"},{"word":"drop out","example":"We tried to predict which cadets would stay in military training and which would drop out","meaning":"to quit","synonyms":"leave","antonyms":"continue","verbForm":"drop out","nounForm":"dropout","japanese":"脱落する"},{"word":"due to","example":"The game has been cancelled due to the weather conditions","meaning":"because of","synonyms":"owing to","antonyms":"despite","verbForm":"—","nounForm":"—","japanese":"because of（Verbal）"},{"word":"during","example":"During my elementary school in Hiroshima,","meaning":"in the time of","synonyms":"throughout","antonyms":"—","verbForm":"—","nounForm":"—","japanese":""},{"word":"dynamics","example":"The dynamics between the team members are very positive","meaning":"forces or processes of change","synonyms":"interactions","antonyms":"stability","verbForm":"—","nounForm":"dynamic","japanese":"力関係、人間関係や組織の作用"},{"word":"either way","example":"Either way works — the outcome won't change","meaning":"regardless of choice","synonyms":"anyway","antonyms":"—","verbForm":"—","nounForm":"—","japanese":""},{"word":"embrace","example":"We should embrace the opportunity","meaning":"to accept willingly","synonyms":"accept","antonyms":"reject","verbForm":"embrace","nounForm":"embrace","japanese":"喜んで応じる、受け入れる"},{"word":"enhance","example":"The new update will enhance the user experience","meaning":"to improve","synonyms":"improve","antonyms":"worsen","verbForm":"enhance","nounForm":"enhancement","japanese":"強化する、高める"},{"word":"enormous","example":"He ate an enormous helping of pasta","meaning":"very large","synonyms":"huge","antonyms":"small","verbForm":"—","nounForm":"enormity","japanese":""},{"word":"ensure","example":"We have to pay attention to ensure the quality of service","meaning":"to make certain","synonyms":"guarantee","antonyms":"risk","verbForm":"ensure","nounForm":"assurance","japanese":"確実にする、保証する"},{"word":"entrepreneurs","example":"We're entrepreneurs, we run our own businesses","meaning":"people who start businesses","synonyms":"business founders","antonyms":"employees","verbForm":"—","nounForm":"entrepreneur","japanese":"起業家"},{"word":"evaluate","example":"It's impossible to evaluate these results without knowing more about the research methods","meaning":"to assess","synonyms":"assess","antonyms":"ignore","verbForm":"evaluate","nounForm":"evaluation","japanese":""},{"word":"even if","example":"","meaning":"despite possibility","synonyms":"although","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"例え～だったとしても"},{"word":"ever since","example":"He's been depressed ever since the death of his brother","meaning":"from a time in the past until now","synonyms":"since","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"その後ずっと / それ以来"},{"word":"exaggerate","example":"He tends to exaggerate when he tells stories","meaning":"to overstate","synonyms":"overstate","antonyms":"understate","verbForm":"exaggerate","nounForm":"exaggeration","japanese":"誇張する"},{"word":"explore","example":"The best way to explore the countryside is on foot","meaning":"to investigate","synonyms":"examine","antonyms":"ignore","verbForm":"explore","nounForm":"exploration","japanese":"探検する / 探求する"},{"word":"extent","example":"To what extent can we rely on this data?","meaning":"degree or level","synonyms":"degree","antonyms":"—","verbForm":"extend","nounForm":"extent","japanese":"範囲"},{"word":"face (problem)","example":"Everyday we're facing difficult choices","meaning":"to confront","synonyms":"confront","antonyms":"avoid","verbForm":"face","nounForm":"—","japanese":"直面する / 困難に対処する"},{"word":"false pride","example":"There is a difference between false pride","meaning":"unjustified pride","synonyms":"arrogance","antonyms":"humility","verbForm":"—","nounForm":"pride","japanese":"偽りの誇り"},{"word":"fascinate","example":"Science has always fascinated me","meaning":"to attract strongly","synonyms":"captivate","antonyms":"bore","verbForm":"fascinate","nounForm":"fascination","japanese":""},{"word":"feel connected to","example":"I can feel connected to the world","meaning":"to feel emotionally linked","synonyms":"relate to","antonyms":"disconnect","verbForm":"connect","nounForm":"connection","japanese":"～とつながっていると感じる"},{"word":"field","example":"Are you still in the same field?","meaning":"area of study","synonyms":"domain","antonyms":"—","verbForm":"—","nounForm":"field","japanese":"野原 / 分野・専門領域"},{"word":"filter out","example":"They filter out the sounds of languages that were not familiar","meaning":"to remove unwanted parts","synonyms":"remove","antonyms":"include","verbForm":"filter","nounForm":"filter","japanese":"フィルターで除去する"},{"word":"find common ground","example":"We need to find common ground if we want to work together","meaning":"to reach agreement","synonyms":"agree","antonyms":"disagree","verbForm":"find","nounForm":"ground","japanese":"共通点を見つける"},{"word":"find myself doing","example":"I find myself eating a lot of junk food when I'm stressed out","meaning":"to unexpectedly realize you are doing something","synonyms":"realize","antonyms":"—","verbForm":"find","nounForm":"—","japanese":"気づいたら～している"},{"word":"firmly convinced","example":"I was firmly convinced that every one of my students could learn the material","meaning":"strongly believing something","synonyms":"certain","antonyms":"doubtful","verbForm":"convince","nounForm":"conviction","japanese":"強く確信している"},{"word":"first and foremost","example":"First and foremost, I'd like to thank all of you for being here today","meaning":"most importantly","synonyms":"primarily","antonyms":"secondarily","verbForm":"—","nounForm":"—","japanese":""},{"word":"fit in","example":"","meaning":"to belong or be accepted","synonyms":"belong","antonyms":"stand out","verbForm":"fit","nounForm":"—","japanese":"環境になじむ / 溶け込む"},{"word":"fit the mold","example":"Sometimes, society tells us we don't fit the mold","meaning":"to match expectations or norms","synonyms":"conform","antonyms":"differ","verbForm":"fit","nounForm":"—","japanese":"型にはまる"},{"word":"flaw","example":"minor flaw / fatal flaw","meaning":"a weakness or defect","synonyms":"defect","antonyms":"strength","verbForm":"—","nounForm":"flaw","japanese":""},{"word":"focus on","example":"Focus on language content that is relevant to you","meaning":"to concentrate on","synonyms":"concentrate","antonyms":"ignore","verbForm":"focus","nounForm":"focus","japanese":"～に焦点を当てる"},{"word":"follow the same path","example":"I didn't want to follow the same path as my older brother","meaning":"to do the same as others","synonyms":"imitate","antonyms":"diverge","verbForm":"follow","nounForm":"path","japanese":"同じ道を辿る"},{"word":"for good","example":"I came to the United States, and now for good","meaning":"permanently","synonyms":"forever","antonyms":"temporarily","verbForm":"—","nounForm":"—","japanese":"永久に、永遠に"},{"word":"for some reason","example":"I'm not hungry for some reason","meaning":"without a clear reason","synonyms":"somehow","antonyms":"clearly","verbForm":"—","nounForm":"—","japanese":"何かしらの理由で / 何故か分からないけど"},{"word":"for the sake of","example":"For the sake of clarity, let me explain this again","meaning":"for the purpose of","synonyms":"for","antonyms":"against","verbForm":"—","nounForm":"sake","japanese":"～のために（目的や理由を強調）"},{"word":"force A to B","example":"America intended to force Japan to surrender","meaning":"to make someone do something","synonyms":"compel","antonyms":"allow","verbForm":"force","nounForm":"force","japanese":"強制的に～させる"},{"word":"from all walks of life","example":"I have traveled the world, and talked to people from all walks of life","meaning":"from all backgrounds","synonyms":"diverse","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"あらゆる職業や生活環境の人々"},{"word":"gain","example":"I'm not entirely sure if I'm gaining the skills that are truly in demand","meaning":"to obtain or increase","synonyms":"acquire","antonyms":"lose","verbForm":"gain","nounForm":"gain","japanese":"手に入れる / 身につける"},{"word":"generalization","example":"It's a generalization to assume all vegetarians are health conscious","meaning":"a broad statement","synonyms":"simplification","antonyms":"specification","verbForm":"generalize","nounForm":"generalization","japanese":"一般化"},{"word":"genuine","example":"He gave me a genuine smile","meaning":"real and sincere","synonyms":"authentic","antonyms":"fake","verbForm":"—","nounForm":"genuineness","japanese":"本物の、誠実な、心からの"},{"word":"get back to","example":"I'll get back to you as soon as I finish the meeting","meaning":"to return or reply","synonyms":"return","antonyms":"leave","verbForm":"get","nounForm":"return","japanese":"（後で）折り返す、連絡する、戻る"},{"word":"get in the way","example":"I found quite often that school got in the way of learning","meaning":"to obstruct","synonyms":"block","antonyms":"assist","verbForm":"get","nounForm":"—","japanese":"妨げになる"},{"word":"get involved","example":"I want to get involved in community service to help those in need","meaning":"to participate","synonyms":"engage","antonyms":"avoid","verbForm":"get","nounForm":"involvement","japanese":"関与する、参加する"},{"word":"get out of it","example":"The only way to get out of it is to realize that being different also means thinking differently","meaning":"to avoid responsibility","synonyms":"escape","antonyms":"face","verbForm":"get","nounForm":"—","japanese":"それから抜け出す"},{"word":"get rid of stress","example":"I get rid of stress by boxing","meaning":"to remove stress","synonyms":"relieve","antonyms":"increase","verbForm":"get rid of","nounForm":"stress","japanese":"ストレスを解消する"},{"word":"get straight to the point","example":"Let me get straight to the point, this is worthless","meaning":"to be direct","synonyms":"be direct","antonyms":"be vague","verbForm":"get","nounForm":"point","japanese":"結論から言いますと"},{"word":"get used to doing","example":"I am slowly getting used to waking up early","meaning":"to become accustomed","synonyms":"adapt","antonyms":"resist","verbForm":"get used","nounForm":"habit","japanese":"～することに慣れる"},{"word":"give up hope","example":"I'll give up hope","meaning":"to stop believing","synonyms":"despair","antonyms":"hope","verbForm":"give up","nounForm":"hope","japanese":"希望を捨てる"},{"word":"go the extra mile","example":"She's always willing to go the extra mile for her team","meaning":"to do more than expected","synonyms":"exceed","antonyms":"do minimum","verbForm":"go","nounForm":"—","japanese":"さらに努力する"},{"word":"going back to","example":"Going back to your questions, my answer is No","meaning":"returning to a topic","synonyms":"returning","antonyms":"leaving","verbForm":"go","nounForm":"—","japanese":"～に話を戻すと"},{"word":"got me thinking","example":"And that got me thinking","meaning":"caused me to think","synonyms":"inspired","antonyms":"ignore","verbForm":"get","nounForm":"—","japanese":"考えさせられた"},{"word":"gradually","example":"I'm gradually getting better at speaking English","meaning":"slowly over time","synonyms":"slowly","antonyms":"suddenly","verbForm":"—","nounForm":"gradualness","japanese":"次第に"},{"word":"growth mindset","example":"The best idea I've heard about building grit in kids is something called growth mindset","meaning":"belief that abilities can improve","synonyms":"learning mindset","antonyms":"fixed mindset","verbForm":"—","nounForm":"mindset","japanese":"成長マインドセット"},{"word":"have a hard time","example":"I'm having a hard time paying off my tuition","meaning":"to struggle","synonyms":"struggle","antonyms":"succeed","verbForm":"have","nounForm":"difficulty","japanese":"苦労する / ーするのが大変"},{"word":"highlight","example":"The report highlights the importance of early detection","meaning":"to emphasize","synonyms":"emphasize","antonyms":"ignore","verbForm":"highlight","nounForm":"highlight","japanese":"強調する、目立たせる"},{"word":"hook the listener","example":"When we give a presentation, we always struggle to hook the audience","meaning":"to grab attention","synonyms":"engage","antonyms":"bore","verbForm":"hook","nounForm":"—","japanese":""},{"word":"hypocritical","example":"It's hypocritical to criticize others for lying when you do the same","meaning":"acting against one's stated beliefs","synonyms":"insincere","antonyms":"sincere","verbForm":"—","nounForm":"hypocrisy","japanese":"偽善的な"},{"word":"I can't help but feel","example":"I can't help but feel as if God doesn't exist","meaning":"unable to stop feeling","synonyms":"inevitably feel","antonyms":"control feeling","verbForm":"help","nounForm":"feeling","japanese":""},{"word":"I decided to","example":"I decided to become a person who can always put themselves in others' shoes","meaning":"made a decision","synonyms":"chose","antonyms":"hesitated","verbForm":"decide","nounForm":"decision","japanese":""},{"word":"I don't doubt for a second","example":"I don't doubt for a second that the service is going to be closed","meaning":"complete certainty","synonyms":"certain","antonyms":"unsure","verbForm":"doubt","nounForm":"doubt","japanese":"100% certain of that"},{"word":"I feel a bit uncertain about","example":"I felt a bit uncertain about speaking English in front of them","meaning":"slight doubt","synonyms":"unsure","antonyms":"confident","verbForm":"feel","nounForm":"uncertainty","japanese":""},{"word":"I feel drained","example":"I feel drained when I spend time in noisy places","meaning":"feeling exhausted","synonyms":"exhausted","antonyms":"energized","verbForm":"feel","nounForm":"fatigue","japanese":""},{"word":"I have a feeling","example":"I have a feeling that it's going to be a great event","meaning":"intuition about something","synonyms":"sense","antonyms":"certainty","verbForm":"have","nounForm":"feeling","japanese":"そんな気がする / 直感や予感"},{"word":"I know, right?","example":"He did a great job! I know, right?","meaning":"agreement expression","synonyms":"exactly","antonyms":"disagree","verbForm":"know","nounForm":"—","japanese":"それな"},{"word":"I'm on board","example":"It's a great idea, I'm on board","meaning":"agreeing or supporting","synonyms":"agree","antonyms":"oppose","verbForm":"—","nounForm":"—","japanese":""},{"word":"I'm open to","example":"I'm open to hearing perspectives questioning my current thinking","meaning":"willing to consider","synonyms":"receptive","antonyms":"closed","verbForm":"open","nounForm":"openness","japanese":""},{"word":"I'm overwhelmed","example":"I feel a bit overwhelmed","meaning":"emotionally overloaded","synonyms":"overloaded","antonyms":"calm","verbForm":"overwhelm","nounForm":"overwhelm","japanese":""},{"word":"I'm still figuring out","example":"I'm still figuring out my purpose in life","meaning":"still trying to understand","synonyms":"exploring","antonyms":"knowing","verbForm":"figure out","nounForm":"—","japanese":""},{"word":"I've come to realize that","example":"I've come to realize that people don't change easily","meaning":"gradual understanding","synonyms":"realize","antonyms":"ignore","verbForm":"realize","nounForm":"realization","japanese":"一般論であれば現在形を使う"},{"word":"if that's the case","example":"Did he prepare all the slides? If that's the case, you don't have to do anything","meaning":"under that condition","synonyms":"if so","antonyms":"otherwise","verbForm":"be","nounForm":"case","japanese":"もしそうなら"},{"word":"if you think about it","example":"It's amazing that we can communicate like this if you think about it","meaning":"inviting reflection","synonyms":"consider","antonyms":"ignore","verbForm":"think","nounForm":"thought","japanese":"考え方によれば / よく考えてみると"},{"word":"immersion","example":"People also think that immersion in a new country is the way to learn a language","meaning":"deep involvement","synonyms":"involvement","antonyms":"detachment","verbForm":"immerse","nounForm":"immersion","japanese":"没入"},{"word":"in a split second","example":"They say your life can change in a split second","meaning":"very quickly","synonyms":"instantly","antonyms":"slowly","verbForm":"—","nounForm":"—","japanese":"一瞬で"},{"word":"in demand","example":"I'm not entirely sure if I'm gaining the skills that are truly in demand","meaning":"highly wanted","synonyms":"popular","antonyms":"unwanted","verbForm":"demand","nounForm":"demand","japanese":"需要のある"},{"word":"in general","example":"What did you think about this in general?","meaning":"broadly speaking","synonyms":"generally","antonyms":"specifically","verbForm":"—","nounForm":"generalization","japanese":"全体的に / 一般的に"},{"word":"in terms of","example":"In terms of money, I was better off in my last job","meaning":"regarding","synonyms":"concerning","antonyms":"—","verbForm":"—","nounForm":"terms","japanese":"～の観点から / ～に関して"},{"word":"in the end","example":"In the end, what really matters in a friendship is trust","meaning":"finally","synonyms":"eventually","antonyms":"initially","verbForm":"—","nounForm":"end","japanese":""},{"word":"in the first place","example":"You could have avoided such a mistake if you had checked carefully in the first place","meaning":"originally or at all","synonyms":"originally","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"そもそも"},{"word":"in the midst of","example":"I was in the midst of a life-changing experience","meaning":"in the middle of","synonyms":"during","antonyms":"outside","verbForm":"—","nounForm":"midst","japanese":"真っ最中で"},{"word":"in this case","example":"In this case, I think we need to take a different approach","meaning":"in this situation","synonyms":"here","antonyms":"otherwise","verbForm":"—","nounForm":"case","japanese":"この場合は"},{"word":"inflict","example":"The suffering inflicted on these children was unimaginable","meaning":"to cause harm","synonyms":"impose","antonyms":"relieve","verbForm":"inflict","nounForm":"infliction","japanese":""},{"word":"insecurity","example":"There is a rising feeling of insecurity about the future","meaning":"lack of confidence","synonyms":"uncertainty","antonyms":"confidence","verbForm":"—","nounForm":"insecurity","japanese":""},{"word":"instead of","example":"We decided to chill out at home instead of going out","meaning":"as an alternative","synonyms":"rather than","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～の代わりに / ～しないで"},{"word":"intentionally","example":"They did it intentionally","meaning":"on purpose","synonyms":"deliberately","antonyms":"accidentally","verbForm":"—","nounForm":"intention","japanese":"わざと、故意に"},{"word":"interfere","example":"Please do not interfere in other people's affairs","meaning":"to interrupt or disturb","synonyms":"interrupt","antonyms":"assist","verbForm":"interfere","nounForm":"interference","japanese":"干渉する"},{"word":"introvert","example":"Introverts would require more deconditioning attention","meaning":"a person who prefers solitude","synonyms":"reserved person","antonyms":"extrovert","verbForm":"—","nounForm":"introversion","japanese":""},{"word":"it goes without saying","example":"It goes without saying that health comes first","meaning":"obviously true","synonyms":"obviously","antonyms":"questionable","verbForm":"—","nounForm":"—","japanese":"言うまでもない"},{"word":"it is what it is","example":"There's nothing we can do, so it is what it is","meaning":"acceptance of reality","synonyms":"accept","antonyms":"resist","verbForm":"be","nounForm":"—","japanese":"仕方がない / そういうものだ"},{"word":"keep -ing","example":"I'll keep studying English","meaning":"to continue doing something","synonyms":"continue","antonyms":"stop","verbForm":"keep","nounForm":"—","japanese":""},{"word":"keep an eye on","example":"Please keep an eye on the progress and report back to me","meaning":"to watch carefully","synonyms":"monitor","antonyms":"ignore","verbForm":"keep","nounForm":"—","japanese":"見守る"},{"word":"keep going","example":"No matter how hard it gets, keep going!","meaning":"to continue","synonyms":"persist","antonyms":"stop","verbForm":"keep","nounForm":"—","japanese":"続ける、頑張り続ける"},{"word":"keep in mind","example":"Please keep in mind that this is just the beginning of our journey","meaning":"to remember","synonyms":"remember","antonyms":"forget","verbForm":"keep","nounForm":"mind","japanese":"心に留めておく"},{"word":"keep in touch","example":"Let's keep in touch after you move to a new city","meaning":"to stay in contact","synonyms":"stay connected","antonyms":"lose contact","verbForm":"keep","nounForm":"touch","japanese":"連絡を保つ"},{"word":"keep it up","example":"You're doing very well everybody, keep it up!","meaning":"to continue doing well","synonyms":"continue","antonyms":"stop","verbForm":"keep","nounForm":"—","japanese":""},{"word":"keep up","example":"Keep up the good work / You walk too fast! I can't keep up with you","meaning":"to maintain pace","synonyms":"maintain","antonyms":"fall behind","verbForm":"keep","nounForm":"—","japanese":"持続する / ついていく"},{"word":"keep your word","example":"It's important to keep your word, especially in business","meaning":"to keep a promise","synonyms":"fulfill promise","antonyms":"break promise","verbForm":"keep","nounForm":"word","japanese":"約束を守る"},{"word":"kick in","example":"When the sleep deprivation really kicked in","meaning":"to start working (effect)","synonyms":"activate","antonyms":"stop","verbForm":"kick","nounForm":"—","japanese":"始める"},{"word":"label someone as different","example":"When we label someone as different, it dehumanizes them in a way","meaning":"to categorize unfairly","synonyms":"stereotype","antonyms":"accept","verbForm":"label","nounForm":"label","japanese":"誰かを異質だとラベル付けする"},{"word":"land","example":"He finally landed his dream job","meaning":"to arrive or succeed","synonyms":"arrive","antonyms":"depart","verbForm":"land","nounForm":"landing","japanese":"着陸する / 獲得する"},{"word":"lead","example":"She leads a team of 20 people","meaning":"to guide","synonyms":"guide","antonyms":"follow","verbForm":"lead","nounForm":"leader","japanese":"導く、率いる"},{"word":"learn by","example":"The purple people were people who had learned by grammar and formal study","meaning":"to learn through method","synonyms":"learn through","antonyms":"—","verbForm":"learn","nounForm":"learning","japanese":"～によって学ぶ"},{"word":"liberate","example":"The movement aimed to liberate people from oppression","meaning":"to set free","synonyms":"free","antonyms":"restrict","verbForm":"liberate","nounForm":"liberation","japanese":"解放する"},{"word":"like you said","example":"Like you said, this is one of the biggest problems","meaning":"referring to prior statement","synonyms":"as you mentioned","antonyms":"—","verbForm":"say","nounForm":"—","japanese":"あなたが言ったように"},{"word":"look (something) up","example":"I'm going to look up how we can get there","meaning":"to search information","synonyms":"search","antonyms":"ignore","verbForm":"look up","nounForm":"lookup","japanese":""},{"word":"look around","example":"I looked around and I saw all of these people from different countries","meaning":"to explore","synonyms":"explore","antonyms":"ignore","verbForm":"look","nounForm":"—","japanese":"見渡す、周囲を見回す"},{"word":"lost in translation","example":"Some of the nuances of what I wanted to convey were lost in translation","meaning":"meaning not conveyed","synonyms":"misunderstood","antonyms":"clear","verbForm":"lose","nounForm":"loss","japanese":"翻訳で失われる"},{"word":"made a difference","example":"What makes me different is what has made me stand out and be successful","meaning":"had an impact","synonyms":"mattered","antonyms":"irrelevant","verbForm":"make","nounForm":"difference","japanese":"影響を与えた"},{"word":"make a difference","example":"I don't think either way makes a difference","meaning":"to have impact","synonyms":"matter","antonyms":"be irrelevant","verbForm":"make","nounForm":"difference","japanese":""},{"word":"make a mistake","example":"Nothing and nobody is perfect, and if you make a mistake, there's no turning back","meaning":"to do something wrong","synonyms":"err","antonyms":"succeed","verbForm":"make","nounForm":"mistake","japanese":"間違えて～する"},{"word":"make the most of","example":"","meaning":"to use fully","synonyms":"maximize","antonyms":"waste","verbForm":"make","nounForm":"—","japanese":""},{"word":"make up for","example":"","meaning":"to compensate","synonyms":"compensate","antonyms":"worsen","verbForm":"make up","nounForm":"—","japanese":"補う / 埋め合わせる"},{"word":"manipulate","example":"He knows how to manipulate people to get what he wants","meaning":"to control unfairly","synonyms":"control","antonyms":"free","verbForm":"manipulate","nounForm":"manipulation","japanese":"操作する、操る"},{"word":"master","example":"One of the major hurdles for learners is mastering its pronunciation","meaning":"to become very skilled","synonyms":"excel","antonyms":"fail","verbForm":"master","nounForm":"mastery","japanese":""},{"word":"measure","example":"We need to measure whether we've been successful","meaning":"to assess","synonyms":"evaluate","antonyms":"ignore","verbForm":"measure","nounForm":"measurement","japanese":"測定する"},{"word":"misconception","example":"There's a common misconception that drinking coffee stunts your growth","meaning":"wrong belief","synonyms":"misunderstanding","antonyms":"truth","verbForm":"—","nounForm":"misconception","japanese":"誤解、誤った考え"},{"word":"misunderstand","example":"I misunderstood her character","meaning":"to not understand correctly","synonyms":"misinterpret","antonyms":"understand","verbForm":"misunderstand","nounForm":"misunderstanding","japanese":""},{"word":"motivate","example":"What motivated me to go to Vietnam was a genuine interest in experiencing life abroad","meaning":"to inspire action","synonyms":"inspire","antonyms":"discourage","verbForm":"motivate","nounForm":"motivation","japanese":""},{"word":"motor skill","example":"Whether they're studying a motor skill","meaning":"physical skill","synonyms":"physical ability","antonyms":"—","verbForm":"—","nounForm":"skill","japanese":"運動技能"},{"word":"much more than","example":"What if doing well in school depends on much more than your ability to learn quickly?","meaning":"far greater than","synonyms":"significantly more","antonyms":"less","verbForm":"—","nounForm":"—","japanese":"～以上のもの"},{"word":"my goal is to","example":"My goal is to contribute to world peace","meaning":"expressing aim","synonyms":"aim to","antonyms":"—","verbForm":"goal","nounForm":"goal","japanese":""},{"word":"no matter which","example":"No matter which way I choose, it doesn't matter","meaning":"regardless of choice","synonyms":"whichever","antonyms":"—","verbForm":"—","nounForm":"—","japanese":""},{"word":"nominal","example":"My title is just nominal — in reality, I just support the doctors behind the scenes","meaning":"in name only","synonyms":"minimal","antonyms":"substantial","verbForm":"—","nounForm":"—","japanese":""},{"word":"norm","example":"We have to accept norms if you live there","meaning":"standard","synonyms":"standard","antonyms":"anomaly","verbForm":"—","nounForm":"norm","japanese":"規範、一般水準"},{"word":"observe","example":"We've now observed the same tendency in 45 patients","meaning":"to watch carefully","synonyms":"monitor","antonyms":"ignore","verbForm":"observe","nounForm":"observation","japanese":""},{"word":"on the other hand","example":"In Japan, a glass of water is always served free of charge on the other hand","meaning":"contrast","synonyms":"however","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"一方で"},{"word":"once and for all","example":"I wanted to resolve the issue once and for all","meaning":"finally","synonyms":"definitively","antonyms":"repeatedly","verbForm":"—","nounForm":"—","japanese":"これで終わりにするために"},{"word":"open the doors","example":"Hypnopaedia did open the doors to research in other areas","meaning":"to create opportunity","synonyms":"enable","antonyms":"block","verbForm":"open","nounForm":"opening","japanese":"門戸を開く"},{"word":"or so","example":"I think it's going to start in 10 minutes or so","meaning":"approximately","synonyms":"about","antonyms":"exactly","verbForm":"—","nounForm":"—","japanese":"～くらい"},{"word":"ordeal","example":"As I got through that ordeal","meaning":"difficult experience","synonyms":"hardship","antonyms":"ease","verbForm":"—","nounForm":"ordeal","japanese":"苦難"},{"word":"out of nowhere","example":"He appeared out of nowhere and surprised everyone","meaning":"suddenly","synonyms":"suddenly","antonyms":"gradually","verbForm":"—","nounForm":"—","japanese":"突然"},{"word":"overall","example":"The overall situation is good, despite a few minor problems","meaning":"generally","synonyms":"generally","antonyms":"specifically","verbForm":"—","nounForm":"—","japanese":""},{"word":"participate","example":"She never participates in any of our discussions, does she?","meaning":"to take part","synonyms":"join","antonyms":"avoid","verbForm":"participate","nounForm":"participation","japanese":""},{"word":"pass on","example":"I think I'll pass on the party tonight","meaning":"to give or decline","synonyms":"transfer","antonyms":"keep","verbForm":"pass","nounForm":"—","japanese":"気軽な断り方・やわらかい"},{"word":"passion and perseverance","example":"Grit is passion and perseverance for very long-term goals","meaning":"strong drive and persistence","synonyms":"grit","antonyms":"apathy","verbForm":"persevere","nounForm":"perseverance","japanese":"情熱と忍耐"},{"word":"pay off","example":"All her hard work finally paid off","meaning":"to bring result","synonyms":"succeed","antonyms":"fail","verbForm":"pay off","nounForm":"payoff","japanese":"報われる、成果が出る"},{"word":"perceive","example":"I perceived something moving in the shadows","meaning":"to interpret","synonyms":"interpret","antonyms":"ignore","verbForm":"perceive","nounForm":"perception","japanese":""},{"word":"persevere","example":"Very few persevere","meaning":"to continue despite difficulty","synonyms":"persist","antonyms":"quit","verbForm":"persevere","nounForm":"perseverance","japanese":"粘り強く続ける"},{"word":"persist","example":"If the pain persists, please consult a doctor","meaning":"to continue firmly","synonyms":"continue","antonyms":"stop","verbForm":"persist","nounForm":"persistence","japanese":"固執する / やり通す"},{"word":"perspective","example":"Her attitude leads a fresh perspective to the subject","meaning":"viewpoint","synonyms":"viewpoint","antonyms":"—","verbForm":"—","nounForm":"perspective","japanese":""},{"word":"play a role","example":"Agriculture plays a great role in the country's economic development","meaning":"to have a function","synonyms":"contribute","antonyms":"—","verbForm":"play","nounForm":"role","japanese":"役割を果たす"},{"word":"point out","example":"I would like to point out the importance of teamwork","meaning":"to indicate","synonyms":"highlight","antonyms":"ignore","verbForm":"point","nounForm":"point","japanese":"指摘する"},{"word":"practical","example":"We need to find a practical solution to this problem","meaning":"useful","synonyms":"useful","antonyms":"impractical","verbForm":"—","nounForm":"practicality","japanese":"実用的な"},{"word":"prefer","example":"I prefer tea to coffee","meaning":"to like more","synonyms":"favor","antonyms":"dislike","verbForm":"prefer","nounForm":"preference","japanese":"より好む / 比較のニュアンスが強い"},{"word":"pretty much","example":"This is pretty much done","meaning":"almost","synonyms":"nearly","antonyms":"exactly","verbForm":"—","nounForm":"—","japanese":"ほぼ"},{"word":"principle","example":"There are five principles and seven actions","meaning":"basic rule","synonyms":"rule","antonyms":"exception","verbForm":"—","nounForm":"principle","japanese":"原則"},{"word":"procrastination","example":"No, that's procrastination","meaning":"delaying action","synonyms":"delay","antonyms":"act","verbForm":"procrastinate","nounForm":"procrastination","japanese":"先延ばし、怠慢"},{"word":"prolong","example":"New inventions in the medical field can sometimes prolong our lives","meaning":"to extend","synonyms":"extend","antonyms":"shorten","verbForm":"prolong","nounForm":"prolongation","japanese":""},{"word":"prompt","example":"This incident prompted me to evaluate our recruiting process","meaning":"to cause or immediate","synonyms":"trigger","antonyms":"delay","verbForm":"prompt","nounForm":"prompt","japanese":""},{"word":"push myself too hard","example":"","meaning":"to overwork","synonyms":"overwork","antonyms":"relax","verbForm":"push","nounForm":"pressure","japanese":"無理をする / 過度に追い込む"},{"word":"put into words","example":"It's hard to put into words, even now","meaning":"to express","synonyms":"express","antonyms":"suppress","verbForm":"put","nounForm":"words","japanese":"言葉にする"},{"word":"put on a brave face","example":"I decided to put on a brave face, and embrace everything I could about the American way of life","meaning":"to hide fear","synonyms":"pretend brave","antonyms":"show fear","verbForm":"put","nounForm":"—","japanese":"強がってみせる"},{"word":"put up with","example":"I can't put up with this humid weather","meaning":"to tolerate","synonyms":"tolerate","antonyms":"reject","verbForm":"put up","nounForm":"—","japanese":"我慢する"},{"word":"quite a bit","example":"My grandma has quite a bit of experience when it comes to gardening","meaning":"a lot","synonyms":"a lot","antonyms":"little","verbForm":"—","nounForm":"—","japanese":"かなりの量"},{"word":"raise questions","example":"It raises questions about the true motivations behind America's use of the atomic bomb","meaning":"to cause doubt","synonyms":"question","antonyms":"answer","verbForm":"raise","nounForm":"question","japanese":"疑問を持たせる / 問題を提起する"},{"word":"rather than","example":"I think you should study pronunciation first rather than spending too much time on vocabulary","meaning":"instead of","synonyms":"instead of","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～ではなく / ～より"},{"word":"recommend (that)","example":"The doctor recommended that I get more exercise","meaning":"to suggest","synonyms":"suggest","antonyms":"oppose","verbForm":"recommend","nounForm":"recommendation","japanese":""},{"word":"regardless of the odds","example":"To accomplish any task, regardless of the odds","meaning":"despite difficulty","synonyms":"despite","antonyms":"because of","verbForm":"—","nounForm":"odds","japanese":"確率に関係なく"},{"word":"regret -ing","example":"I really regret not taking the chance to study abroad when I was younger","meaning":"to feel sorry for","synonyms":"regret","antonyms":"be glad","verbForm":"regret","nounForm":"regret","japanese":""},{"word":"reimagine yourself","example":"Being able to reimagine yourself beyond what other people see — that is the toughest task of all","meaning":"to rethink identity","synonyms":"redefine","antonyms":"accept","verbForm":"reimagine","nounForm":"imagination","japanese":"自分を再創造する"},{"word":"reject","example":"My idea was completely rejected","meaning":"to refuse","synonyms":"refuse","antonyms":"accept","verbForm":"reject","nounForm":"rejection","japanese":""},{"word":"relevant","example":"Education should be relevant to the child's needs","meaning":"related","synonyms":"related","antonyms":"irrelevant","verbForm":"—","nounForm":"relevance","japanese":""},{"word":"remain","example":"The doctor ordered him to remain in bed for a few days","meaning":"to stay","synonyms":"stay","antonyms":"leave","verbForm":"remain","nounForm":"remainder","japanese":""},{"word":"remind","example":"This song reminds me of my childhood","meaning":"to help remember","synonyms":"prompt","antonyms":"forget","verbForm":"remind","nounForm":"reminder","japanese":"思い出す / 思い出させる"},{"word":"remove barriers","example":"Remove barriers to practice","meaning":"to eliminate obstacles","synonyms":"eliminate","antonyms":"create","verbForm":"remove","nounForm":"removal","japanese":"障害を取り除く"},{"word":"resonate with","example":"I always try to choose words that are familiar to them, so they can resonate with my story","meaning":"to connect emotionally","synonyms":"connect","antonyms":"disconnect","verbForm":"resonate","nounForm":"resonance","japanese":""},{"word":"rose-colored glasses","example":"She tends to see the world through rose-colored glasses","meaning":"overly optimistic view","synonyms":"idealistic","antonyms":"realistic","verbForm":"—","nounForm":"—","japanese":"楽観的な考え方"},{"word":"say no","example":"I wanted to say no, but I couldn't","meaning":"to refuse","synonyms":"refuse","antonyms":"accept","verbForm":"say","nounForm":"—","japanese":"会話的・柔らかくもできる"},{"word":"see eye to eye","example":"It's important that we see eye to eye on this matter","meaning":"to agree","synonyms":"agree","antonyms":"disagree","verbForm":"see","nounForm":"—","japanese":"意見が一致する"},{"word":"see something through","example":"I was determined to see it through, no matter what","meaning":"to finish","synonyms":"complete","antonyms":"quit","verbForm":"see","nounForm":"—","japanese":"最後までやり遂げる"},{"word":"self-confidence","example":"The most important thing? Self-confidence","meaning":"belief in oneself","synonyms":"confidence","antonyms":"insecurity","verbForm":"—","nounForm":"confidence","japanese":"自信"},{"word":"self-correct","example":"Learn just enough that you can actually practice and self-correct as you practice","meaning":"to fix own errors","synonyms":"correct","antonyms":"ignore","verbForm":"correct","nounForm":"correction","japanese":"自己修正する"},{"word":"separate","example":"We need to separate work and personal life","meaning":"to divide","synonyms":"divide","antonyms":"combine","verbForm":"separate","nounForm":"separation","japanese":"分離 / 分ける、区別する"},{"word":"setting","example":"I started studying kids and adults in all kinds of super challenging settings","meaning":"environment","synonyms":"context","antonyms":"—","verbForm":"set","nounForm":"setting","japanese":"環境"},{"word":"show respect","example":"It takes courage to show respect","meaning":"to act respectfully","synonyms":"respect","antonyms":"disrespect","verbForm":"show","nounForm":"respect","japanese":"敬意を示す"},{"word":"sibling","example":"I have two siblings—an older sister and a younger brother","meaning":"brother or sister","synonyms":"—","antonyms":"—","verbForm":"—","nounForm":"sibling","japanese":"兄弟姉妹"},{"word":"simply put","example":"Simply put, I'm not interested","meaning":"in simple terms","synonyms":"simply","antonyms":"complexly","verbForm":"—","nounForm":"—","japanese":"簡単に言えば"},{"word":"skill acquisition","example":"When you actually look at the studies of skill acquisition","meaning":"learning skills","synonyms":"learning","antonyms":"—","verbForm":"acquire","nounForm":"acquisition","japanese":"スキル習得"},{"word":"sleep deprivation","example":"When the sleep deprivation really kicked in","meaning":"lack of sleep","synonyms":"insomnia","antonyms":"rest","verbForm":"deprive","nounForm":"deprivation","japanese":"睡眠不足"},{"word":"somehow","example":"I don't know how, but somehow I will ask her out","meaning":"in some way","synonyms":"somehow","antonyms":"clearly","verbForm":"—","nounForm":"—","japanese":"何となく"},{"word":"somewhat","example":"I would say that her English skills have improved somewhat since we last met","meaning":"to some degree","synonyms":"slightly","antonyms":"completely","verbForm":"—","nounForm":"—","japanese":"いくらか / やや / 多少"},{"word":"spark","example":"It's hard to spark Japanese interest in anything religious","meaning":"to trigger","synonyms":"trigger","antonyms":"stop","verbForm":"spark","nounForm":"spark","japanese":""},{"word":"speak out","example":"If you disagree with something, speak out!","meaning":"to express openly","synonyms":"speak up","antonyms":"stay silent","verbForm":"speak","nounForm":"speech","japanese":"はっきり意見を述べる"},{"word":"spend time on something","example":"I don't want to spend too much time on shopping","meaning":"to use time","synonyms":"invest time","antonyms":"waste time","verbForm":"spend","nounForm":"time","japanese":"時間をかける"},{"word":"spontaneously","example":"I've never been the kind of person who can speak spontaneously","meaning":"without planning","synonyms":"naturally","antonyms":"deliberately","verbForm":"—","nounForm":"spontaneity","japanese":""},{"word":"stand out","example":"What makes me different is what has made me stand out and be successful","meaning":"to be noticeable","synonyms":"be distinct","antonyms":"blend in","verbForm":"stand","nounForm":"—","japanese":"目立つ"},{"word":"stand tall","example":"Even in difficult times, she stood tall and faced her challenges","meaning":"to be confident","synonyms":"be confident","antonyms":"shrink","verbForm":"stand","nounForm":"—","japanese":"胸を張って立つ"},{"word":"start off","example":"It's going to start off fair in Los Angeles","meaning":"to begin","synonyms":"begin","antonyms":"end","verbForm":"start","nounForm":"start","japanese":"始める（着手する）"},{"word":"state","example":"He clearly stated his opinion during the meeting","meaning":"to express","synonyms":"express","antonyms":"hide","verbForm":"state","nounForm":"statement","japanese":"述べる、状態、州"},{"word":"step away from","example":"I need to step away from working, and enjoy nature","meaning":"to distance oneself","synonyms":"withdraw","antonyms":"approach","verbForm":"step","nounForm":"—","japanese":""},{"word":"stick to","example":"I want to stick to my weekday sleep routine","meaning":"to continue firmly","synonyms":"adhere","antonyms":"abandon","verbForm":"stick","nounForm":"—","japanese":"ルールや習慣に従う / こだわる"},{"word":"stick with","example":"Grit is sticking with your future, day in, day out","meaning":"to continue or stay","synonyms":"persist","antonyms":"quit","verbForm":"stick","nounForm":"—","japanese":"続ける"},{"word":"struggle to do","example":"I'm struggling hard to pay for school","meaning":"to find difficult","synonyms":"struggle","antonyms":"succeed","verbForm":"struggle","nounForm":"struggle","japanese":"～するのに苦労する"},{"word":"suggest","example":"I suggest we take a break","meaning":"to propose","synonyms":"propose","antonyms":"oppose","verbForm":"suggest","nounForm":"suggestion","japanese":"提案する、示唆する"},{"word":"sustain","example":"I couldn't sustain my progress","meaning":"to maintain","synonyms":"maintain","antonyms":"stop","verbForm":"sustain","nounForm":"sustainability","japanese":"持続させる / 維持する"},{"word":"take a break","example":"Let's take a break and continue later","meaning":"to rest","synonyms":"rest","antonyms":"work","verbForm":"take","nounForm":"break","japanese":"休憩を取る"},{"word":"take a stand","example":"So take a stand to defend your race, the human race","meaning":"to express opinion firmly","synonyms":"defend","antonyms":"remain neutral","verbForm":"take","nounForm":"stand","japanese":"立場を取る"},{"word":"take a step back","example":"Sometimes you need to take a step back to see the bigger picture","meaning":"to reconsider","synonyms":"reconsider","antonyms":"rush","verbForm":"take","nounForm":"step","japanese":"一歩引いて考える"},{"word":"take action","example":"The final action you need to take is something that I call direct connect","meaning":"to act","synonyms":"act","antonyms":"delay","verbForm":"take","nounForm":"action","japanese":"行動を起こす"},{"word":"take into consideration","example":"Please take into consideration all the factors before making a decision","meaning":"to consider","synonyms":"consider","antonyms":"ignore","verbForm":"take","nounForm":"consideration","japanese":"考慮する"},{"word":"take it easy","example":"Take it easy and don't stress too much","meaning":"to relax","synonyms":"relax","antonyms":"stress","verbForm":"take","nounForm":"—","japanese":"気楽にやる"},{"word":"take it for granted","example":"Never take your health for granted","meaning":"to assume","synonyms":"assume","antonyms":"appreciate","verbForm":"take","nounForm":"—","japanese":"当たり前に思う"},{"word":"take it in stride","example":"She took it in stride when she was moved to live with a counselor","meaning":"to handle calmly","synonyms":"handle calmly","antonyms":"panic","verbForm":"take","nounForm":"stride","japanese":"冷静に受け止める"},{"word":"take it one step at a time","example":"Let's take it one step at a time","meaning":"to proceed gradually","synonyms":"proceed slowly","antonyms":"rush","verbForm":"take","nounForm":"step","japanese":"一歩ずつ進める"},{"word":"take it to the next level","example":"It's time to take our efforts to the next level","meaning":"to improve further","synonyms":"improve","antonyms":"stagnate","verbForm":"take","nounForm":"level","japanese":"次のレベルに引き上げる"},{"word":"take muscle","example":"Speaking takes muscle","meaning":"to require strength/effort","synonyms":"require effort","antonyms":"be easy","verbForm":"take","nounForm":"—","japanese":"筋力を要する"},{"word":"take off","example":"Her flight takes off in ten minutes","meaning":"to remove or become successful quickly","synonyms":"remove / succeed","antonyms":"put on / fail","verbForm":"take off","nounForm":"—","japanese":"出発する / 離陸する"},{"word":"take the world by storm","example":"The young singer's debut album took the world by storm","meaning":"to become very successful quickly","synonyms":"dominate","antonyms":"fail","verbForm":"take","nounForm":"—","japanese":"世界を席巻する"},{"word":"take your time","example":"Take your time, there's no rush","meaning":"to not rush","synonyms":"relax","antonyms":"hurry","verbForm":"take","nounForm":"time","japanese":"ゆっくりやる"},{"word":"tear you apart","example":"Stay away from those who will tear you apart","meaning":"to criticize harshly","synonyms":"criticize","antonyms":"praise","verbForm":"tear","nounForm":"—","japanese":"あなたを引き裂く"},{"word":"tell the difference","example":"Can you tell the difference between the original and the copy?","meaning":"to distinguish","synonyms":"differentiate","antonyms":"confuse","verbForm":"tell","nounForm":"difference","japanese":"違いが分かる"},{"word":"tend to do","example":"I had heard that Vietnamese people tend to change jobs frequently","meaning":"to usually do","synonyms":"usually","antonyms":"rarely","verbForm":"tend","nounForm":"tendency","japanese":"～しがちである"},{"word":"thanks for having me","example":"It's a pleasure to be here, thank you for having me","meaning":"expression of gratitude","synonyms":"thank you","antonyms":"—","verbForm":"have","nounForm":"—","japanese":""},{"word":"that's a fair point","example":"I think that's a fair point","meaning":"valid opinion","synonyms":"valid","antonyms":"invalid","verbForm":"—","nounForm":"point","japanese":"確かにそうだね"},{"word":"the path to personal growth","example":"I've already told you how my path to personal growth started","meaning":"way to self-improvement","synonyms":"development path","antonyms":"stagnation","verbForm":"grow","nounForm":"growth","japanese":"個人的成長への道"},{"word":"this experience inspired me","example":"This experience inspired me to learn English more seriously","meaning":"caused motivation","synonyms":"motivated","antonyms":"discouraged","verbForm":"inspire","nounForm":"inspiration","japanese":""},{"word":"tie together","example":"These are logical transformers that tie bits of a language together","meaning":"to connect ideas","synonyms":"connect","antonyms":"separate","verbForm":"tie","nounForm":"—","japanese":"つなぎ合わせる"},{"word":"to be fair","example":"The restaurant had a few issues with service, but to be fair, the food was exceptional","meaning":"considering all sides","synonyms":"fairly","antonyms":"unfairly","verbForm":"—","nounForm":"fairness","japanese":"（批判をソフトに）、公平"},{"word":"to be honest with you","example":"To be completely honest with you, those are the last things I look for","meaning":"speaking truthfully","synonyms":"honestly","antonyms":"dishonestly","verbForm":"—","nounForm":"honesty","japanese":"正直に言うと"},{"word":"to begin with","example":"To begin with, the project was difficult to realize because of a limited budget","meaning":"at first","synonyms":"initially","antonyms":"finally","verbForm":"begin","nounForm":"beginning","japanese":"まず最初に"},{"word":"to my surprise","example":"To my surprise, the test was much easier than I expected","meaning":"unexpectedly","synonyms":"unexpectedly","antonyms":"expectedly","verbForm":"surprise","nounForm":"surprise","japanese":"驚いたことに"},{"word":"to this day","example":"To this day, I still think about what happened back then","meaning":"until now","synonyms":"still","antonyms":"no longer","verbForm":"—","nounForm":"day","japanese":"今日に至るまで"},{"word":"tragic","example":"We had to learn about the tragic events of 6th August 1945","meaning":"causing great sadness","synonyms":"sad","antonyms":"happy","verbForm":"—","nounForm":"tragedy","japanese":""},{"word":"transparency","example":"The company has improved its transparency by sharing more information with the public","meaning":"openness","synonyms":"openness","antonyms":"secrecy","verbForm":"—","nounForm":"transparency","japanese":"透明性"},{"word":"trial and error","example":"I have done trial and error for hundreds of times","meaning":"learning by trying","synonyms":"experimentation","antonyms":"certainty","verbForm":"—","nounForm":"trial","japanese":""},{"word":"turn down","example":"I was surprised when she turned down my offer","meaning":"to reject or lower","synonyms":"reject","antonyms":"accept","verbForm":"turn","nounForm":"—","japanese":"日常会話で自然"},{"word":"unlike","example":"Unlike the previous time, today I did well on my test","meaning":"different from","synonyms":"different","antonyms":"similar","verbForm":"—","nounForm":"—","japanese":"～とは違って"},{"word":"valuable","example":"","meaning":"worth a lot","synonyms":"valuable","antonyms":"worthless","verbForm":"value","nounForm":"value","japanese":""},{"word":"view","example":"From my point of view, the project is progressing well","meaning":"opinion or sight","synonyms":"opinion","antonyms":"—","verbForm":"view","nounForm":"view","japanese":"見解、視点"},{"word":"walk in someone else's shoes","example":"","meaning":"to empathize","synonyms":"empathize","antonyms":"ignore","verbForm":"walk","nounForm":"—","japanese":""},{"word":"well-being","example":"People doing yoga benefit from an increased feeling of well-being","meaning":"health and happiness","synonyms":"welfare","antonyms":"suffering","verbForm":"—","nounForm":"well-being","japanese":""},{"word":"what if","example":"What if I lose my job? What if I say no?","meaning":"hypothetical thinking","synonyms":"suppose","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"もし～したらどうする？"},{"word":"when it comes to","example":"When it comes to money, I cannot really trust them","meaning":"regarding","synonyms":"about","antonyms":"—","verbForm":"come","nounForm":"—","japanese":"～に関して言えば"},{"word":"whereas","example":"He likes learning from textbooks, whereas I like learning on the job","meaning":"in contrast","synonyms":"while","antonyms":"similar","verbForm":"—","nounForm":"—","japanese":"一方で"},{"word":"whether or not","example":"Whether or not you like it doesn't matter","meaning":"regardless of condition","synonyms":"if","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～であろうとなかろうと"},{"word":"willing to fail","example":"We have to be willing to fail, to be wrong, to start over again with lessons learned","meaning":"ready to risk failure","synonyms":"brave","antonyms":"risk-averse","verbForm":"—","nounForm":"willingness","japanese":"失敗する覚悟がある"},{"word":"without","example":"I can't live without coffee","meaning":"lacking","synonyms":"lacking","antonyms":"with","verbForm":"—","nounForm":"—","japanese":"～なしで"},{"word":"you can just","example":"You can just call me Mike","meaning":"suggestion","synonyms":"simply","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"～するだけでいいよ"},{"word":"you know what I mean?","example":"You know what I mean?","meaning":"checking understanding","synonyms":"understand","antonyms":"confuse","verbForm":"know","nounForm":"—","japanese":"言っていることわかる？"},{"word":"get + 人 + to do","example":"She finally got her kids to go to bed","meaning":"cause someone to act","synonyms":"make","antonyms":"prevent","verbForm":"get","nounForm":"—","japanese":"お願い・説得して～してもらう"},{"word":"make it to","example":"I finally made it to the station on time","meaning":"succeed in reaching","synonyms":"reach","antonyms":"fail","verbForm":"make","nounForm":"—","japanese":"～にたどり着く / ～に間に合う"},{"word":"like I said","example":"Like I said, we should be careful","meaning":"referring back","synonyms":"as said","antonyms":"—","verbForm":"say","nounForm":"—","japanese":"さっき言ったように"},{"word":"contrary to","example":"Contrary to expectations, it didn't rain","meaning":"opposite of","synonyms":"against","antonyms":"in line with","verbForm":"—","nounForm":"—","japanese":"～に反して"},{"word":"that's what matters","example":"It's not perfect, but that's what matters","meaning":"key point","synonyms":"important","antonyms":"trivial","verbForm":"matter","nounForm":"matter","japanese":"それが大事なんだ"},{"word":"aggressor","example":"The aggressor started the fight","meaning":"attacker","synonyms":"attacker","antonyms":"defender","verbForm":"—","nounForm":"aggression","japanese":"侵略者・加害者"},{"word":"victim","example":"The victim reported the crime","meaning":"harmed person","synonyms":"sufferer","antonyms":"attacker","verbForm":"—","nounForm":"victim","japanese":"被害者"},{"word":"casualty","example":"There were many casualties in the accident","meaning":"injured/dead person","synonyms":"victim","antonyms":"—","verbForm":"—","nounForm":"casualty","japanese":"死傷者"},{"word":"that being said","example":"It's expensive. That being said, it's worth it","meaning":"transition phrase","synonyms":"however","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"そうは言っても"},{"word":"for the first time in ~years","example":"I saw snow for the first time in five years","meaning":"first occurrence after gap","synonyms":"first time","antonyms":"repeated","verbForm":"—","nounForm":"time","japanese":"～ぶりに初めて"},{"word":"narrow down","example":"We need to narrow down the options","meaning":"to reduce options","synonyms":"limit","antonyms":"expand","verbForm":"narrow","nounForm":"narrowing","japanese":"絞り込む"},{"word":"go over","example":"Let's go over the report together","meaning":"to review","synonyms":"review","antonyms":"ignore","verbForm":"go","nounForm":"—","japanese":"確認する / 復習する"},{"word":"absolutely","example":"That's absolutely true","meaning":"completely","synonyms":"totally","antonyms":"partially","verbForm":"—","nounForm":"—","japanese":"完全に / まったく（強調）"},{"word":"come up with","example":"She came up with a great idea","meaning":"to create idea","synonyms":"invent","antonyms":"fail","verbForm":"come","nounForm":"—","japanese":"思いつく"},{"word":"heads-up","example":"Thanks for the heads-up about the delay","meaning":"warning","synonyms":"warning","antonyms":"surprise","verbForm":"—","nounForm":"—","japanese":"事前の注意・知らせ"},{"word":"cling to","example":"The child clung to her mother","meaning":"to hold tightly","synonyms":"hold","antonyms":"release","verbForm":"cling","nounForm":"—","japanese":"しがみつく / 固執する"},{"word":"concrete","example":"We need concrete evidence","meaning":"specific","synonyms":"specific","antonyms":"abstract","verbForm":"—","nounForm":"concreteness","japanese":"具体的・明確な"},{"word":"intelligibility","example":"Clear pronunciation improves intelligibility","meaning":"clarity of speech","synonyms":"clarity","antonyms":"confusion","verbForm":"—","nounForm":"intelligibility","japanese":"理解しやすさ"},{"word":"admiration","example":"I have admiration for her courage","meaning":"respect","synonyms":"respect","antonyms":"contempt","verbForm":"admire","nounForm":"admiration","japanese":"強い尊敬・称賛"},{"word":"coherence","example":"The essay lacks coherence","meaning":"logical connection","synonyms":"consistency","antonyms":"inconsistency","verbForm":"cohere","nounForm":"coherence","japanese":"一貫性・つながり"},{"word":"validate","example":"The test validates the theory","meaning":"to confirm","synonyms":"confirm","antonyms":"reject","verbForm":"validate","nounForm":"validation","japanese":"正当性を確認する"},{"word":"optimal","example":"This is the optimal solution","meaning":"best possible","synonyms":"best","antonyms":"worst","verbForm":"—","nounForm":"optimum","japanese":"最適な"},{"word":"vulnerability","example":"The system has vulnerabilities","meaning":"weakness","synonyms":"weakness","antonyms":"strength","verbForm":"—","nounForm":"vulnerability","japanese":"弱点・脆弱性"},{"word":"going in circles","example":"We are going in circles","meaning":"no progress","synonyms":"stagnate","antonyms":"progress","verbForm":"go","nounForm":"—","japanese":"堂々巡りする"},{"word":"intimate","example":"We need to maintain an intimate relationship with our clients","meaning":"close or personal","synonyms":"close","antonyms":"distant","verbForm":"—","nounForm":"intimacy","japanese":"親密な、深い"},{"word":"despise","example":"I despise any form of discrimination in the workplace","meaning":"strongly hate","synonyms":"hate","antonyms":"love","verbForm":"despise","nounForm":"despise","japanese":"軽蔑する、忌み嫌う"},{"word":"flourish","example":"We hope our new branch in Hanoi will flourish","meaning":"to grow well","synonyms":"thrive","antonyms":"decline","verbForm":"flourish","nounForm":"flourishing","japanese":"繁栄する、活躍する"},{"word":"dread","example":"Many staff members dread the complex tax audit","meaning":"to fear","synonyms":"fear","antonyms":"welcome","verbForm":"dread","nounForm":"dread","japanese":"恐れる、ひどく不安に思う"},{"word":"grumble","example":"It is better to address issues before staff start to grumble","meaning":"to complain","synonyms":"complain","antonyms":"praise","verbForm":"grumble","nounForm":"grumble","japanese":"不平を言う"},{"word":"doable","example":"Reducing the lead time to three days is doable","meaning":"possible","synonyms":"feasible","antonyms":"impossible","verbForm":"—","nounForm":"—","japanese":"実行可能な、できる"},{"word":"call off","example":"We had to call off the meeting due to the typhoon","meaning":"to cancel","synonyms":"cancel","antonyms":"continue","verbForm":"call off","nounForm":"—","japanese":"中止する"},{"word":"following","example":"Following the approval from Yama, we will proceed","meaning":"next or after","synonyms":"next","antonyms":"previous","verbForm":"follow","nounForm":"following","japanese":"～を受けて、～に続いて"},{"word":"referral","example":"Could you provide a referral for the person in charge?","meaning":"recommendation","synonyms":"recommendation","antonyms":"—","verbForm":"refer","nounForm":"referral","japanese":"紹介、推薦"},{"word":"ineligible","example":"This expense is ineligible for company reimbursement","meaning":"not qualified","synonyms":"unqualified","antonyms":"eligible","verbForm":"—","nounForm":"eligibility","japanese":"対象外の、資格のない"},{"word":"reimburse","example":"We will reimburse the travel costs as overtime pay","meaning":"to repay","synonyms":"repay","antonyms":"charge","verbForm":"reimburse","nounForm":"reimbursement","japanese":"払い戻す、清算する"},{"word":"subject to","example":"The overtime pay is not subject to PIT","meaning":"depending on","synonyms":"depending","antonyms":"independent","verbForm":"—","nounForm":"—","japanese":"～の対象となる"},{"word":"identify","example":"We need to identify the cause of the staff turnover","meaning":"to recognize","synonyms":"recognize","antonyms":"ignore","verbForm":"identify","nounForm":"identification","japanese":"特定する、見極める"},{"word":"retention","example":"Improving staff retention is a key priority for us","meaning":"keeping","synonyms":"keeping","antonyms":"loss","verbForm":"retain","nounForm":"retention","japanese":"（社員の）定着、保持"},{"word":"alignment","example":"We need better alignment between expectations and reality","meaning":"agreement","synonyms":"agreement","antonyms":"conflict","verbForm":"align","nounForm":"alignment","japanese":"一致、調整"},{"word":"competitive","example":"Our clinic offers competitive pricing in Hanoi","meaning":"relating to competition","synonyms":"rival","antonyms":"cooperative","verbForm":"compete","nounForm":"competition","japanese":"競争力のある"},{"word":"accommodate","example":"Our facility can accommodate large groups for check-ups","meaning":"to provide space or adapt","synonyms":"adapt","antonyms":"refuse","verbForm":"accommodate","nounForm":"accommodation","japanese":"収容する、受け入れる"},{"word":"specifically","example":"Specifically, I am concerned about the new staff members","meaning":"clearly defined","synonyms":"precisely","antonyms":"generally","verbForm":"specify","nounForm":"specification","japanese":"具体的には"},{"word":"consistent","example":"Thank you for your consistent support of our service","meaning":"steady","synonyms":"steady","antonyms":"inconsistent","verbForm":"consist","nounForm":"consistency","japanese":"継続的な、一貫した"},{"word":"maintain","example":"We must maintain high standards of Japanese quality","meaning":"to keep","synonyms":"sustain","antonyms":"lose","verbForm":"maintain","nounForm":"maintenance","japanese":"維持する、管理する"},{"word":"accordingly","example":"Please update the records and process the pay accordingly","meaning":"therefore","synonyms":"therefore","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"それに従って、適切に"},{"word":"quotation","example":"Could you send a formal quotation by tomorrow?","meaning":"price statement","synonyms":"quote","antonyms":"—","verbForm":"quote","nounForm":"quotation","japanese":"見積もり"},{"word":"lead time","example":"What is the expected lead time for the AirFit N20?","meaning":"preparation time","synonyms":"prep time","antonyms":"delay","verbForm":"—","nounForm":"lead time","japanese":"リードタイム（所要期間）"},{"word":"out of stock","example":"Unfortunately, the item is currently out of stock","meaning":"unavailable","synonyms":"unavailable","antonyms":"available","verbForm":"—","nounForm":"stock","japanese":"在庫切れ"},{"word":"invoice","example":"Please issue the e-invoice after the payment is settled","meaning":"bill","synonyms":"bill","antonyms":"—","verbForm":"invoice","nounForm":"invoice","japanese":"請求書"},{"word":"withholding","example":"The company is responsible for PIT withholding","meaning":"holding back tax","synonyms":"deduction","antonyms":"release","verbForm":"withhold","nounForm":"withholding","japanese":"源泉徴収"},{"word":"exemption","example":"Is there any tax exemption for these allowances?","meaning":"freedom from obligation","synonyms":"exception","antonyms":"obligation","verbForm":"exempt","nounForm":"exemption","japanese":"免除、控除"},{"word":"requirement","example":"Does this meet the legal requirements in Vietnam?","meaning":"necessity","synonyms":"necessity","antonyms":"optional","verbForm":"require","nounForm":"requirement","japanese":"必要条件、要件"},{"word":"negotiate","example":"I will negotiate a better price with the supplier","meaning":"discuss terms","synonyms":"bargain","antonyms":"refuse","verbForm":"negotiate","nounForm":"negotiation","japanese":"交渉する"},{"word":"collaboration","example":"We look forward to a successful collaboration","meaning":"working together","synonyms":"cooperation","antonyms":"conflict","verbForm":"collaborate","nounForm":"collaboration","japanese":"協力、提携"},{"word":"inquiry","example":"Thank you for your inquiry about our health check-ups","meaning":"question","synonyms":"question","antonyms":"answer","verbForm":"inquire","nounForm":"inquiry","japanese":"問い合わせ"},{"word":"representative","example":"I am the representative of DYM Medical Center Hanoi","meaning":"acting for others","synonyms":"agent","antonyms":"—","verbForm":"represent","nounForm":"representation","japanese":"代表者、担当者"},{"word":"affordable","example":"Our pricing is affordable for local companies","meaning":"low cost","synonyms":"cheap","antonyms":"expensive","verbForm":"—","nounForm":"affordability","japanese":"手頃な価格の"},{"word":"establish","example":"We established the clinic to provide Japanese quality","meaning":"to set up","synonyms":"create","antonyms":"destroy","verbForm":"establish","nounForm":"establishment","japanese":"設立する、確立する"},{"word":"furthermore","example":"Furthermore, we offer discounts for corporate clients","meaning":"in addition","synonyms":"moreover","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"さらに"},{"word":"consequently","example":"Consequently, we decided to change the supplier","meaning":"as a result","synonyms":"therefore","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"結果として"},{"word":"essentially","example":"Essentially, we need to improve communication","meaning":"basically","synonyms":"basically","antonyms":"specifically","verbForm":"—","nounForm":"essence","japanese":"本質的に"},{"word":"alternatively","example":"Alternatively, we can use a rental service","meaning":"another option","synonyms":"instead","antonyms":"—","verbForm":"—","nounForm":"—","japanese":"あるいは（別の案として）"},{"word":"prime","example":"Our clinic is in a prime location near your office","meaning":"main or best","synonyms":"main","antonyms":"secondary","verbForm":"—","nounForm":"prime","japanese":"最高の、主要な"},{"word":"seamless","example":"We aim to provide a seamless experience for patients","meaning":"smooth","synonyms":"smooth","antonyms":"rough","verbForm":"—","nounForm":"seamlessness","japanese":"途切れのない、円滑な"},{"word":"exclusive","example":"We can offer an exclusive discount for your staff","meaning":"limited","synonyms":"limited","antonyms":"inclusive","verbForm":"exclude","nounForm":"exclusivity","japanese":"独占的な、限定の"},{"word":"provision","example":"We ensure the provision of high-quality medical services","meaning":"supply or rule","synonyms":"supply","antonyms":"lack","verbForm":"provide","nounForm":"provision","japanese":"提供、支給"},{"word":"category","example":"Which category should this expense fall under?","meaning":"group","synonyms":"group","antonyms":"—","verbForm":"categorize","nounForm":"category","japanese":"カテゴリー、分類"},{"word":"authorization","example":"I need authorization from the general director","meaning":"permission","synonyms":"permission","antonyms":"prohibition","verbForm":"authorize","nounForm":"authorization","japanese":"承認、権限"},{"word":"implementation","example":"We will implement the new rule from next week","meaning":"the act of putting a plan into action","synonyms":"execution","antonyms":"abandonment","verbForm":"implement","nounForm":"implementation","japanese":"実施、導入"},{"word":"compliance","example":"We must ensure compliance with local tax laws","meaning":"following rules or laws","synonyms":"adherence","antonyms":"violation","verbForm":"comply","nounForm":"compliance","japanese":"（法令）遵守"},{"word":"personnel","example":"All personnel must attend the safety training","meaning":"people working in an organization","synonyms":"staff","antonyms":"—","verbForm":"—","nounForm":"personnel","japanese":"全職員、人員"},{"word":"assignment","example":"What is his specific assignment in the clinic?","meaning":"a task or duty given","synonyms":"task","antonyms":"—","verbForm":"assign","nounForm":"assignment","japanese":"任務、割り当て"},{"word":"confirmation","example":"Please send a confirmation email after the meeting","meaning":"proof that something is true","synonyms":"verification","antonyms":"denial","verbForm":"confirm","nounForm":"confirmation","japanese":"確認"},{"word":"adjustment","example":"We need to make an adjustment to the payslip","meaning":"a small change","synonyms":"modification","antonyms":"rigidity","verbForm":"adjust","nounForm":"adjustment","japanese":"調整"},{"word":"contribution","example":"We appreciate your contribution to the team","meaning":"something given to help","synonyms":"donation","antonyms":"withdrawal","verbForm":"contribute","nounForm":"contribution","japanese":"貢献"},{"word":"expansion","example":"We are planning the expansion of our health services","meaning":"increase in size or scope","synonyms":"growth","antonyms":"reduction","verbForm":"expand","nounForm":"expansion","japanese":"拡大、拡張"},{"word":"efficiency","example":"We want to improve the efficiency of our operations","meaning":"ability to work well with little waste","synonyms":"productivity","antonyms":"inefficiency","verbForm":"—","nounForm":"efficiency","japanese":"効率"},{"word":"urgent","example":"This is an urgent request for the AirFit masks","meaning":"requiring immediate attention","synonyms":"pressing","antonyms":"unimportant","verbForm":"—","nounForm":"urgency","japanese":"緊急の"},{"word":"regularly","example":"We have a sales meeting regularly every Monday","meaning":"happening often","synonyms":"frequently","antonyms":"rarely","verbForm":"—","nounForm":"regularity","japanese":"定期的に"},{"word":"promotion","example":"We are running a promotion for check-up packages","meaning":"advancement or advertising","synonyms":"advancement","antonyms":"demotion","verbForm":"promote","nounForm":"promotion","japanese":"促進、宣伝"},{"word":"registration","example":"Please complete the registration at the reception","meaning":"official recording","synonyms":"enrollment","antonyms":"removal","verbForm":"register","nounForm":"registration","japanese":"登録"},{"word":"availability","example":"Please check the doctor's availability for next week","meaning":"state of being available","synonyms":"accessibility","antonyms":"unavailability","verbForm":"—","nounForm":"availability","japanese":"空き状況、有効性"},{"word":"description","example":"Does the job description match the reality?","meaning":"explanation of something","synonyms":"explanation","antonyms":"—","verbForm":"describe","nounForm":"description","japanese":"説明（書）、描写"},{"word":"settle","example":"I will settle the outstanding payment today","meaning":"to resolve or pay","synonyms":"resolve","antonyms":"prolong","verbForm":"settle","nounForm":"settlement","japanese":"清算する、解決する"},{"word":"advise","example":"Please be advised that our office will be closed","meaning":"to give guidance","synonyms":"recommend","antonyms":"discourage","verbForm":"advise","nounForm":"advice","japanese":"知らせる、助言する"},{"word":"minimize","example":"We want to minimize the risk of tax audits","meaning":"to reduce to smallest amount","synonyms":"reduce","antonyms":"maximize","verbForm":"minimize","nounForm":"minimization","japanese":"最小化する"},{"word":"maximize","example":"We should maximize the use of our clinic space","meaning":"to increase to greatest amount","synonyms":"increase","antonyms":"minimize","verbForm":"maximize","nounForm":"maximization","japanese":"最大化する"},{"word":"refine","example":"We need to refine the recruitment interview process","meaning":"to improve by making small changes","synonyms":"improve","antonyms":"worsen","verbForm":"refine","nounForm":"refinement","japanese":"磨きをかける、洗練させる"},{"word":"review","example":"Let's review the monthly sales report together","meaning":"to examine again","synonyms":"assess","antonyms":"ignore","verbForm":"review","nounForm":"review","japanese":"見直す、復習する"},{"word":"determine","example":"We need to determine the final price for the client","meaning":"to decide or find out","synonyms":"decide","antonyms":"guess","verbForm":"determine","nounForm":"determination","japanese":"決定する"},{"word":"facilitate","example":"This system will facilitate better communication","meaning":"to make easier","synonyms":"assist","antonyms":"hinder","verbForm":"facilitate","nounForm":"facilitation","japanese":"容易にする、促進する"},{"word":"coordinate","example":"Please coordinate the schedule with the HR team","meaning":"to organize activities","synonyms":"organize","antonyms":"disrupt","verbForm":"coordinate","nounForm":"coordination","japanese":"調整する"},{"word":"regarding","example":"I am writing regarding the recent site inspection","meaning":"about or concerning","synonyms":"concerning","antonyms":"—","verbForm":"—","nounForm":"regard","japanese":"～に関して"},{"word":"previously","example":"As I mentioned previously, the stock is limited","meaning":"before now","synonyms":"earlier","antonyms":"later","verbForm":"—","nounForm":"—","japanese":"以前に、前述の通り"},{"word":"currently","example":"We are currently reviewing the staff benefits","meaning":"at present","synonyms":"now","antonyms":"previously","verbForm":"—","nounForm":"—","japanese":"現在は"},{"word":"ideally","example":"Ideally, we want to finish this by Friday","meaning":"in a perfect situation","synonyms":"perfectly","antonyms":"poorly","verbForm":"—","nounForm":"ideal","japanese":"理想的には"},{"word":"strictly","example":"This information must be kept strictly confidential","meaning":"in a firm way","synonyms":"firmly","antonyms":"loosely","verbForm":"—","nounForm":"strictness","japanese":"厳格に"},{"word":"approximately","example":"The meeting will take approximately 30 minutes","meaning":"about or roughly","synonyms":"roughly","antonyms":"exactly","verbForm":"—","nounForm":"approximation","japanese":"およそ、約"},{"word":"briefly","example":"Could you briefly explain the current situation?","meaning":"in a short way","synonyms":"shortly","antonyms":"lengthily","verbForm":"—","nounForm":"brevity","japanese":"簡潔に"},{"word":"mutually","example":"We should find a mutually beneficial solution","meaning":"shared by both sides","synonyms":"jointly","antonyms":"individually","verbForm":"—","nounForm":"mutuality","japanese":"相互に"},{"word":"professionally","example":"We must handle this matter professionally","meaning":"in a skilled manner","synonyms":"expertly","antonyms":"unprofessionally","verbForm":"—","nounForm":"professionalism","japanese":"プロとして、専門的に"},{"word":"reliable","example":"We need a reliable partner for medical logistics","meaning":"dependable","synonyms":"dependable","antonyms":"unreliable","verbForm":"rely","nounForm":"reliability","japanese":"信頼できる"},{"word":"compliant","example":"We must stay compliant with Vietnamese laws","meaning":"following rules","synonyms":"obedient","antonyms":"noncompliant","verbForm":"comply","nounForm":"compliance","japanese":"遵守している"},{"word":"prospective","example":"We are meeting a prospective client tomorrow","meaning":"expected or potential","synonyms":"potential","antonyms":"past","verbForm":"—","nounForm":"prospect","japanese":"見込みのある、将来の"},{"word":"discrepancy","example":"We found a discrepancy in the inventory count","meaning":"difference or inconsistency","synonyms":"inconsistency","antonyms":"agreement","verbForm":"—","nounForm":"discrepancy","japanese":"（計算などの）不一致、食い違い"},{"word":"significant","example":"There is a significant improvement in the result","meaning":"important","synonyms":"important","antonyms":"insignificant","verbForm":"signify","nounForm":"significance","japanese":"重大な、かなりの"},{"word":"exceed","example":"The total cost must not exceed the original quote","meaning":"to go beyond","synonyms":"surpass","antonyms":"fall short","verbForm":"exceed","nounForm":"excess","japanese":"～を超える"},{"word":"appendix","example":"Please refer to the appendix for the price list","meaning":"additional section","synonyms":"supplement","antonyms":"—","verbForm":"—","nounForm":"appendix","japanese":"付録、付記"},{"word":"deduction","example":"Social insurance is a mandatory deduction in Vietnam","meaning":"amount taken away","synonyms":"reduction","antonyms":"addition","verbForm":"deduct","nounForm":"deduction","japanese":"（給与からの）控除"},{"word":"incentive","example":"We offer an incentive scheme for our sales team","meaning":"something that motivates","synonyms":"motivation","antonyms":"discouragement","verbForm":"—","nounForm":"incentive","japanese":"インセンティブ、報奨"},{"word":"allowance","example":"The housing allowance is included in his package","meaning":"permitted amount","synonyms":"allocation","antonyms":"restriction","verbForm":"allow","nounForm":"allowance","japanese":"手当"},{"word":"inventory","example":"We conduct an inventory check at the end of each month","meaning":"stock of goods","synonyms":"stock","antonyms":"shortage","verbForm":"—","nounForm":"inventory","japanese":"在庫、棚卸し資産"},{"word":"utilize","example":"","meaning":"to use effectively","synonyms":"use","antonyms":"waste","verbForm":"utilize","nounForm":"utilization","japanese":""}];

// ============================================================
// STATE
// ============================================================
const STORAGE_KEY = 'wordmaster_v2';
let progress = {}; // { wordIndex: { views, correct, wrong } }
let queue = [];
let queueIndex = 0;
let currentMode = 'random';
let currentSort = 'random';
let isFlipped = false;
let sessionAnswers = 0;

function loadProgress() {
  try { progress = JSON.parse(localStorage.getItem(STORAGE_KEY)) || {}; } catch(e) { progress = {}; }
}
function saveProgress() {
  try { localStorage.setItem(STORAGE_KEY, JSON.stringify(progress)); } catch(e){}
}
function getP(i) {
  if (!progress[i]) progress[i] = { views: 0, correct: 0, wrong: 0 };
  return progress[i];
}

// ============================================================
// QUEUE BUILDING
// ============================================================
function buildQueue() {
  let indices = [];
  if (currentMode === 'random') {
    indices = RAW.map((_,i) => i);
  } else if (currentMode === 'unseen') {
    indices = RAW.map((_,i) => i).filter(i => getP(i).views === 0);
    if (indices.length === 0) { showToast('未閲覧の単語がありません'); indices = RAW.map((_,i) => i); }
  } else if (currentMode === 'wrong') {
    indices = RAW.map((_,i) => i).filter(i => getP(i).wrong > 0);
    if (indices.length === 0) { showToast('不正解の単語がありません'); indices = RAW.map((_,i) => i); }
  } else if (currentMode === 'correct') {
    indices = RAW.map((_,i) => i).filter(i => getP(i).correct > 0);
    if (indices.length === 0) { showToast('正解済みの単語がありません'); indices = RAW.map((_,i) => i); }
  }

  // sort
  if (currentSort === 'random') {
    indices = indices.sort(() => Math.random() - 0.5);
  } else if (currentSort === 'views') {
    indices = indices.sort((a,b) => getP(a).views - getP(b).views);
  } else if (currentSort === 'accuracy') {
    indices = indices.sort((a,b) => {
      const pA = getP(a), pB = getP(b);
      const rA = pA.correct + pA.wrong === 0 ? -1 : pA.correct / (pA.correct + pA.wrong);
      const rB = pB.correct + pB.wrong === 0 ? -1 : pB.correct / (pB.correct + pB.wrong);
      return rA - rB;
    });
  }
  queue = indices;
  queueIndex = 0;
}

// ============================================================
// CARD RENDERING
// ============================================================
function renderCard() {
  if (queue.length === 0) return;
  const idx = queue[queueIndex];
  const w = RAW[idx];
  isFlipped = false;
  document.getElementById('cardInner').classList.remove('flipped');
  document.getElementById('actionRow').style.display = 'none';

  // Front
  document.getElementById('cf-word').textContent = w.word;
  document.getElementById('cf-example').textContent = w.example ? `"${w.example.substring(0,100)}${w.example.length>100?'…':''}"` : '';

  // Back
  document.getElementById('cb-meaning').textContent = w.meaning || '—';
  document.getElementById('cb-japanese').textContent = w.japanese || '—';
  document.getElementById('cb-example').textContent = w.example || '—';

  let forms = '';
  if (w.verbForm && w.verbForm !== '—') forms += `<span class="tag">動 ${w.verbForm}</span>`;
  if (w.nounForm && w.nounForm !== '—') forms += `<span class="tag">名 ${w.nounForm}</span>`;
  if (w.synonyms && w.synonyms !== '—') forms += `<span class="tag">類 ${w.synonyms}</span>`;
  if (w.antonyms && w.antonyms !== '—') forms += `<span class="tag">反 ${w.antonyms}</span>`;
  document.getElementById('cb-forms').innerHTML = forms || '—';

  // Counter & progress
  const total = queue.length;
  document.getElementById('cardCounter').textContent = `${queueIndex+1} / ${total}`;
  const pct = Math.round(((queueIndex+1)/total)*100);
  document.getElementById('progressFill').style.width = pct + '%';
  document.getElementById('progressRight').textContent = pct + '%';
  document.getElementById('progressLeft').textContent = `問題 ${queueIndex+1}`;

  // Record view
  const p = getP(idx);
  p.views++;
  saveProgress();
  updateHeader();
}

function flipCard() {
  isFlipped = !isFlipped;
  document.getElementById('cardInner').classList.toggle('flipped', isFlipped);
  if (isFlipped) {
    document.getElementById('actionRow').style.display = 'flex';
  }
}

function speakWord(e) {
  e.stopPropagation();
  const idx = queue[queueIndex];
  const text = RAW[idx].word;
  if ('speechSynthesis' in window) {
    window.speechSynthesis.cancel();
    const utt = new SpeechSynthesisUtterance(text);
    utt.lang = 'en-US'; utt.rate = 0.9;
    window.speechSynthesis.speak(utt);
  } else { showToast('読み上げ非対応'); }
}

function markAnswer(correct) {
  const idx = queue[queueIndex];
  const p = getP(idx);
  if (correct) p.correct++; else p.wrong++;
  sessionAnswers++;
  saveProgress();
  document.getElementById('actionRow').style.display = 'none';
  setTimeout(nextCard, 300);
}

function nextCard() {
  if (queueIndex < queue.length - 1) {
    queueIndex++;
    renderCard();
  } else {
    showToast('🎉 セッション完了！キューの最初に戻ります');
    queueIndex = 0;
    renderCard();
  }
}

function prevCard() {
  if (queueIndex > 0) { queueIndex--; renderCard(); }
  else showToast('最初のカードです');
}

function setMode(mode) {
  currentMode = mode;
  document.querySelectorAll('.mode-tab').forEach(t => t.classList.remove('active'));
  document.getElementById('tab-' + mode).classList.add('active');
  buildQueue();
  renderCard();
}

function setSortMode(sort) {
  currentSort = sort;
  document.querySelectorAll('.sort-pill').forEach(p => p.classList.remove('active'));
  document.getElementById('sort-' + sort).classList.add('active');
  buildQueue();
  renderCard();
}

// ============================================================
// HEADER STATS
// ============================================================
function updateHeader() {
  const total = RAW.length;
  const correct = Object.values(progress).filter(p => p.correct > 0).length;
  document.getElementById('hCorrect').textContent = correct;
  document.getElementById('hTotal').textContent = total;
}

// ============================================================
// LIST VIEW
// ============================================================
function buildList(filter = '') {
  const list = document.getElementById('wordList');
  const f = filter.toLowerCase();
  const items = RAW.map((w,i) => ({w, i}))
    .filter(({w}) => !f || w.word.toLowerCase().includes(f) || w.meaning.toLowerCase().includes(f) || w.japanese.toLowerCase().includes(f));

  list.innerHTML = items.slice(0, 200).map(({w,i}) => {
    const p = getP(i);
    const total = p.correct + p.wrong;
    const rate = total === 0 ? null : Math.round(p.correct/total*100);
    return `<div class="word-item" onclick="jumpToCard(${i})">
      <div class="word-item-left">
        <div class="wi-word">${w.word}</div>
        <div class="wi-meaning">${w.meaning.substring(0,50)}</div>
      </div>
      <div class="word-item-right">
        <div class="wi-views">👁 ${p.views}</div>
        <div class="wi-correct ${rate===null?'none':rate>=70?'good':'bad'}">${rate===null?'未回答':rate+'%'}</div>
      </div>
    </div>`;
  }).join('');
  if (items.length > 200) list.innerHTML += `<div style="text-align:center;padding:12px;color:var(--text2);font-size:12px;">+${items.length-200}件 — 検索で絞り込んでください</div>`;
}

function filterList() {
  buildList(document.getElementById('searchInput').value);
}

function jumpToCard(idx) {
  // find in queue or rebuild
  buildQueue();
  const pos = queue.indexOf(idx);
  if (pos !== -1) { queueIndex = pos; }
  else { queue.unshift(idx); queueIndex = 0; }
  switchView('study');
  renderCard();
}

// ============================================================
// STATS VIEW
// ============================================================
function renderStats() {
  const total = RAW.length;
  const viewed = Object.values(progress).filter(p => p.views > 0).length;
  const correct = Object.values(progress).filter(p => p.correct > 0).length;
  const wrong = Object.values(progress).filter(p => p.wrong > 0 && p.correct === 0).length;
  const unseen = total - viewed;

  document.getElementById('stat-total').innerHTML = `${total}<span class="unit">語</span>`;
  document.getElementById('stat-viewed').innerHTML = `${viewed}<span class="unit">語</span>`;
  document.getElementById('stat-session').innerHTML = `${sessionAnswers}<span class="unit">回答</span>`;
  document.getElementById('leg-correct').textContent = `正解: ${correct}語`;
  document.getElementById('leg-wrong').textContent = `不正解: ${wrong}語`;
  document.getElementById('leg-unseen').textContent = `未学習: ${unseen}語`;

  const canvas = document.getElementById('donut');
  const ctx = canvas.getContext('2d');
  canvas.width = 80; canvas.height = 80;
  const cx = 40, cy = 40, r = 30, lw = 10;
  const data = [
    { val: correct, color: '#6affcf' },
    { val: wrong, color: '#ff6a8a' },
    { val: Math.max(0, unseen), color: '#22222e' }
  ];
  const sum = data.reduce((a,d) => a+d.val, 0) || 1;
  let start = -Math.PI/2;
  ctx.clearRect(0,0,80,80);
  data.forEach(d => {
    const angle = (d.val / sum) * Math.PI * 2;
    ctx.beginPath(); ctx.arc(cx,cy,r,start,start+angle);
    ctx.strokeStyle = d.color; ctx.lineWidth = lw;
    ctx.stroke();
    start += angle;
  });
}

function resetProgress() {
  if (confirm('進捗をリセットしますか？')) {
    progress = {}; sessionAnswers = 0;
    saveProgress(); updateHeader(); renderStats();
    showToast('✅ リセット完了');
  }
}

// ============================================================
// VIEW SWITCHING
// ============================================================
function switchView(name) {
  document.querySelectorAll('.view').forEach(v => v.classList.remove('active'));
  document.getElementById('view-' + name).classList.add('active');
  document.querySelectorAll('.bnav-item').forEach(b => b.classList.remove('active'));
  document.getElementById('bnav-' + name).classList.add('active');
  if (name === 'list') buildList();
  if (name === 'stats') renderStats();
}

// ============================================================
// TOAST
// ============================================================
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg; t.classList.add('show');
  setTimeout(() => t.classList.remove('show'), 2500);
}

// ============================================================
// SWIPE SUPPORT
// ============================================================
(function() {
  let startX = 0, startY = 0;
  const el = document.getElementById('cardOuter');
  el.addEventListener('touchstart', e => { startX = e.touches[0].clientX; startY = e.touches[0].clientY; }, { passive: true });
  el.addEventListener('touchend', e => {
    const dx = e.changedTouches[0].clientX - startX;
    const dy = e.changedTouches[0].clientY - startY;
    if (Math.abs(dx) > Math.abs(dy) && Math.abs(dx) > 50) {
      if (dx < 0) nextCard(); else prevCard();
    }
  });
})();

// ============================================================
// INIT
// ============================================================
loadProgress();
buildQueue();
renderCard();
updateHeader();
</script>
</body>
</html>
