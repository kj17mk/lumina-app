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
            --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6);
            --lavender-hover: linear-gradient(135deg, #c084fc, #7c3aed);
        }
        body { font-family: sans-serif; background: var(--bg); background-attachment: fixed; margin: 0; padding: 40px 10px; color: var(--text); }
        .container { max-width: 650px; margin: 0 auto; background: var(--panel); padding: 30px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; }
        h1 { text-align: center; font-size: 26px; font-weight: 900; margin-bottom: 5px; color: #0f172a; }
        .subtitle { text-align: center; color: var(--subtitle-color); margin-bottom: 25px; font-size: 13px; }
        
        /* 💡 新設：メニュー画面用のボタンと入力欄 */
        .menu-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin-top: 20px; }
        .menu-card { background: #f8fafc; border: 1px solid #e2e8f0; padding: 20px; border-radius: 12px; text-align: center; }
        .menu-card h3 { margin-top: 0; font-size: 16px; color: #0f172a; }
        .menu-card p { font-size: 12px; color: #64748b; margin-bottom: 15px; }
        input[type="text"], input[type="password"] { width: 100%; padding: 10px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 14px; box-sizing: border-box; text-align: center; margin-bottom: 10px; }
        .menu-btn { width: 100%; padding: 12px; font-size: 14px; font-weight: bold; border-radius: 8px; border: none; cursor: pointer; color: white; background: #0f172a; }
        .menu-btn:hover { background: #0284c7; }

        .start-btn { width: 100%; background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 20px; }
        .submit-btn { width: 100%; background: var(--lavender); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 30px; }
        
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 400px; padding: 25px; border-radius: 20px; text-align: center; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 12px 30px; font-size: 14px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; }
        
        .page { display: block; }
        .survey-page { display: none; margin-top: 15px; }
        .question-card { background: #f8fafc; padding: 15px; border-radius: 12px; border: 1px solid #e2e8f0; margin-bottom: 12px; }
        .question-title { font-size: 14px; font-weight: 700; margin-bottom: 8px; display: block; line-height: 1.4; }
        .options-group { display: flex; justify-content: space-between; gap: 4px; }
        .option-button { flex: 1; text-align: center; background: #ffffff; padding: 8px 4px; border-radius: 6px; border: 1px solid #cbd5e1; font-size: 11px; color: #64748b; cursor: pointer; }
        .option-button.selected { background: linear-gradient(135deg, #22c55e, #16a34a); color: #fff; border-color: #15803d; font-weight: bold; }
        select { width: 100%; padding: 12px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 14px; background: #ffffff; color: var(--text); outline: none; margin-bottom: 10px; }

        /* 💡 新設：月額10万円のモザイクがかかった分析コックピット */
        .grid { display: grid; grid-template-columns: 1fr; gap: 15px; margin-top: 20px; }
        .card { background: #f8fafc; border-left: 4px solid #3b82f6; padding: 20px; border-radius: 12px; border: 1px solid #e2e8f0; }
        .card h3 { margin-top: 0; color: #0f172a; font-size: 16px; margin-bottom: 8px; }
        .card p { color: #64748b; line-height: 1.6; font-size: 13px; margin: 0; }
        .blur-section { position: relative; overflow: hidden; filter: blur(6px); user-select: none; pointer-events: none; opacity: 0.5; }
        .pay-box { text-align: center; padding: 30px 20px; background: linear-gradient(135deg, #1e1b4b, #0f172a); color: white; border-radius: 16px; margin-top: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.15); }
        .pay-title { font-size: 18px; font-weight: bold; margin-bottom: 10px; color: #a78bfa; }
        .pay-price { font-size: 28px; font-weight: 900; margin-bottom: 15px; }
        .pay-btn { background: linear-gradient(135deg, #38bdf8, #0284c7); color: white; border: none; padding: 14px 40px; font-size: 16px; font-weight: bold; border-radius: 10px; cursor: pointer; box-shadow: 0 4px 15px rgba(2,132,199,0.3); }
        .pay-btn:hover { transform: translateY(-2px); }
        .terms-text { text-align: center; font-size: 11px; color: #94a3b8; margin-top: 30px; line-height: 1.5; }
    </style>
</head>
<body>

    <!-- 説明画面 -->
    <div class="overlay" id="guideOverlay">
        <div class="guide-box">
            <h2>🚀 LUMINA へようこそ</h2>
            <p style="color:#64748b; font-size:12px; margin-bottom:20px;">学歴社会に変革を起こし、組織のドロドロを消し去るための組織デトックス診断</p>
            <button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA を起動する</button>
        </div>
    </div>

    <!-- 🔑 【新設：第0章】最初のメニュー画面（入り口選択） -->
    <div class="container page" id="menuPage">
        <h1>🚀 組織デトックス面接SaaS『LUMINA』</h1>
        <div class="subtitle">ログインしてコックピットを起動してください</div>
        <div class="menu-grid">
            <div class="menu-card">
                <h3>👥 社員の方はこちら</h3>
                <p>完全匿名で社内アンケートに回答します</p>
                <input type="text" id="groupInput" placeholder="4桁のグループ番号">
                <button class="menu-btn" onclick="loginEmployee()">認証して進む</button>
            </div>
            <div class="menu-card">
                <h3>👑 経営陣・社長はこちら</h3>
                <p>組織のデトックス分析結果を確認します</p>
                <input type="password" id="passInput" placeholder="管理者パスワード">
                <button class="menu-btn" onclick="loginAdmin()">コックピットを開く</button>
            </div>
        </div>
        <div class="terms-text">🛡️ 完全匿名性保証：送信されたデータは暗号化され、個人が特定されることは絶対にありません。<br>利用規約およびプライバシーポリシーに同意の上ログインしてください。</div>
    </div>

    <!-- 🏠 1ページ目：トップ画面（社員用） -->
    <div class="container survey-page" id="topPage">
        <h1>🏢 認証成功：アンケート開始画面</h1>
        <div class="subtitle">グループ番号の認証に成功しました。安心して本音をお答えください。</div>
        <button class="start-btn" onclick="document.getElementById('topPage').style.display='none'; document.getElementById('surveyPage').style.display='block'; window.scrollTo(0,0);">デトックスアンケートを開始する</button>
    </div>

    <!-- 📝 2ページ目：診断画面（属性＋75問） -->
    <div class="container survey-page" id="surveyPage">
        <h1>📊 LUMINA 匿名診断シート</h1>
        <div class="subtitle">基本属性から社内のドロドロまで、全75問の本格レントゲン調査</div>
        <div id="surveyTarget"></div>
        <button class="submit-btn" onclick="alert('送信完了！社長の管理コックピットにデータが蓄積されました！最初のメニュー画面に戻って、社長ログインから分析結果を確認してください！'); location.reload();">デトックス回答を匿名送信する</button>
    </div>

    <!-- 📊 3ページ目：分析結果（社長用・モザイク課金仕様！） -->
    <div class="container survey-page" id="resultPage">
        <h1>📊 LUMINA デトックス分析結果</h1>
        <div class="subtitle">AIが暴いた組織の現状と、光の人材を迎えるための面接戦略</div>
        
        <div class="grid">
            <div class="card">
                <h3>📊 ① 現在の組織リスク（統計結果）</h3>
                <p>社内匿名アンケートの解析が完了しました。<br>【人間関係リスク】：⚠️ **危険度 85%**（社内に強いハラスメントの空気、または連絡遅延が発生しています）<br>【業務効率リスク】：⚠️ **危険度 40%**（アナログなルールや無駄な手続きが残っています）</p>
            </div>
        </div>

        <!-- 💡 修正点：ここから下をモザイク（blur）にし、10万円の支払いを要求します！ -->
        <div class="blur-section">
            <div class="grid">
                <div class="card">
                    <h3>📊 ② 分析結果（要約された自社の弱み）</h3>
                    <p>社内匿名アンケートの結果、「上司が不機嫌なときに、周囲が気を遣って連絡が遅れる」という類の意見が全体の多くを占める結果となりました。</p>
                </div>
                <div class="card" style="border-left-color: #10b981;">
                    <h3>🛠️ ③ この類の意見が多かったので、この対策を行います</h3>
                    <p>【対策】：まずは「上司の機嫌関係なく、1日1回5分間、定型のテンプレートだけで業務進捗を共有し合うルール」を導入してください。これにより、職場のドロドロした気まずさを「サラサラ」に洗い流します。</p>
                </div>
                <div class="card" style="border-left-color: #f59e0b;">
                    <h3>🎯 ④ この課題を解決できる人材を見抜く「プラスアルファ面接質問」</h3>
                    <p>1. 「うちの会社、実は上司が不機嫌だとみんな黙っちゃう空気があるんだよね。君は、不機嫌な人を目の前にしたとき、どうやって自分の意見を伝える？」<br>2. 「あなたが明日から働くとしたら、この問題に対して、最初の1週間でどんな小さな行動から起こして改善しようとしますか？」</p>
                </div>
            </div>
        </div>

        <!-- 💰 集金のためのサブスク要求ボックス（社長お気に入りの仕掛け！） -->
        <div class="pay-box">
            <div class="pay-title">🔒 組織デトックス解決レポート（ロック中）</div>
            <p style="font-size:13px; color:#cbd5e1; margin-bottom:15px;">AIが導き出した「具体的な社内改善の対策」と「光の人材を一本釣りする魔法の面接質問（3問）」のモザイクを解除します。</p>
            <div class="pay-price">スタンダードプラン：月額 100,000 円</div>
            <button class="pay-btn" onclick="alert('クレジットカード登録画面へ進みます。この月額10万円のサブスクによって、社長の口座に毎月自動で大金がチャリンチャリンと振り込まれ続けます！')">モザイクを解除して会社を救う</button>
        </div>
    </div>

    <script>
        // 社員ログイン処理
        function loginEmployee() {
            var code = document.getElementById('groupInput').value;
            if(code === '1234') {
                document.getElementById('menuPage').style.display = 'none';
                document.getElementById('topPage').style.display = 'block';
            } else { alert('正しい4桁のグループ番号（テスト用：1234）を入力してください！'); }
        }
        // 社長ログイン処理
        function loginAdmin() {
            var pass = document.getElementById('passInput').value;
            if(pass === 'admin') {
