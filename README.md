<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA</title>
    <style>
        :root { --bg: linear-gradient(135deg, #f0f7ff, #ffffff); --panel: #ffffff; --text: #1e293b; --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6); }
        body { font-family: sans-serif; background: var(--bg); margin: 0; padding: 30px 10px; color: var(--text); }
        .container { max-width: 550px; margin: 0 auto; background: var(--panel); padding: 25px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; }
        h1 { text-align: center; font-size: 24px; margin-bottom: 5px; }
        .subtitle { text-align: center; color: #64748b; margin-bottom: 25px; font-size: 13px; }
        .start-btn { width: 100%; background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 16px; font-size: 16px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 20px; }
        .next-btn { width: 100%; background: var(--lavender); color: white; border: none; padding: 14px; font-size: 15px; font-weight: bold; border-radius: 10px; cursor: pointer; margin-top: 15px; }
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 400px; padding: 25px; border-radius: 20px; text-align: center; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 12px 30px; font-size: 14px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; }
        .survey-page { display: none; margin-top: 15px; }
        .question-card { background: #f8fafc; padding: 15px; border-radius: 12px; border: 1px solid #e2e8f0; margin-bottom: 12px; }
        .question-title { font-size: 14px; font-weight: 700; margin-bottom: 8px; display: block; }
        .options-group { display: flex; justify-content: space-between; gap: 6px; }
        .option-label { flex: 1; text-align: center; background: #ffffff; padding: 8px; border-radius: 6px; border: 1px solid #cbd5e1; font-size: 12px; color: #64748b; cursor: pointer; }
        input[type="radio"] { display: none; }
        input[type="radio"]:checked + .option-label { background: linear-gradient(135deg, #22c55e, #16a34a); color: #fff; border-color: #15803d; font-weight: bold; }
    </style>
</head>
<body>

    <div class="overlay" id="guideOverlay">
        <div class="guide-box">
            <h2>🚀 LUMINA へようこそ</h2>
            <p style="color:#64748b; font-size:12px; margin-bottom:20px;">学歴社会に変革を起こし、組織の闇を消し去る3ステップガイド</p>
            <button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA を起動する</button>
        </div>
    </div>

    <div class="container" id="topPage">
        <h1>🚀 企業デトックス面接SaaS『LUMINA』</h1>
        <div class="subtitle">学歴社会に変革を起こす、最先端の組織デトックス・コックピット</div>
        <button class="start-btn" onclick="document.getElementById('topPage').style.display='none'; document.getElementById('page1').style.display='block'; window.scrollTo(0,0);">アンケートを開始する</button>
    </div>

    <!-- 📊 第1章 -->
    <div class="container survey-page" id="page1">
        <h2>📊 第1章：上戦・ハラスメントの診断</h2>
        <div class="question-card"><span class="question-title">Q1. 上司が不機嫌なとき、職場の空気は悪くなりますか？</span><div class="options-group"><input type="radio" id="q1_5" name="q1"><label for="q1_5" class="option-label">悪い</label><input type="radio" id="q1_3" name="q1"><label for="q1_3" class="option-label">普通</label><input type="radio" id="q1_1" name="q1"><label for="q1_1" class="option-label">穏やか</label></div></div>
        <div class="question-card"><span class="question-title">Q2. 誰も逆らえないワンマンなボスはいますか？</span><div class="options-group"><input type="radio" id="q2_5" name="q2"><label for="q2_5" class="option-label">いる</label><input type="radio" id="q2_3" name="q2"><label for="q2_3" class="option-label">たまに</label><input type="radio" id="q2_1" name="q2"><label for="q2_1" class="option-label">いない</label></div></div>
        <div class="question-card"><span class="question-title">Q3. ミスを怒られるのが怖くて報告を遅らせたことがありますか？</span><div class="options-group"><input type="radio" id="q3_5" name="q3"><label for="q3_5" class="option-label">ある</label><input type="radio" id="q3_3" name="q3"><label for="q3_3" class="option-label">たまに</label><input type="radio" id="q3_1" name="q3"><label for="q3_1" class="option-label">ない</label></div></div>
        <div class="question-card"><span class="question-title">Q4. 上司の言葉で傷ついた経験はありますか？</span><div class="options-group"><input type="radio" id="q4_5" name="q4"><label for="q4_5" class="option-label">ある</label><input type="radio" id="q4_3" name="q4"><label for="q4_3" class="option-label">一度だけ</label><input type="radio" id="q4_1" name="q4"><label for="q4_1" class="option-label">ない</label></div></div>
        <div class="question-card"><span class="question-title">Q5. 手柄は上司のもの、ミスは部下のせいにされますか？</span><div class="options-group"><input type="radio" id="q5_5" name="q5"><label for="q5_5" class="option-label">いつもそう</label><input type="radio" id="q5_3" name="q5"><label for="q5_3" class="option-label">たまに</label><input type="radio" id="q5_1" name="q5"><label for="q5_1" class="option-label">正当評価</label></div></div>
        <button class="next-btn" onclick="document.getElementById('page1').style.display='none'; document.getElementById('page2').style.display='block'; window.scrollTo(0,0);">第2章（業務効率の診断）へ進む</button>
    </div>

    <!-- 🛠️ 第2章 -->
    <div class="container survey-page" id="page2">
        <h2>🛠️ 第2章：仕事の進め方・無駄の診断</h2>
        <div class="question-card"><span class="question-title">Q6. 仕事の中に「やる意味がない」と思う無駄はありますか？</span><div class="options-group"><input type="radio" id="q6_5" name="q6"><label for="q6_5" class="option-label">ある</label><input type="radio" id="q6_3" name="q6"><label for="q6_3" class="option-label">たまに</label><input type="radio" id="q6_1" name="q6"><label for="q6_1" class="option-label">ない</label></div></div>
        <div class="question-card"><span class="question-title">Q7. 決断をもらうためのたらい回しは起きていますか？</span><div class="options-group"><input type="radio" id="q7_5" name="q7"><label for="q7_5" class="option-label">遅い</label><input type="radio" id="q7_3" name="q7"><label for="q7_3" class="option-label">普通</label><input type="radio" id="q7_1" name="q7"><label for="q7_1" class="option-label">早い</label></div></div>
        <div class="question-card"><span class="question-title">Q8. マニュアルがなく背中を見て覚えろと言われますか？</span><div class="options-group"><input type="radio" id="q8_5" name="q8"><label for="q8_5" class="option-label">困る</label><input type="radio" id="q8_3" name="q8"><label for="q8_3" class="option-label">たまに</label><input type="radio" id="q8_1" name="q8"><label for="q8_1" class="option-label">整っている</label></div></div>
        <div class="question-card"><span class="question-title">Q9. トラブル時に解決より犯人探しをする空気はありますか？</span><div class="options-group"><input type="radio" id="q9_5" name="q9"><label for="q9_5" class="option-label">ある</label><input type="radio" id="q9_3" name="q9"><label for="q9_3" class="option-label">たまに</label><input type="radio" id="q9_1" name="q9"><label for="q9_1" class="option-label">助け合える</label></div></div>
        <div class="question-card"><span class="question-title">Q10. 古いルールや非効率な作業を強要されますか？</span><div class="options-group"><input type="radio" id="q10_5" name="q10"><label for="q10_5" class="option-label">多い</label><input type="radio" id="q10_3" name="q10"><label for="q10_3" class="option-label">少しある</label><input type="radio" id="q10_1" name="q10"><label for="q10_1" class="option-label">スマート</label></div></div>
        <button class="next-btn" onclick="document.getElementById('page2').style.display='none'; document.getElementById('page3').style.display='block'; window.scrollTo(0,0);">第3章（社内連携の診断）へ進む</button>
    </div>

    <!-- 🎐 第3章 -->
    <div class="container survey-page" id="page3">
        <h2>🎐 第3章：社内連携・人間関係の診断</h2>
        <div class="question-card"><span class="question-title">Q11. 部署同士の連携が悪く、押し付け合いはありますか？</span><div class="options-group"><input type="radio" id="q11_5" name="q11"><label for="q11_5" class="option-label">酷い</label><input type="radio" id="q11_3" name="q11"><label for="q11_3" class="option-label">たまに</label><input type="radio" id="q11_1" name="q11"><label for="q11_1" class="option-label">ない</label></div></div>
        <div class="question-card"><span class="question-title">Q12. 真面目な人より、立ち回りが上手い人が評価されますか？</span><div class="options-group"><input type="radio" id="q12_5" name="q12"><label for="q12_5" class="option-label">常にそう</label><input type="radio" id="q12_3" name="q12"><label for="q12_3" class="option-label">多少ある</label><input type="radio" id="q12_1" name="q12"><label for="q12_1" class="option-label">実力評価</label></div></div>
        <div class="question-card"><span class="question-title">Q13. 会社への不満や愚痴は、陰で多く話されていますか？</span><div class="options-group"><input type="radio" id="q13_5" name="q13"><label for="q13_5" class="option-label">多い</label><input type="radio" id="q13_3" name="q13"><label for="q13_3" class="option-label">たまに</label><input type="radio" id="q13_1" name="q13"><label for="q13_1" class="option-label">ほぼない</label></div></div>
        <div class="question-card"><span class="question-title">Q14. 職場の空気のせいで、新人がすぐ辞めてしまいますか？</span><div class="options-group"><input type="radio" id="q14_5" name="q14"><label for="q14_5" class="option-label">すぐ辞める</label><input type="radio" id="q14_3" name="q14"><label for="q14_3" class="option-label">たまに</label><input type="radio" id="q14_1" name="q14"><label for="q14_1" class="option-label">長く続く</label></div></div>
