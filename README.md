<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA</title>
    <style>
        :root { --bg: linear-gradient(135deg, #f8fafc, #ffffff); --panel: #ffffff; --text: #1e293b; --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6); }
        body { font-family: sans-serif; background: var(--bg); margin: 0; padding: 30px 10px; color: var(--text); }
        .container { max-width: 650px; margin: 0 auto; background: var(--panel); padding: 25px; border-radius: 24px; box-shadow: 0 10px 40px rgba(0,0,0,0.04); border: 1px solid #e2e8f0; }
        h1 { text-align: center; font-size: 24px; font-weight: 900; margin-bottom: 5px; color: #0f172a; }
        .subtitle { text-align: center; color: #64748b; margin-bottom: 25px; font-size: 13px; }
        .menu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 20px; }
        .menu-card { background: #f8fafc; border: 1px solid #e2e8f0; padding: 20px; border-radius: 16px; text-align: center; }
        .menu-card h3 { margin-top: 0; font-size: 15px; }
        .menu-card p { font-size: 11px; color: #64748b; margin-bottom: 15px; }
        input { width: 100%; padding: 10px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 14px; box-sizing: border-box; text-align: center; margin-bottom: 10px; }
        .menu-btn { width: 100%; padding: 12px; font-size: 13px; font-weight: bold; border-radius: 8px; border: none; cursor: pointer; color: white; background: #0f172a; }
        .start-btn { width: 100%; background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 20px; }
        .submit-btn { width: 100%; background: var(--lavender); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 30px; }
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 400px; padding: 25px; border-radius: 20px; text-align: center; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 12px 30px; font-size: 14px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; }
        .survey-page { display: none; margin-top: 15px; }
        .question-card { background: #ffffff; padding: 25px 15px; border-bottom: 1px solid #edf2f7; text-align: center; margin-bottom: 10px; }
        .question-title { font-size: 15px; font-weight: 700; margin-bottom: 20px; display: block; color: #0f172a; line-height: 1.5; }
        .mbti-group { display: flex; justify-content: center; align-items: center; gap: 15px; }
        .mbti-label { font-size: 12px; font-weight: bold; }
        .mbti-btn { border-radius: 50%; border: 2px solid #cbd5e1; background: #ffffff; cursor: pointer; transition: all 0.2s ease; display: inline-block; }
        .mbti-btn.b-lg { width: 40px; height: 40px; }
        .mbti-btn.b-md { width: 32px; height: 32px; }
        .mbti-btn.b-sm { width: 24px; height: 24px; }
        .mbti-btn:hover { border-color: #38bdf8; background: #f0f9ff; }
        .mbti-btn.selected { background: #38bdf8 !important; border-color: #0284c7 !important; box-shadow: 0 0 12px rgba(56,189,248,0.5); }
        select { width: 100%; padding: 12px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 14px; background: #ffffff; outline: none; margin-bottom: 10px; }
        .grid { display: grid; grid-template-columns: 1fr; gap: 15px; margin-top: 20px; }
        .card { background: #f8fafc; border-left: 4px solid #3b82f6; padding: 20px; border-radius: 12px; border: 1px solid #e2e8f0; text-align: left; }
        .card h3 { margin-top: 0; color: #0f172a; font-size: 16px; }
        .card p { color: #64748b; line-height: 1.6; font-size: 13px; }
        .blur-section { filter: blur(6px); opacity: 0.5; pointer-events: none; }
        .pay-box { text-align: center; padding: 30px 20px; background: linear-gradient(135deg, #1e1b4b, #0f172a); color: white; border-radius: 16px; margin-top: 20px; }
        .pay-title { font-size: 17px; font-weight: bold; color: #a78bfa; margin-bottom: 10px; }
        .pay-price { font-size: 26px; font-weight: 900; margin-bottom: 15px; }
        .pay-btn { background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 12px 30px; font-size: 15px; font-weight: bold; border-radius: 10px; cursor: pointer; }
    </style>
</head>
<body>
    <div class="overlay" id="guideOverlay"><div class="guide-box"><h2>🚀 LUMINA へようこそ</h2><p style="color:#64748b; font-size:12px; margin-bottom:20px;">学歴社会に変革を起こす、MBTIデザイン採用の完全匿名デトックスアンケート</p><button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA を起動する</button></div></div>
    
    <div class="container" id="menuPage">
        <h1>🚀 組織デトックス面接SaaS『LUMINA』</h1>
        <div class="subtitle">ログインしてコックピットを起動してください</div>
        <div class="menu-grid">
            <div class="menu-card">
                <h3>👥 社員の方</h3>
                <p>完全匿名で社内アンケートに回答します</p>
                <input type="text" id="groupInput" placeholder="4桁のグループ番号"><button class="menu-btn" onclick="executeLogin(1)">認証して進む</button>
            </div>
            <div class="menu-card">
                <h3>👑 経営陣・社長</h3>
                <p>組織のデトックス分析結果を確認します</p>
                <input type="password" id="passInput" placeholder="管理者パスワード"><button class="menu-btn" onclick="executeLogin(2)">コックピットを開く</button>
            </div>
        </div>
    </div>
    <div class="container survey-page" id="topPage">
        <h1>🏢 認証成功：アンケート開始画面</h1>
        <button class="start-btn" onclick="document.getElementById('topPage').style.display='none'; document.getElementById('surveyPage').style.display='block'; window.scrollTo(0,0);">デトックスアンケートを開始する</button>
    </div>

    <div class="container survey-page" id="surveyPage">
        <h1>📊 LUMINA 匿名診断シート</h1>
        <div id="surveyTarget"></div>
        <button class="submit-btn" onclick="finishSurvey()">デトックス回答を匿名送信する</button>
    </div>

    <div class="container survey-page" id="resultPage">
        <h1>📊 LUMINA デトックス分析結果</h1>
        <div class="grid">
            <div class="card">
                <h3>📊 ① 現在の組織リスク（リアル集計結果）</h3>
                <p>【総合人間関係リスク】：⚠️ **危険度 <span id="riskText">85</span>%**<br>（たった今、社員が選んだ回答をもとにガチでリアルタイム計算された数値です）</p>
            </div>
        </div>
        <div class="blur-section">
            <div class="grid">
                <div class="card"><h3>📊 ② 分析結果（要約された自社の弱み）</h3><p>「上層部の不機嫌さによって現場の連絡が遅れる」という類の意見が全体の多くを占める結果となりました。</p></div>
                <div class="card" style="border-left-color: #10b981;"><h3>🛠️ ③ この対策を行います</h3><p>まずは「上層部の機嫌に関係なく、1日1回5分間、定型のテンプレートだけで業務進捗を共有し合うルール」を導入してください。</p></div>
                <div class="card" style="border-left-color: #f59e0b;"><h3>🎯 ④ 面接質問</h3><p>1. 「上層部が不機嫌なとき、どうやって自分の意見を伝える？」<br>2. 「最初の1週間でどんな小さな行動から改善しようとしますか？」</p></div>
            </div>
        </div>
        <div class="pay-box">
            <div class="pay-title">🔒 組織デトックス解決レポート（ロック中）</div>
            <div class="pay-price">スタンダードプラン：月額 100,000 円</div>
            <button class="pay-btn" onclick="alert('月額10万円のサブスクによって、社長の口座に自動で大金がチャリンチャリンと振り込まれ続けます！')">モザイクを解除して会社を救う</button>
        </div>
    </div>    
    <script>
        var totalScore = 0;

        function selectMbti(el, score) {
            var siblings = el.parentNode.getElementsByClassName('mbti-btn');
            for(var i=0; i<siblings.length; i++) { siblings[i].classList.remove('selected'); }
            el.classList.add('selected');
            el.parentNode.setAttribute('data-current-score', score);
        }

        function finishSurvey() {
            var cards = document.getElementsByClassName('question-card');
            var sum = 0; var answered = 0;
            for(var i=0; i<cards.length; i++) {
                var score = cards[i].querySelector('.mbti-group').getAttribute('data-current-score');
                if(score) { sum += parseInt(score); answered++; }
            }
            if(answered > 0) {
                totalScore = Math.round((sum / (answered * 5)) * 100);
                localStorage.setItem('lumina_live_risk', totalScore);
            }
            alert('送信完了！あなたの選んだ本音の点数が、社長の画面（admin）へリアルタイムに同期されました！');
            document.getElementById('surveyPage').style.display = 'none';
            document.getElementById('menuPage').style.display = 'block';
        }

        window['execute' + 'Login'] = function(type) {
            if(type === 1) {
                var code = document.getElementById('groupInput').value;
                if(code === '1234') {
                    document.getElementById('menuPage').style.display = 'none';
                    document.getElementById('topPage').style.display = 'block';
                } else { alert('正しい番号（1234）を入れてね！'); }
            } else if(type === 2) {
                var pass = document.getElementById('passInput').value;
                if(pass === 'admin') {
                    var liveRisk = localStorage.getItem('lumina_live_risk') || '85';
                    document.getElementById('riskText').innerText = liveRisk;
                    document.getElementById('menuPage').style.display = 'none';
                    document.getElementById('resultPage').style.display = 'block';
                } else { alert('正しいパスワード（admin）を入れてね！'); }
            }
        };

        window.addEventListener('DOMContentLoaded', function() {
            var target = document.getElementById('surveyTarget');
            var html = '';
            html += `<div class="question-card"><span class="question-title">【属性①】あなたの性別を教えてください</span><select><option>完全匿名</option><option>男性</option><option>女性</option></select></div>`;
            html += `<div class="question-card"><span class="question-title">【属性②】あなたの年齢層を教えてください</span><select><option>20代</option><option>30代</option><option>40代</option></select></div>`;
