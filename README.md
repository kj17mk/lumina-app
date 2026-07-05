<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA</title>
    <style>
        :root { --bg: linear-gradient(135deg, #f8fafc, #ffffff); --panel: #ffffff; --text: #1e293b; }
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
        .submit-btn { width: 100%; background: linear-gradient(135deg, #a78bfa, #8b5cf6); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 30px; }
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
            for(var i=0; i<siblings.length; i++) { 
                siblings[i].classList.remove('selected'); 
            }
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
            var questions = [
                "Q1. 上司の不機嫌さで職場の空気は重くなりますか？", "Q2. 社内に強い影響力を持つワンマンな上司はいますか？", "Q3. ミスを指摘されるのが心配で報告が遅れたことは？", "Q4. 上司の対応に深く悩んだ経験はありますか？", "Q5. 成果の評価や責任の所在に理不尽さを感じますか？",
                "Q6. 指示がコロコロ変わって現場は混乱しますか？", "Q7. 特定の部下だけを優遇するような偏りはありますか？", "Q8. 有給休暇を申請するときに気まずさを感じる？", "Q9. 定時で帰りづらい同調圧力はありますか？", "Q10. 上司が自分の意見を絶対に曲げない頑固さは？",
                "Q11. 部下の私生活に過剰に踏み込んできますか？", "Q12. 勤務時間外や休日に仕事の連絡が来ますか？", "Q13. ミスをみんなの前で厳しく叱責する空気は？", "Q14. 相談しても突き放されることはありますか？", "Q15. 上司の仕事の進め方が不透明だと感じますか？",
                "Q16. 精神論や根性論で仕事を押し付けられますか？", "Q17. 部下の将来の成長を本気で考えてくれますか？", "Q18. 上司の知識が古く、やり方が更新されてない？", "Q19. 意見を言うと反抗的だと捉えられますか？", "Q20. この上司の下ではこれ以上働きたくないですか？",
                "Q21. 毎日「やる意味がない」と思う無駄な作業はある？", "Q22. 決断をもらうための手続きに時間がかかる？", "Q23. マニュアルがなく丁寧な指導がない状態で困った？", "Q24. トラブル時に解決より責任追及ばかりする空気は？", "Q25. アナログな印刷や無駄な手続きは残っていますか？",
                "Q26. 会議の時間が長く、何も決まらないことは多い？", "Q27. 情報共有のツールが使いこなせていない？", "Q28. パソコンやシステムが古すぎて業務の足を引っ張る？", "Q29. 誰が何の仕事を持っているのかお互いに見えない？", "Q30. 特定の人にだけ仕事が集中する偏りはありますか？",
                "Q31. 前任者からの引き継ぎが不十分で混乱した？", "Q32. ルールを変えようとしても前例がないと却下される？", "Q33. 無駄な報告書や日報の作成に時間を取られる？", "Q34. 現場の意見を聞かずにシステムが変わる？", "Q35. 残業を美徳とする効率の悪い働き方がある？",
                "Q36. 業務中の雑用の負担が一部に偏っている？", "Q37. トラブルの再発防止策が形だけで機能してない？", "Q38. 取引先の理不尽な要求を現場に丸投げする？", "Q39. スキルアップのための教育の機会が不足している？", "Q40. 今の仕事のやり方は5年後も通用しない？",
                "Q41. 部署同士の仲が悪く、情報の隠し合いがある？", "Q42. 真面目な人より、立ち回りが上手な人が勝つ？", "Q43. 会社の不満や陰口が裏で頻繁に話されている？", "Q44. 新入社員が職場の空気のせいですぐ辞めてしまう？", "Q45. 面倒な仕事を押し付け合っている空気はある？",
                "Q46. 社内に派閥があり、ギスギスした空気がある？", "Q47. 他人のミスを裏で悪く言う文化はありますか？", "Q48. 同僚への相談や質問がしにくい壁を感じる？", "Q49. チーム内での感謝や労いの言葉が不足している？", "Q50. 誰かが休んだときにカバーし合える体制がない？",
                "Q51. 社内イベントの強制参加の圧力はありますか？", "Q52. 会話が少なく、職場全体がいつも暗い？", "Q53. 手柄の横取りや責任の押し付け合いがある？", "Q54. 異動や配属の希望が本人の意思に関係なく決まる？", "Q55. 失敗した人を立ち上がれないほど冷遇する空気は？",
                "Q56. 社内の噂話が広まるスピードが異常に早い？", "Q57. 誰かが孤立しているのを周囲が見て見ぬ振り？", "Q58. お互いの価値観や個性を認め合える多様性がない？", "Q59. メンタルを崩して休職する人が定期的にいる？", "Q60. この職場の人間関係はよくないと感じますか？",
                "Q61. 社長が掲げる綺麗事の目標に現場は冷めてる？", "Q62. もっと現場のリアルを見てくれと叫びたい？", "Q63. 今の給料の金額やボーナスに対して納得がいかない？", "Q64. 評価の基準が不明確で、どう頑張ればいいか不明？", "Q65. もし会社を自由にリセットできるスイッチがあれば押す？",
                "Q66. 友達に対して「ウチの会社は良い職場だ」と自慢できない？", "Q67. 経営陣が現場の意見を吸い上げる気がないと感じる？", "Q68. 会社の将来性がなく、不安になる感覚はある？", "Q69. 社長のお気に入りだけが出世する人事はある？", "Q70. 会社の理念やビジョンが現場に1ミリも響いてない？",
                "Q71. 福利厚生やオフィス環境への投資が少ない？", "Q72. トラブルを隠蔽しようとする体質が会社にある？", "Q73. 経営陣の言っていることとやっていることが矛盾している？", "Q74. この会社にいても自分の市場価値は上がらない？", "Q75. ぶっちゃけ、今すぐこの会社を辞めて転職したいですか？"
            ];
            
            for (var i = 0; i < questions.length; i++) {
                html += '<div class="question-card">';
                html += '<span class="question-title">' + questions[i] + '</span>';
                html += '<div class="mbti-group">';
                html += '<span class="mbti-label" style="color:#0284c7; margin-right:5px;">同意</span>';
                html += '<button class="mbti-btn b-lg" onclick="selectMbti(this,5)"></button>';
                html += '<button class="mbti-btn b-md" onclick="selectMbti(this,4)"></button>';
                html += '<button class="mbti-btn b-sm" onclick="selectMbti(this,3)"></button>';
                html += '<button class="mbti-btn b-sm" onclick="selectMbti(this,2)"></button>';
                html += '<button class="mbti-btn b-md" onclick="selectMbti(this,1)"></button>';
                html += '<span class="mbti-label" style="color:#64748b; margin-left:5px;">反対</span>';
                html += '</div></div>';
            }
            target.innerHTML = html;
        });
    </script>
</body>
</html>
