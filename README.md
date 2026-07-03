<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA - 企業デトックス面接SaaS -</title>
    <style>
        :root { 
            --bg: linear-gradient(135deg, #f0f7ff, #ffffff); 
            --panel: #ffffff; 
            --text: #1e293b; 
            --subtitle-color: #64748b;
            --accent: #0284c7; 
            --badge-bg: #e0f2fe;
            --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6);
            --lavender-hover: linear-gradient(135deg, #c084fc, #7c3aed);
        }
        body { font-family: 'Segoe UI', system-ui, sans-serif; background: var(--bg); background-attachment: fixed; margin: 0; padding: 60px 20px; color: var(--text); }
        .container { max-width: 800px; margin: 0 auto; background: var(--panel); padding: 50px 40px; border-radius: 24px; box-shadow: 0 15px 35px rgba(2,132,199,0.08); border: 1px solid #e2e8f0; }
        h1 { color: #0f172a; text-align: center; font-size: 34px; letter-spacing: 2px; margin-bottom: 5px; font-weight: 900; }
        .subtitle { text-align: center; color: var(--subtitle-color); margin-bottom: 50px; font-size: 15px; }
        .info-badges { display: flex; justify-content: center; gap: 20px; font-size: 13px; font-weight: 700; }
        .badge { background: var(--badge-bg); padding: 10px 20px; border-radius: 30px; display: flex; align-items: center; gap: 8px; }
        .badge-lock { color: #0369a1; }
        .badge-time { color: #b45309; }
        .start-btn { width: 100%; background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 22px; font-size: 20px; font-weight: 800; border-radius: 16px; cursor: pointer; margin-top: 40px; box-shadow: 0 4px 15px rgba(2,132,199,0.2); transition: 0.3s; letter-spacing: 4px; }
        .start-btn:hover { transform: translateY(-3px); box-shadow: 0 6px 20px rgba(2,132,199,0.3); }
        .next-btn { width: 100%; background: var(--lavender); color: white; border: none; padding: 18px; font-size: 18px; font-weight: bold; border-radius: 12px; cursor: pointer; margin-top: 30px; box-shadow: 0 4px 15px rgba(139,92,246,0.2); transition: 0.2s; }
        .next-btn:hover { transform: translateY(-2px); background: var(--lavender-hover); box-shadow: 0 6px 20px rgba(139,92,246,0.3); }
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 550px; padding: 40px; border-radius: 24px; border: 1px solid #e2e8f0; text-align: center; box-shadow: 0 20px 40px rgba(0,0,0,0.1); }
        .guide-title { font-size: 24px; font-weight: 800; color: #0f172a; margin-bottom: 25px; }
        .guide-steps { text-align: left; margin-bottom: 30px; }
        .step-item { background: #f8fafc; padding: 15px; border-radius: 12px; margin-bottom: 12px; border: 1px solid #e2e8f0; display: flex; align-items: center; gap: 15px; }
        .step-num { background: #0284c7; color: #ffffff; font-weight: 900; width: 28px; height: 28px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 14px; flex-shrink: 0; }
        .step-text { color: #334155; font-size: 14px; line-height: 1.5; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 14px 40px; font-size: 16px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; transition: 0.2s; }
        .close-guide-btn:hover { background: #0284c7; }
        .page { display: block; }
        .survey-page { display: none; margin-top: 30px; animation: fadeIn 0.4s ease; }
        .question-card { background: #f8fafc; padding: 25px; border-radius: 16px; border: 1px solid #e2e8f0; margin-bottom: 20px; }
        .question-title { font-size: 16px; font-weight: 700; color: #0f172a; margin-bottom: 15px; display: block; line-height: 1.5; }
        .options-group { display: flex; justify-content: space-between; gap: 10px; }
        .option-label { flex: 1; text-align: center; background: #ffffff; padding: 12px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 13px; color: #64748b; cursor: pointer; transition: 0.2s; }
        .option-label:hover { background: #f0fdf4; color: #166534; border-color: #22c55e; }
        input[type="radio"] { display: none; }
        input[type="radio"]:checked + .option-label { background: linear-gradient(135deg, #22c55e, #16a34a); color: #fff; border-color: #15803d; font-weight: bold; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
    </style>
</head>
<body>

    <!-- 説明画面 -->
    <div class="overlay" id="guideOverlay">
        <div class="guide-box">
            <div class="guide-title">🚀 LUMINA へようこそ</div>
            <p style="color: #64748b; font-size: 14px; margin-bottom: 25px;">学歴社会に変革を起こし、組織のドロドロを消し去るための3ステップガイド</p>
            <div class="guide-steps">
                <div class="step-item"><div class="step-num">1</div><div class="step-text"><strong>社内アンケートの実施</strong><br>社員に「本音を暴く20の質問」に完全匿名で回答してもらいます。</div></div>
                <div class="step-item"><div class="step-num">2</div><div class="step-text"><strong>全自動デトックス分析</strong><br>「アンケートを開始する」を押すと、全5問×4章の本格診断がスタートします。</div></div>
                <div class="step-item"><div class="step-num">3</div><div class="step-text"><strong>光の人材を一本釣り</strong><br>会社の弱みを隠した面接質問を自動生成。学歴不問のヒーローを見抜きます。</div></div>
            </div>
            <button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA コックピットを起動する</button>
        </div>
    </div>

    <!-- 🏠 1ページ目 -->
    <div class="container page" id="topPage">
        <h1>🚀 企業デトックス面接SaaS『LUMINA』</h1>
        <div class="subtitle">学歴社会に変革を起こす、最先端の組織デトックス・コックピット</div>
        <div class="info-badges">
            <div class="badge badge-lock">🔒 完全匿名（回答した個人は絶対に特定されません）</div>
            <div class="badge badge-time">⏳ 所要時間：約5分（全20問の本格デトックス）</div>
        </div>
        <button class="start-btn" onclick="document.getElementById('topPage').style.display='none'; document.getElementById('page1').style.display='block'; window.scrollTo(0,0);">アンケートを開始する</button>
    </div>

    <!-- 📊 第1章 -->
    <div class="container survey-page" id="page1">
        <h1>📊 第1章：上司・ハラスメント of 診断</h1>
        <div class="subtitle">まずは社内の「上司の空気や理不尽さ」について教えてください。（1/4）</div>
        <div class="question-card"><span class="question-title">Q1. 上司が不機嫌なとき、職場の空気は悪くなりますか？</span><div class="options-group"><input type="radio" id="q1_5" name="q1" value="5"><label for="q1_5" class="option-label">めちゃくちゃ悪い</label><input type="radio" id="q1_3" name="q1" value="3"><label for="q1_3" class="option-label">たまに気を遣う</label><input type="radio" id="q1_1" name="q1" value="1"><label for="q1_1" class="option-label">いつも穏やか</label></div></div>
        <div class="question-card"><span class="question-title">Q2. この会社に誰も逆らえない「王様」のようなワンマンな人はいますか？</span><div class="options-group"><input type="radio" id="q2_5" name="q2" value="5"><label for="q2_5" class="option-label">完全に独裁状態</label><input type="radio" id="q2_3" name="q2" value="3"><label for="q2_3" class="option-label">一部にボスがいる</label><input type="radio" id="q2_1" name="q2" value="1"><label for="q2_1" class="option-label">みんな平等</label></div></div>
        <div class="question-card"><span class="question-title">Q3. ミスをしたとき、怒られるのが怖くて報告をわざと遅らせたことがありますか？</span><div class="options-group"><input type="radio" id="q3_5" name="q3" value="5"><label for="q3_5" class="option-label">怖くて隠しちゃう</label><input type="radio" id="q3_3" name="q3" value="3"><label for="q3_3" class="option-label">たまに躊躇する</label><input type="radio" id="q3_1" name="q3" value="1"><label for="q3_1" class="option-label">即座に共有できる</label></div></div>
        <div class="question-card"><span class="question-title">Q4. 上司から言われた言葉で、「これ今の時代ならパワハラでは？」と傷ついた言葉はありますか？</span><div class="options-group"><input type="radio" id="q4_5" name="q4" value="5"><label for="q4_5" class="option-label">頻繁にある</label><input type="radio" id="q4_3" name="q4" value="3"><label for="q4_3" class="option-label">一度だけある</label><input type="radio" id="q4_1" name="q4" value="1"><label for="q4_1" class="option-label">一切ない</label></div></div>
        <div class="question-card"><span class="question-title">Q5. 手柄は全部上司のものになり、ミスをしたときだけ部下のせいにされる瞬間はありますか？</span><div class="options-group"><input type="radio" id="q5_5" name="q5" value="5"><label for="q5_5" class="option-label">いつもそう</label><input type="radio" id="q5_3" name="q5" value="3"><label for="q5_3" class="option-label">たまに感じる</label><input type="radio" id="q5_1" name="q5" value="1"><label for="q5_1" class="option-label">正当に評価される</label></div></div>
        <button class="next-btn" onclick="document.getElementById('page1').style.display='none'; document.getElementById('page2').style.display='block'; window.scrollTo(0,0);">第2章（業務効率の診断）へ進む</button>
    </div>

    <!-- 🛠️ 第2章 -->
    <div class="container survey-page" id="page2">
        <h1>🛠️ 第2章：仕事の進め方・無駄の診断</h1>
        <div class="subtitle">次に、日々の業務の効率や理不尽な作業ルールについて教えてください。（2/4）</div>
        <div class="question-card"><span class="question-title">Q6. 毎日やっている仕事の中に、「マジでやる意味ないだろ」という無駄な作業はありますか？</span><div class="options-group"><input type="radio" id="q6_5" name="q6" value="5"><label for="q6_5" class="option-label">無駄だらけ</label><input type="radio" id="q6_3" name="q6" value="3"><label for="q6_3" class="option-label">たまにある</label><input type="radio" id="q6_1" name="q6" value="1"><label for="q6_1" class="option-label">一切ない</label></div></div>
