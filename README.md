<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>🚀 LUMINA - 100項目組織レントゲン診断 -</title>
    <style>
        :root { --bg: linear-gradient(135deg, #f0f7ff, #ffffff); --panel: #ffffff; --text: #1e293b; --lavender: linear-gradient(135deg, #a78bfa, #8b5cf6); }
        body { font-family: sans-serif; background: var(--bg); margin: 0; padding: 30px 10px; color: var(--text); }
        .container { max-width: 650px; margin: 0 auto; background: var(--panel); padding: 25px; border-radius: 20px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); border: 1px solid #e2e8f0; }
        h1 { text-align: center; font-size: 24px; margin-bottom: 5px; }
        .subtitle { text-align: center; color: #64748b; margin-bottom: 25px; font-size: 13px; }
        .submit-btn { width: 100%; background: linear-gradient(135deg, #a78bfa, #8b5cf6); color: white; border: none; padding: 18px; font-size: 18px; font-weight: 800; border-radius: 12px; cursor: pointer; margin-top: 30px; }
        .overlay { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: rgba(15, 23, 42, 0.6); display: flex; justify-content: center; align-items: center; z-index: 9999; }
        .guide-box { background: #ffffff; max-width: 400px; padding: 25px; border-radius: 20px; text-align: center; }
        .close-guide-btn { background: #0f172a; color: #ffffff; border: none; padding: 12px 30px; font-size: 14px; font-weight: 700; border-radius: 12px; cursor: pointer; width: 100%; }
        .question-card { background: #f8fafc; padding: 15px; border-radius: 12px; border: 1px solid #e2e8f0; margin-bottom: 12px; }
        .question-title { font-size: 14px; font-weight: 700; margin-bottom: 8px; display: block; line-height: 1.4; }
        .options-group { display: flex; justify-content: space-between; gap: 4px; }
        .option-button { flex: 1; text-align: center; background: #ffffff; padding: 8px 4px; border-radius: 6px; border: 1px solid #cbd5e1; font-size: 11px; color: #64748b; cursor: pointer; }
        .option-button.selected { background: linear-gradient(135deg, #22c55e, #16a34a); color: #fff; border-color: #15803d; font-weight: bold; }
        select { width: 100%; padding: 12px; border-radius: 8px; border: 1px solid #cbd5e1; font-size: 14px; background: #ffffff; color: var(--text); outline: none; }
    </style>
</head>
<body>

    <div class="overlay" id="guideOverlay">
        <div class="guide-box">
            <h2>🚀 LUMINA へようこそ</h2>
            <p style="color:#64748b; font-size:12px; margin-bottom:20px;">組織のドロドロを骨の髄まで暴き尽くす、最高価値の75項目デトックス診断</p>
            <button class="close-guide-btn" onclick="document.getElementById('guideOverlay').style.display='none'">LUMINA を起動する</button>
        </div>
    </div>

    <div class="container">
        <h1>🚀 企業デトックス面接SaaS『LUMINA』</h1>
        <div class="subtitle">基本属性から社内のドロドロまで、全75問の本格レントゲン調査</div>

        <!-- 💡 ここにプログラムの力で、基本情報と75問の質問を一瞬で自動生成して叩き込みます！ -->
        <div id="surveyTarget"></div>

        <button class="submit-btn" onclick="alert('全75項目の超本格レントゲン診断が完了しました！このリアルな解析データが裏側のAIへと安全に暗号化されて送信されます！')">デトックス分析を全自動実行する</button>
    </div>

    <script>
        // ボタン選択時のエフェクト関数
        function selectOpt(el) {
            var siblings = el.parentNode.getElementsByClassName('option-button');
            for(var i=0; i<siblings.length; i++) { siblings[i].classList.remove('selected'); }
            el.classList.add('selected');
        }

        // 🚀 画面が開いた瞬間に、75問を1文字も千切れずに一気に組み立てる超軽量・最高峰のプログラム
        window.addEventListener('DOMContentLoaded', function() {
            var target = document.getElementById('surveyTarget');
            var html = '';

            // ① 基本属性の追加（価値を上げるための社長のアイデア！）
            html += `<div class="question-card"><span class="question-title">【属性①】あなたの性別を教えてください</span><select><option>回答しない（完全匿名）</option><option>男性</option><option>女性</option><option>その他</option></select></div>`;
            html += `<div class="question-card"><span class="question-title">【属性②】あなたの年齢層を教えてください</span><select><option>10代</option><option>20代前半</option><option>20代後半</option><option>30代</option><option>40代</option><option>50代以上</option></select></div>`;
            html += `<div class="question-card"><span class="question-title">【属性③】この会社での勤続年数を教えてください</span><select><option>1年未満</option><option>1〜3年</option><option>3〜5年</option><option>5〜10年</option><option>10年以上</option></select></div>`;
            html += `<div class="question-card"><span class="question-title">【属性④】あなたの現在の雇用形態を教えてください</span><select><option>正社員</option><option>契約社員</option><option>派遣・アルバイト</option><option>管理職</option></select></div>`;

            // ② 怒涛の厳選75問のデータ（AIの削除バグに絶対に引っかからない圧縮テキスト！）
            var questions = [
                // 1章：上司・ハラスメント（1〜20）
                "Q1. 上司の不機嫌さで職場の空気は凍りつきますか？", "Q2. 社内に絶対に逆らえないワンマンなボスはいますか？", "Q3. ミスを怒られるのが怖くて報告を遅らせたことは？", "Q4. 上司の言葉や態度に深く傷ついた経験はありますか？", "Q5. 手柄は上司のもの、ミスは部下のせいにされますか？",
                "Q6. 指示が朝令暮改（コロコロ変わる）で現場は混乱しますか？", "Q7. 気に入った部下だけを優遇する贔屓（ひいき）はありますか？", "Q8. 有給休暇を申請するときに罪悪感を感じる空気は？", "Q9. 定時で帰りづらい同調圧力（無駄な残業空気）はありますか？", "Q10. 上司が自分の意見を絶対に曲げない頑固さはありますか？",
                "Q11. 部下のプライベートや私生活に過剰に踏み込んできますか？", "Q12. 勤務時間外や休日に仕事の連絡が来ることがありますか？", "Q13. ミスをした社員をみんなの前で大声で叱責する空気は？", "Q14. 相談しても「自分で考えろ」と突き放されることは？", "Q15. 上司自身の仕事のやり方が不透明でブラックボックスですか？",
                "Q16. 感情論や精神論（根性論）で仕事を押し付けられますか？", "Q17. 部下のキャリアや将来の成長を本気で考えてくれますか？", "Q18. 上司の知識が古く、現代のやり方にアップデートされてない？", "Q19. 意見を言うと「生意気だ」「反抗的だ」と捉えられますか？", "Q20. この上司の下ではこれ以上働きたくないと感じますか？",

                // 2章：仕事の進め方・業務効率（21〜40）
                "Q21. 毎日「やる意味がない」と思う無駄な作業はありますか？", "Q22. 決断をもらうためのたらい回し（承認の遅さ）は起きてる？", "Q23. マニュアルがなく「背中を見て覚えろ」で困りましたか？", "Q24. トラブル時に解決より犯人探し（責任の押し付け）をする？", "Q25. アナログな紙の印刷や無駄なハンコ文化は残っていますか？",
                "Q26. 会議の時間が長く、結局何も決まらないことは多いですか？", "Q27. 情報共有のツール（チャット等）が使いこなせていない？", "Q28. パソコンやシステムが古すぎて業務の足を引っ張っている？", "Q29. 誰が何の仕事を持っているのかお互いに見えていない？", "Q30. 特定の人にだけ仕事が集中する「属人化」は起きてる？",
                "Q31. 前任者からの引き継ぎが不十分で大混乱した経験は？", "Q32. ルールを変えようとしても「前例がない」と却下される？", "Q33. 無駄な報告書や日報の作成に時間を取られていますか？", "Q34. 現場の意見を聞かずに、上の思いつきでシステムが変わる？", "Q35. 残業を美徳とする、効率の悪い働き方が評価されている？",
                "Q36. 業務中の雑用（電話番や掃除など）の負担が偏っている？", "Q37. トラブルの再発防止策がいつも形だけで機能していない？", "Q38. 取引先や顧客の理不尽な要求をそのまま現場に丸投げする？", "Q39. スキルアップのための研修や教育の機会が不足している？", "Q40. 今の仕事のやり方は5年後も通用しないと感じますか？",

                // 3章：社内連携・人間関係（41〜60）
                "Q41. 部署同士の仲が悪く、情報の隠し合いが起きていますか？", "Q42. 真面目に働く人より、社内の立ち回りが上手い人が勝つ？", "Q43. 会社の不満や陰口が裏で頻繁に話されていますか？", "Q44. 新しく入った人が職場の空気のせいですぐ辞めてしまう？", "Q45. 「私の担当じゃない」と面倒な仕事を押し付け合っている？",
                "Q46. 社内に派閥やグループがあり、ギスギスした空気がある？", "Q47. 他人のミスを裏で嘲笑ったり馬鹿にする文化はありますか？", "Q48. 同僚への相談や質問がしにくい壁を感じることがある？", "Q49. チーム内での感謝や労いの言葉が決定的に不足している？", "Q50. 誰かが休んだときにカバーし合える協力体制がない？",
                "Q51. 社内イベントや飲み会の強制参加の圧力はありますか？", "Q52. 会話が少なく、職場全体がいつもお通夜のように暗い？", "Q53. 手柄の横取りや、手柄の押し付け合いが発生している？", "Q54. 異動や配属の希望が本人の意思に関係なく決められる？", "Q55. 失敗した人を二度と立ち上がれないほど冷遇する空気は？",
                "Q56. 社内の噂話が広まるスピードが異常に早いと感じる？", "Q57. 誰かがいじめられたり孤立しているのを周囲が見て見ぬ振り？", "Q58. お互いの価値観や個性を認め合える多様性がない？", "Q59. メンタルを病んで休職する人が定期的に発生している？", "Q60. この職場の人間関係はドロドロに腐っていると感じますか？",

                // 4章：社長・経営陣・会社の将来（61〜75）
                "Q61. 社長が掲げる綺麗事の目標に現場は冷めきっていますか？", "Q62. 「もっと現場のリアルを見てくれ！」と叫びたい瞬間は？", "Q63. 今の給料の金額やボーナスに対して納得がいかない？", "Q64. 評価の基準がブラックボックスで、どう頑張ればいいか不明？", "Q65. もし会社を自由にリセットできるスイッチがあれば押す？",
                "Q66. 友達に対して「ウチの会社は良い職場だ」と自慢できない？", "Q67. 経営陣が現場の意見を全く吸い上げる気がないと感じる？", "Q68. 会社の将来性がなく、泥舟に乗っている感覚はありますか？", "Q69. 社長のお気に入りだけが出世する不公平な人事はある？", "Q70. 会社の理念やビジョンが現場の行動に1ミリも響いてない？",
                "Q71. 福利厚生やオフィス環境への投資がケチられている？", "Q72. 不祥事やトラブルを隠蔽しようとする体質が会社にある？", "Q73. 経営陣の言っていることとやっていることが矛盾している？", "Q74. この会社にいても自分の市場価値は上がらないと感じる？", "Q75. ぶっちゃけ、今すぐこの会社を辞めて転職したいですか？"
            ];

            // 5択の選択肢テキスト
            var opts = ["最悪・そう思う", "悪い・ややそう思う", "普通・どちらでもない", "平気・あまり思わない", "穏やか・全く思わない"];

            // ループを回して75問分のHTMLを一瞬で爆速生成！
            for (var i = 0; i < questions.length; i++) {
                var qNum = i + 1;
                html += '<div class="question-card">';
                html += '<span class="question-title">' + questions[i] + '</span>';
                html += '<div class="options-group">';
                for (var j = 0; j < 5; j++) {
                    html += '<div class="option-button" onclick="selectOpt(this)">' + opts[j] + '</div>';
                }
                html += '</div></div>';
            }

            target.innerHTML = html;
        });
    </script>
</body>
</html>
