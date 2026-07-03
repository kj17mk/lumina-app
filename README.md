<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA</title>
    <style>
        :root { --bg: linear-gradient(135deg, #f0f7ff, #ffffff); --panel: #ffffff; --text: #1e293b; --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6); }
        body { font-family: sans-serif; background: var(--bg); margin: 0; padding: 30px 10px; color: var(--text); }
        .container { max-width: 650px; margin: 0 auto; background: var(--panel); padding: 25px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; }
        h1 { text-align: center; font-size: 24px; margin-bottom: 5px; }
        .subtitle { text-align: center; color: #64748b; margin-bottom: 25px; font-size: 13px; }
        .start-btn { width: 100%; background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 16px; font-size: 16px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 20px; }
        
        /* 💡 戻るボタンと進むボタンを横並びにするスタイル設定 */
        .btn-group { display: flex; gap: 10px; margin-top: 20px; }
        .back-btn { flex: 1; background: #e2e8f0; color: #475569; border: none; padding: 14px; font-size: 15px; font-weight: bold; border-radius: 10px; cursor: pointer; }
        .next-btn { flex: 2; background: var(--lavender); color: white; border: none; padding: 14px; font-size: 15px; font-weight: bold; border-radius: 10px; cursor: pointer; }
        
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 400px; padding: 25px; border-radius: 20px; text-align: center; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 12px 30px; font-size: 14px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; }
        .survey-page { display: none; margin-top: 15px; }
        .question-card { background: #f8fafc; padding: 15px; border-radius: 12px; border: 1px solid #e2e8f0; margin-bottom: 12px; }
        .question-title { font-size: 14px; font-weight: 700; margin-bottom: 8px; display: block; }
        .options-group { display: flex; justify-content: space-between; gap: 4px; }
        .option-button { flex: 1; text-align: center; background: #ffffff; padding: 8px 4px; border-radius: 6px; border: 1px solid #cbd5e1; font-size: 11px; color: #64748b; cursor: pointer; }
        .option-button.selected { background: linear-gradient(135deg, #22c55e, #16a34a); color: #fff; border-color: #15803d; font-weight: bold; }
    </style>
</head>
<body>

    <div class="overlay" id="guideOverlay"><div class="guide-box"><h2>🚀 LUMINA へようこそ</h2><p style="color:#64748b; font-size:12px; margin-bottom:20px;">学歴社会に変革を起こし、組織のドロドロを消し去るための3ステップガイド</p><button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA を起動する</button></div></div>
    <div class="container" id="topPage"><h1>🚀 企業デトックス面接SaaS『LUMINA』</h1><div class="subtitle">学歴社会に変革を起こす、最先端の組織デトックス・コックピット</div><button class="start-btn" onclick="document.getElementById('topPage').style.display='none'; document.getElementById('page1').style.display='block'; window.scrollTo(0,0);">アンケートを開始する</button></div>

    <!-- 📊 第1章 -->
    <div class="container survey-page" id="page1">
        <h2>📊 第1章：上司・ハラスメントの診断</h2>
        <div class="question-card"><span class="question-title">Q1. 上司が不機嫌なとき、職場の空気は悪くなりますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">最悪</div><div class="option-button" onclick="selectOpt(this)">悪い</div><div class="option-button" onclick="selectOpt(this)">普通</div><div class="option-button" onclick="selectOpt(this)">平気</div><div class="option-button" onclick="selectOpt(this)">穏やか</div></div></div>
        <div class="question-card"><span class="question-title">Q2. 誰も逆らえないワンマンなボスはいますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">独裁</div><div class="option-button" onclick="selectOpt(this)">いる</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">いない</div></div></div>
        <div class="question-card"><span class="question-title">Q3. ミスを怒られるのが怖くて報告を遅らせたことがありますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">常にある</div><div class="option-button" onclick="selectOpt(this)">ある</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">即報告</div></div></div>
        <div class="question-card"><span class="question-title">Q4. 上司の言葉で傷ついた経験はありますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">常に傷つく</div><div class="option-button" onclick="selectOpt(this)">ある</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">一切ない</div></div></div>
        <div class="question-card"><span class="question-title">Q5. 手柄は上司のもの、ミスは部下のせいにされますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">絶対そう</div><div class="option-button" onclick="selectOpt(this)">多い</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">正当評価</div></div></div>
        <div class="btn-group">
            <button class="back-btn" onclick="document.getElementById('page1').style.display='none'; document.getElementById('topPage').style.display='block'; window.scrollTo(0,0);">戻る</button>
            <button class="next-btn" onclick="document.getElementById('page1').style.display='none'; document.getElementById('page2').style.display='block'; window.scrollTo(0,0);">第2章へ進む</button>
        </div>
    </div>

    <!-- 🛠️ 第2章 -->
    <div class="container survey-page" id="page2">
        <h2>🛠️ 第2章：仕事の進め方・無駄の診断</h2>
        <div class="question-card"><span class="question-title">Q6. 仕事の中に「やる意味がない」と思う無駄はありますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">山ほどある</div><div class="option-button" onclick="selectOpt(this)">多い</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">一切ない</div></div></div>
        <div class="question-card"><span class="question-title">Q7. 決断をもらうためのたらい回しは起きていますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">遅すぎる</div><div class="option-button" onclick="selectOpt(this)">遅い</div><div class="option-button" onclick="selectOpt(this)">普通</div><div class="option-button" onclick="selectOpt(this)">早い</div><div class="option-button" onclick="selectOpt(this)">一瞬</div></div></div>
        <div class="question-card"><span class="question-title">Q8. マニュアルがなく背中を見て覚えろと言われますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">大いに困る</div><div class="option-button" onclick="selectOpt(this)">困る</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">完璧にある</div></div></div>
        <div class="question-card"><span class="question-title">Q9. トラブル時に解決より犯人探しをする空気はありますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">絶対そう</div><div class="option-button" onclick="selectOpt(this)">ある</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">助け合える</div></div></div>
        <div class="question-card"><span class="question-title">Q10. 古いルールや非効率な作業を強要されますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">毎日ある</div><div class="option-button" onclick="selectOpt(this)">多い</div><div class="option-button" onclick="selectOpt(this)">少しある</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">スマート</div></div></div>
        <div class="btn-group">
            <button class="back-btn" onclick="document.getElementById('page2').style.display='none'; document.getElementById('page1').style.display='block'; window.scrollTo(0,0);">戻る</button>
            <button class="next-btn" onclick="document.getElementById('page2').style.display='none'; document.getElementById('page3').style.display='block'; window.scrollTo(0,0);">第3章へ進む</button>
        </div>
    </div>

    <!-- 🎐 第3章 -->
    <div class="container survey-page" id="page3">
        <h2>🎐 第3章：社内連携・人間関係の診断</h2>
        <div class="question-card"><span class="question-title">Q11. 部署同士の連携が悪く、押し付け合いはありますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">最悪に酷い</div><div class="option-button" onclick="selectOpt(this)">酷い</div><div class="option-button" onclick="selectOpt(this)">たまに</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">ない</div></div></div>
        <div class="question-card"><span class="question-title">Q12. 真面目な人より、立ち回りが上手い人が評価されますか？</span><div class="options-group"><div class="option-button" onclick="selectOpt(this)">絶対そう</div><div class="option-button" onclick="selectOpt(this)">常にそう</div><div class="option-button" onclick="selectOpt(this)">多少ある</div><div class="option-button" onclick="selectOpt(this)">ほぼない</div><div class="option-button" onclick="selectOpt(this)">実力評価</div></div></div>
