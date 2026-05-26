import { useState, useEffect, useMemo } from "react";
import { LineChart, Line, BarChart, Bar, XAxis, YAxis, Tooltip, ResponsiveContainer, CartesianGrid, Cell } from "recharts";

const C = {
  bg:"#fdf8ff", s1:"#ffffff", s2:"#fef3f8", s3:"#f8f0ff",
  border:"#f0d9f7", border2:"#fce4ef",
  pink:"#e8417a", pinkL:"#ff6fa8", pinkBg:"#fff0f5",
  purple:"#8b35cc", purpleL:"#b06de0", purpleBg:"#f5eeff",
  orange:"#f07030", orangeL:"#ff9555", orangeBg:"#fff4ee",
  text:"#2d1040", sub:"#7a4d9a", muted:"#c09ad0",
  green:"#27a86a", greenBg:"#f0faf5",
  red:"#e03060", redBg:"#fff0f3",
  gold:"#d48800", goldBg:"#fffbee",
  shadow:"0 2px 16px rgba(180,100,220,0.10)",
  shadow2:"0 4px 24px rgba(180,100,220,0.15)",
};

const MASTER_KNOWLEDGE = {
  nekasegi:{
    summary:"Threads×有料記事販売。最短3日で収益化。フォロワー0から機能する。",
    roadmap:["①アカウントパワー：客目線バズ投稿でホーム表示を増やす","②欲求喚起投稿：理想の未来×手段×再現性の3点セット","③有益投稿：即効性ある情報を無償提供（欲求喚起5:有益1）","④CTA：見ることが読者の得になる形で誘導","⑤無料note：体験談+概要で売れる顧客に変える","⑥有料note成約：欲しくて仕方ない状態を作ってから誘導"],
    desireElements:["見た人があこがれる理想を実現している","それがあなたのアカウントから手に入る","難易度が高くない"],
    ctaTips:["してほしいアクション＝お客様の利益の図式を作る","見てくださいではなく見ることが得になる形に","無料noteの一部を見せて全部見たくなる状態を作る"],
    addLectures:["投稿に主語を入れる：投稿→アカウント→中の人への興味移行","売れている様子を見せる：人気感・バンドワゴン効果","差別化は中の人を出すこと：人格・信念・性格","小さなコミュニティ：双方向投稿→企画→小さな島","LINE/オプチャ：500フォロワーから。告知役割で使う"],
  },
  hookMethods:{
    osaru:{name:"おさる式",core:"知らないと損する情報緊急性型",pattern:"知らないと損→今すぐ確認→具体手順→CTA",examples:["知らないと損する話","今すぐ確認してほしいこと","9割の人が知らない○○","やってはいけない○○"]},
    nekasegi:{name:"寝稼ぎ式",core:"診断・分類・返信誘発型",pattern:"あなたはどのタイプ？→分類→私もそうだった→返信誘発",examples:["これ、当てはまる？","あなたはどのタイプ？①②③","ひとつでもあるなら…","番号だけ置いていって"]},
    hika:{name:"ヒカさん式",core:"人格＋数字＋読者の変化で信頼を積む型",patterns:["業界の常識ぶち壊し型：Threads攻略という低重要度テーマに囚われるな","実績スクショ＋コメント型：月100万達成のDMが来た","自分語り＋人間味型：昔は○○だったけど今は","キャラ・コミュニティ感型：仲間と一緒に走る感覚","戦略図型：全体像の地図を見せる"],transfers:["戦略図投稿：勝ちパターンの地図を見せる","読者の変化投稿：noteを読んで動き出した声","逆張り型：損するのは準備してない人より順番を間違えた人"]},
  },
  aiTechniques:{
    babySegment:{name:"ベイビーセグメント",howto:"AIに競合が拾ってない無名セグメントを20個+月収・課金心理まで出させる",benefit:"競合ゼロのセグメントを最初に取れる"},
    painStacking:{name:"Pain Stacking",howto:"AIにペルソナの悩みを5層に積んで1商品で同時解決する構成を出させる",benefit:"商品の刺さり方が3倍変わる"},
    reverseFunnel:{name:"Reverse Funnel",howto:"最終商品から逆算して必要な信頼・気づき・前提を洗い出し投稿テーマ30個を出させる",benefit:"投稿1個1個が販売の伏線になる"},
    preLaunchEcho:{name:"Pre-Launch Echo",howto:"商品が存在しない状態でコンセプトを投稿して反応を見る",benefit:"需要確定してから作るからリリース直後から売れる"},
    ghostReviewer:{name:"Ghost Reviewer",howto:"4人の視点（3年後の自分・競合・買わなかった客・購入者）でレビューさせる",benefit:"1人で4方向の本音フィードバックが手に入る"},
  },
  postLayers:{
    rule:"伸びる投稿は認知、保存される投稿は信頼、売れる投稿は導線。1投稿に全部詰めない。",
    recognition:"認知投稿：バズ・拡散・フォロワー獲得。共感、驚き、あるある、損失回避",
    trust:"信頼投稿：体験談・チェックリスト・判断基準・Before/After。保存される",
    funnel:"導線投稿：プロフィール・無料note・有料note・マガジンへ。売れる",
  },
  reflectionFramework:{
    evaluationAxes:["1行目の強さ（スクロールを止めたか）","読者が私のことだと思えたか","共感だけで終わらず次の行動があるか","CTA（誘導先）は自然か","売り込み感が出すぎていないか","noteやプロフィールに進む理由が積み上がったか","バズ投稿の直後に橋渡し投稿があるか"],
    winLosePattern:{win:"過去告白＋時間軸具体型（7年前の私は、金曜の夜が嫌だった）が最強",lose:"ロジック質問型（○○って何からすればいいの？）は今の段階では弱い",golden:"曜日・時間帯・生活シーン＋マイナス感情の3点セット"},
    postTypes:["共感投稿（読者の気持ちを代弁）","欲求喚起投稿（理想の未来をイメージさせる）","有益投稿（保存される実務情報）","診断・返信誘発型","知らないと損する型（情報緊急性）","ストーリー投稿（体験談・Before/After）","導線投稿（note・プロフィールへ）","レビュー投稿（売れた様子・読者の変化）"],
  },
  fukuStyle:{
    coreMessage:"今すぐ離婚を決めなくていい。でも、自分と子どもを守る準備だけは、今日から始めていい。",
    winningPatterns:["共感で広げる→傾聴で関係を作る→失敗談と実用情報でnoteへ橋渡し","過去の私＋曜日/時間＋負の感情","読者の罪悪感を外す→準備という希望→note/プロフィールへ","伸びた投稿の翌日に橋渡し投稿（直後に導線を置く）","傾聴投稿では売らない。翌日以降のリプ欄CTA"],
    ctaExamples:["必要な人だけ、プロフィールのnoteに置いてます","必要であれば見てみてください","今すぐ離婚を決めなくていい。でも準備の順番だけ見ておいてほしい"],
    avoid:["共感だけで終わらせない","伸びた投稿にCTAを入れないのが一番もったいない","深夜23時以降の投稿は初速が出にくい","画像ゼロの1日は作らない"],
  },
};

const EXTENDED_KNOWLEDGE = {

  fanPrinciples: {
    summary:"ファン化とは『情報』ではなく『人』で選ばれている状態。テクニックではなく在り方の問題。",
    sixPrinciples:[
      {id:1,name:"仲間ポジション",core:"先生ポジションではなく横に並んで走る。上から教えるより巻き込む。尊敬は距離を生むが、応援は距離を縮める。",action:"教えるではなく共有する言い方に変える。弱さを隠さない。読者を参加者にする質問を入れる。"},
      {id:2,name:"属人性",core:"情報は誰でも出せる。でも『あなた』は一人しかいない。立場・過程・感情・価値観・日常の5要素が属人性を構成する。",action:"投稿の最初の1〜2文に自分にしか書けない要素を入れる。自分の名前を別の人に変えても成立する投稿は属人性ゼロ。"},
      {id:3,name:"途中を見せる",core:"完成品は消費され、途中の物語は伴走される。チャレンジ宣言→進捗報告→うまくいかなかった日も投稿。投稿の最後に次の一手を入れる。",action:"週1回進捗報告。達成できなくても途中経過を出す。"},
      {id:4,name:"信用残高",core:"売上は信用の副産物。毎日の存在感・1対1のやりとり・仲間を巻き込む攻めの信用構築。一定ラインを超えたときまとめて返ってくる。",action:"毎日顔を出す。約束を守る。無料で価値を出し切る。巻き込みで攻めの信用構築。"},
      {id:5,name:"救済",core:"正論でも励ましでも現状肯定でもない。今の行動の先にある具体的な未来を見せること。今を否定せず、今に留まらせない。",action:"ビフォーアフター接続型・1歩の価値翻訳型・具体的3ステップ型の投稿を使い分ける。"},
      {id:6,name:"止まらない",core:"完成はピーク、未完成は未来。売れ続ける人の共通点：常に次のワクワクを持つ・圧倒的安心感・現在地を隠さない。巻き込んだ仲間の存在が止まらない力になる。",action:"月1回進化予告。週末に振り返り投稿。7日間チャレンジを繰り返す。"},
    ],
    brandCore:"煽らない・責めない・盛らない。一貫性があるブランドはファンが惚れる。",
    fanDefinition:"ファンは『作る』ものではなく『なっていただく』もの。こちらの在り方次第で引き寄せられる。",
  },

  influenceStrategy: {
    summary:"フォロワー数ゲームから降りて、ファン化とポジション取りで生き残る。",
    weakerStrategy:{
      position:"弱者＝0→1層の代弁者。大手には見えない現場の目線を持つ強みがある。",
      triangle:"大手↔自分↔フォロワー候補の三角形を作る。大手の翻訳者・共闘者・ちょっと先を歩く先輩。",
      targetBig:"推し大手3人を選ぶ。リプ返信率がそこそこある・リーダータイプ・フォロワーの声を紹介する人。",
      selectRule:"Q1:いなくなったら寂しい? Q2:伸びたら自分のことのように嬉しい? Q3:一緒に仕事している自分を想像できる?",
    },
    replyTypes:[
      {name:"要約＋自分事化リプ",pattern:"大手投稿を1行で要約→自分の状況に当てはめる→今日からやってみます",benefit:"ちゃんと読んだ人として印象が残る"},
      {name:"補足情報リプ（0→1層の翻訳）",pattern:"完全同意→初心者がつまずくポイントを補足→ミニTipsを1つ添える",benefit:"翻訳者ポジションを確立できる"},
      {name:"即実践＋感謝リプ（最強カード）",pattern:"どの投稿を見て何をやったか→結果の変化を数字/感情で→感謝",benefit:"共闘者として認識される。実績・口コミとして使ってもらえる"},
    ],
    distanceRules:[
      "毎日絡まない。リプ1日1通・引用週2〜3本まで",
      "DMはこちらからは基本送らない",
      "ネタにしないラインを決める（DM内容・削除した投稿等）",
      "月1回デトックス週：大手の名前を出さずに自分だけで投稿する",
    ],
    profileStrategy:{
      gapMethod:"見た目ビジネスガチ勢→中身はカカロット系凡人というギャップを仕込む",
      structure:["1行目：読者の口癖を代弁して弱い自分側に立つ","2行目：キャラで印象を崩す（カカロット系ママ等）","3〜4行目：弱者スタートなのにちゃんと結果も出している","5行目：合言葉で部活感を出す","6行目：行き先を1つだけ示す固定ポストへの誘導"],
      principle:"プロフは自己紹介ではなく、一緒に目指す世界への招待状",
    },
  },

  noteTimingSteps: {
    summary:"noteが売れない理由の9割は内容ではなくタイミング。読者の温度と出し方が揃っていないから。",
    coreInsight:"『読者がすでにお腹が空いている状態でちょうどカレーを出す』設計をする。",
    badPatterns:[
      {name:"ノルマ型",symptom:"毎月〇本出すノルマで焦りが文章に出る",fix:"本数より1本のタイミング精度に全振り"},
      {name:"バズ依存型",symptom:"バズった勢いでいきなりnoteを出す→売れない",fix:"バズはあくまで認知の入口。連続投稿で温度を確認してから出す"},
      {name:"準備過剰型",symptom:"完璧になってから出そうとして誰も待っていない",fix:"宣言を先にして強制的に完成に向かう。完了は完璧に勝る"},
    ],
    fiveSteps:[
      {step:1,name:"種まき期",action:"Threadsでいつも通り発信する。バズ狙いではなく○○といえばこのテーマという記憶の積み上げ。"},
      {step:2,name:"需要発見",action:"これ私・noteで読みたいが来た投稿に★をつける。いいね数ではなくプロフ遷移・コメントの深さで判断。"},
      {step:3,name:"温度上げ",action:"★テーマを2〜3日連続でThreadsに投稿。切り口を変えながら。同じ人から連続リアクションが来たら需要が育ったサイン。"},
      {step:4,name:"宣言",action:"このテーマnoteにまとめますね と1行だけ投稿。読者の頭に空き枠ができ、購入理由が生まれ、自分も書き切れる。"},
      {step:5,name:"執筆・公開",action:"ここで初めてnoteを書く。読者が半分買う気で来る状態で出す。宣言から3〜7日以内が最適。"},
    ],
    finalCheck:[
      "Threadsで『これ私』が来た投稿を起点にしているか",
      "このテーマもっと深く知りたいという声が手元にあるか",
      "予告を1回しているか",
    ],
    kpiToWatch:["エンゲージメント率（2%以上→★候補）","プロフ遷移率（0.5%以上→需要あり）","noteクリック率（3%以上→導線機能中）"],
  },

  noteWritingFormula: {
    corePrinciple:"noteで稼ぐのは才能ではなくやり方。読まれる構造を知っているかどうかの違い。",
    themeSelection:{
      criteria:["悩んでいる人が多い","あなたが体験している","物語として伝えられる"],
      strongThemes:["お金（稼ぎ方・節約・投資）","仕事（転職・フリーランス・副業）","人間関係","メンタルヘルス","失敗談（共感が最も高い）","コンプレックス克服"],
    },
    titleFormula:{
      elements:["数字（具体性）","感情（絶望・衝撃・救われた）","ギャップ（常識とのズレ・意外性）"],
      examples:["20年悩んだ生きづらさが一瞬で軽くなった『たった一つの』理由","30歳まで貯金ゼロだった僕が最初にやった『意外な』こと"],
    },
    introFormula:["問題提起（こんな悩みありませんか）","共感（私もそうでした）","転換点（あることに気づいてから）","読者メリット（この記事で解決します）"],
    storyStructure:["出発（日常の描写）","問題（トラブル・悩み）","葛藤（うまくいかない）","どん底（最大のピンチ）","気づき（解決の糸口）","変化（行動・結果）","学び","読者へのメッセージ"],
    pricingStrategy:{
      starter:"300〜980円：失敗しても痛くない。ランチ代より安い比較で訴求",
      middle:"1,500〜2,980円：書籍超えの法則。再現性のあるツール付きで差別化",
      escalator:"最初安く→売れ行きで値上げ→最終定価という段階的値上げ戦略",
      psychological:"末尾80円（980・1980・2980）がお得感を生む",
    },
    promotionFlow:{
      sns:"SNSで続きが気になる寸止め投稿→要約図解型→感情ストーリー型でnoteへ",
      fixedPost:"固定ポストに最高傑作noteを置いて集客の自動ドアを作る",
      timing:"金曜夜〜日曜午前が最も売れやすい。リリース3〜5日前に予告投稿",
    },
    assetArticlePatterns:[
      "入門ガイド型：初心者が永遠に生まれ続けるテーマ（時間が経っても需要がある）",
      "メンタル処方箋型：人間の本能に訴える普遍的な悩みへの解決策",
      "実体験レビュー型：公式には載っていない本音のメリット・デメリット",
    ],
  },

  actionPrompts: {
    analysisPrompt:`あなたは、SNSマーケティング、個人ビジネス設計、商品設計、集客導線、購買心理、行動心理、実行計画づくりに精通した戦略コンサルタントです。
分析して現実を変えるための行動に落とし込んでください。

【私の目標】
収益目標：[月100万円]
媒体：[Threads × note]
商品：[dododo ChatGPT・有料note・ロードマップ教材]
ターゲット：[副業したいAI初心者]
ポジション：[AI活用を感情的に欲しくなる商品に変換できる人]
悩み：[投稿は伸びるがnoteとの導線が弱い]

【分析対象】（ここにデータを貼る）

必ず以下を出す：現状詰まりポイント / ボトルネック1〜3個 / やめること・直すこと・作ること / 7日間プラン`,

    weeklyReviewPrompt:`今週のThreads運用を振り返ってください。

前提：目標月100万・本命導線はプロフィールnote・かおりスタイルで人間味MAX・数字は厳しめ

期間：[日付]
やったこと：[投稿内容・数字]
伸びた投稿：[内容]
弱かった投稿：[内容]
迷い：[悩んでいること]

出してほしい：1.総合評価★ 2.伸びた/伸びなかった理由 3.フック診断 4.CTA評価 5.note導線評価 6.次の24時間でやること3つ 7.次の投稿全文 8.今日の学びを一言で`,

    executionPrompt:`分析結果をもとに実行計画を作ってください。
優しい総論禁止。行動・期限・成果物・完了条件・検証数字まで具体化。
やめること / 直すこと / 作ること / 7日間プラン / 30日ロードマップ / 心理ブロック対策まで出す。`,
  },

  kaoriRealData: {
    realResults:{
      followers:"SNS本格運用5ヶ月でThreadsフォロワー5,400人突破→その後1万人達成",
      revenue:"note総売上150万円突破・最高月収105万円",
      method:"広告費ゼロ・リスティングゼロ・専門知識なし・ライティングスキルなし",
      startingPoint:"SNSが怖くて6ヶ月間見る専→投稿ボタンを押す手が震えるところから",
    },
    noteTimingResult:"月2万の壁→1週間で約20万円を達成。5ステップのタイミング設計で変わった",
    vibrationAnalysis:"振り返りを仕組みにしたら2週間で3,000人増えて1万人達成",
    positioningKey:"dododo（やる×やる×やる）のdo精神・カカロット系ママ・継続を最強の武器にする",
    contentMix:"遊び・制作過程 / 失敗談・苦労話 / 実績・数字 / ノウハウ / 診断 / 世界観・価値観を使い分ける",
    lessonFromInfluencer:"大手（okirumamaさん）にフォローしてもらえたのは：テーマの一貫性・IDのにおい合わせ・いいねと再投稿での静かな共闘、この3つの積み重け",
  },
};

const FUKU_KNOWLEDGE = {
  profile:{
    name:"ふく",
    accountId:"fuku.2025_hpgd",
    displayName:"ふく｜離婚前に損したくないママが動ける場所",
    bio:"モラハラ・不倫を経験し、証拠収集をしながら調停離婚した三姉妹の母。親権・養育費・面会交流・財産分与・年金分割まで調停で実際に話し合った経験あり。弁護士ではなく、同じように悩むママへ『損しないための準備の順番』を届ける立場。",
    background:"モラハラ・不倫被害→証拠収集→調停離婚→三姉妹の母として経済的自立を目指す実体験の持ち主",
  },
  target:{
    primary:"モラハラ被害中で逃げ出せない・動けないでいるママ",
    pain:["モラハラだと認識できていない","証拠の集め方がわからない","弁護士費用が怖い","離婚後の生活が不安","子どもへの影響が心配","親権を取れるか不安","お金のことが全然わからない","一人で動くのが怖い"],
    mindset:"まず準備ならできそう、と思える小さな一歩を踏み出させる",
    demographics:"子持ちの主婦・ママ層、20〜40代",
  },
  position:{
    uniqueness:"弁護士ではなく『同じ経験をしたママ』として、実体験ベースで準備の順番を伝えられる唯一の立場",
    core:"損しないための準備の順番を届ける",
    NOT:"法律の専門家・弁護士・完璧な成功者の話ではない",
    strength:"親権・養育費・面会交流・財産分与・年金分割まで調停で実際に経験している一次情報の厚さ",
  },
  products:{
    main:"有料note（販売中）",
    lineup:["調停離婚の準備note","証拠収集ガイド","モラハラ認定チェックリスト","財産分与・養育費の計算ガイド","マガジン（シリーズ化）"],
    funnel:"Threads発信→プロフィール→固定note→有料noteへの自然な導線",
    priceRange:"500〜3,980円（note単体）",
  },
  goals:{
    shortTerm:"Threadsからnote・マガジンへ自然につながる導線を確立",
    revenue:["まずnote・マガジンで月10万円","次に月30万円","最終的に月100万円"],
    content:"離婚やモラハラで動けずにいるママが『まず準備ならできそう』と思える投稿を育てる",
  },
  winningPatterns:{
    bestHooks:["モラハラチェックリスト系（診断・共感型）","実体験暴露系（私も同じだった）","準備できること具体的提示（今日からできる）","弁護士費用なしでできたこと"],
    resonanceTriggers:["『これってモラハラ？』の疑問に答える","証拠の集め方を具体的に","子どもへの影響を正直に","一人でできる準備ステップ"],
    ctaStyle:"売り込みではなく『準備の後押し』スタイル。プロフやnoteへの誘導は自然に。",
    avoidWords:["すぐ離婚して","弁護士に頼め","あなたは大丈夫"],
  },
  noteBridge:{
    trigger:"投稿で『準備の入口』を見せてnoteで『準備の全体像』を渡す",
    freeNote:"無料部分でモラハラの具体例・チェックリストの一部を見せる",
    paidNote:"有料部分で準備の順番・テンプレート・実際の調停体験を渡す",
    warmingUp:"2〜3日連続で同じテーマ（例：証拠収集）を違う切り口で投稿してから宣言",
  },
  avoid:{
    topics:["煽り系（早く逃げて・こんな夫最悪）","過度なドラマ化","弁護士の専門領域に踏み込む"],
    style:["上から目線","完璧な成功者感","読者を責める表現"],
    patterns:["反応ゼロのタイミングでいきなりnote告知","ノルマ的な投稿","バズったからすぐnote出す"],
  },
};

const NL = "\n";
const HOOK_TYPES = ["共感型","数字型","逆説型","ストーリー型","質問型","情報緊急型","診断型","遊び・制作過程","その他"];
const POST_ROLES = ["認知","共感","信頼","導線","販売","レビュー","制作過程","世界観","その他"];
const READER_PSYCHES = ["AIわからない","noteが売れない","ネタない","副業したい","かおちゃんみたいになりたい","作業時間減らしたい","今すぐ知りたい","その他"];
const DAYS = ["日","月","火","水","木","金","土"];
const CSV_COLS = ["text","date","time","likes","replies","reposts","views","fc","noteClicks","noteSales","hookType","role","readerPsyche"];
const THREADS_SCOPES = ["threads_basic","threads_content_publish","threads_manage_insights","threads_read_replies"];

const SAMPLE_POSTS = [
  {id:"sp1",text:"ChatGPTに自分の世界観を学習させて、カルーセルを10秒で作る方法。知らないと損すぎる。",date:"2026-05-01",time:"12:00",likes:523,replies:89,reposts:145,views:32000,fc:67,noteClicks:56,noteSales:3,hookType:"情報緊急型",role:"信頼",readerPsyche:"AIわからない"},
  {id:"sp2",text:"2ヶ月で売上500万円になった。でも正直、最初の3ヶ月は1円も稼げなかった。",date:"2026-05-03",time:"21:00",likes:789,replies:167,reposts:234,views:48000,fc:112,noteClicks:89,noteSales:5,hookType:"ストーリー型",role:"共感",readerPsyche:"かおちゃんみたいになりたい"},
  {id:"sp3",text:"AIで遊んでるだけで月50万になった人を3人見た。共通点はたった1つだった。",date:"2026-05-05",time:"19:00",likes:456,replies:78,reposts:189,views:28000,fc:89,noteClicks:45,noteSales:4,hookType:"逆説型",role:"導線",readerPsyche:"副業したい"},
  {id:"sp4",text:"dododo ChatGPT、また10部売れた。ありがとうございます。週末に追記します。",date:"2026-05-08",time:"22:00",likes:234,replies:34,reposts:67,views:12000,fc:23,noteClicks:78,noteSales:7,hookType:"ストーリー型",role:"レビュー",readerPsyche:"今すぐ知りたい"},
  {id:"sp5",text:"これ、当てはまる？①noteを書いているが全然売れない②AIに興味はあるが何から始めれば③作業時間が多いのに収益が少ない。ひとつでもあるなら、やり方の問題かも。",date:"2026-05-10",time:"12:00",likes:678,replies:234,reposts:156,views:42000,fc:134,noteClicks:67,noteSales:2,hookType:"診断型",role:"認知",readerPsyche:"noteが売れない"},
  {id:"sp6",text:"ChatGPTで自分のアイコンを作ってみた。5分で完成。お金もかからない。AIって面白い。",date:"2026-05-12",time:"18:00",likes:1234,replies:289,reposts:445,views:78000,fc:267,noteClicks:12,noteSales:0,hookType:"遊び・制作過程",role:"認知",readerPsyche:"AIわからない"},
  {id:"sp7",text:"売れるnoteと売れないnoteの違いは、文章力じゃなくて導線。9割の人が順番を間違えてる。",date:"2026-05-15",time:"12:00",likes:567,replies:123,reposts:234,views:35000,fc:89,noteClicks:89,noteSales:6,hookType:"逆説型",role:"信頼",readerPsyche:"noteが売れない"},
  {id:"sp8",text:"毎日投稿してる。疲れた日も、ネタない日も、バズらない日も。でも続けると何かが変わる。",date:"2026-05-18",time:"22:00",likes:890,replies:178,reposts:123,views:45000,fc:156,noteClicks:23,noteSales:1,hookType:"共感型",role:"世界観",readerPsyche:"かおちゃんみたいになりたい"},
];

function toNum(v){const n=Number(v);return Number.isFinite(n)?n:0;}
function clamp(v,mn,mx){return Math.max(mn,Math.min(mx,v));}
function makeId(){return Math.random().toString(36).slice(2)+Date.now().toString(36);}

function eg(p){
  const v=toNum(p.views);
  if(v<=0)return 0;
  return +((toNum(p.likes)+toNum(p.replies)*3+toNum(p.reposts)*2)/v*100).toFixed(2);
}
function clickRate(p){
  const v=toNum(p.views);
  if(v<=0)return 0;
  return +((toNum(p.noteClicks)/v)*100).toFixed(2);
}
function salesRate(p){
  const c=toNum(p.noteClicks);
  if(c<=0)return 0;
  return +((toNum(p.noteSales)/c)*100).toFixed(2);
}
function profileScore(p){
  const t=String(p.text||"");
  let s=0;
  ["AI","ChatGPT","note","副業","稼","売","do精神","かわいい","世界観","初心者","発信"].forEach(w=>{if(t.includes(w))s+=5;});
  if(/プロフィール|note|まとめ|詳しくは|リンク/.test(t))s+=15;
  if(/dododo|Brain|カルーセル|分析ツール/.test(t))s+=12;
  if(/失敗|葛藤|しんどかった|正直/.test(t))s+=8;
  if(/やってみた|とりあえず|do精神/.test(t))s+=8;
  return clamp(s,0,100);
}
function funnelScore(p){
  let s=0;
  const e=eg(p),cr=clickRate(p),sr=salesRate(p);
  if(e>=2)s+=18;else if(e>=1)s+=12;else if(e>=0.5)s+=7;
  if(cr>=0.12)s+=22;else if(cr>=0.06)s+=15;else if(cr>0)s+=8;
  if(sr>=5)s+=25;else if(sr>=2)s+=16;else if(sr>0)s+=9;
  if(["導線","販売","信頼","レビュー"].includes(p.role))s+=10;
  if(/プロフィール|note|まとめ|詳しくは/.test(String(p.text||"")))s+=10;
  s+=Math.round(profileScore(p)*0.15);
  return clamp(s,0,100);
}

function postDT(p){const d=new Date(`${p.date||"1970-01-01"}T${p.time||"00:00"}:00`);return isNaN(d)?new Date(0):d;}
function daysBetween(a,b){return(postDT(b)-postDT(a))/(1000*60*60*24);}

function autoClassify(text){
  const t=String(text||"");
  let hookType="共感型",role="共感",readerPsyche="その他";
  if(/\d|[0-9]|つ|ステップ|項目|個|割/.test(t))hookType="数字型";
  if(/知らないと損|損する|9割|絶対|今すぐ|注意|やってはいけない/.test(t))hookType="情報緊急型";
  if(/これ.当てはまる|あなたはどれ|診断|チェック|ひとつでも/.test(t))hookType="診断型";
  if(/じゃなくて|実は|本当は|一番大事|よりも|逆に/.test(t))hookType="逆説型";
  if(/私|あの日|昨日|また|売れた|ありがとう|しんどかった/.test(t))hookType="ストーリー型";
  if(/やってみた|作ってみた|試してみた|ChatGPT|AI.*画像|カルーセル/.test(t))hookType="遊び・制作過程";
  if(/\?|？|どう思う|わかる|教えて/.test(t))hookType="質問型";
  if(/プロフィール|note|まとめ|リンク|詳しくは|dododo|Brain/.test(t))role="導線";
  else if(/売れ|購入|ありがとう|部|レビュー|追記/.test(t))role="レビュー";
  else if(/作って|制作|追加|準備中|近日|週末に/.test(t))role="制作過程";
  else if(/方法|手順|やり方|ステップ|設定|使い方/.test(t))role="信頼";
  else if(/世界観|do精神|続け|毎日|疲れ/.test(t))role="世界観";
  if(/AI|ChatGPT|Claude|Gemini/.test(t))readerPsyche="AIわからない";
  if(/note|売れ|売上/.test(t))readerPsyche="noteが売れない";
  if(/副業|稼ぐ|収益|収入/.test(t))readerPsyche="副業したい";
  if(/今すぐ|知らないと損|緊急/.test(t))readerPsyche="今すぐ知りたい";
  if(/ネタ|アイデア|何を書/.test(t))readerPsyche="ネタない";
  return{hookType,role,readerPsyche};
}

function normalize(p){
  const auto=autoClassify(p.text);
  return{
    id:p.id||makeId(),
    text:String(p.text||"").trim(),
    date:p.date||new Date().toISOString().slice(0,10),
    time:p.time||"21:00",
    likes:toNum(p.likes),replies:toNum(p.replies),reposts:toNum(p.reposts),views:toNum(p.views),
    fc:toNum(p.fc),noteClicks:toNum(p.noteClicks),noteSales:toNum(p.noteSales),
    hookType:p.hookType||auto.hookType,
    role:p.role||auto.role,
    readerPsyche:p.readerPsyche||auto.readerPsyche,
  };
}

function parseCsvLine(line){
  const res=[];let cur="",inQ=false;
  for(let i=0;i<line.length;i++){
    const c=line[i],n=line[i+1];
    if(c==='"'&&inQ&&n==='"'){cur+='"';i++;}
    else if(c==='"'){inQ=!inQ;}
    else if(c===','&&!inQ){res.push(cur.trim());cur="";}
    else cur+=c;
  }
  res.push(cur.trim());return res;
}
function parseCsv(text){
  const lines=String(text||"").split(/\r?\n/).filter(l=>l.trim());
  if(lines.length<2)return[];
  const headers=parseCsvLine(lines[0]).map(h=>h.trim());
  return lines.slice(1).map(line=>{
    const vals=parseCsvLine(line);
    const obj={};headers.forEach((h,i)=>{obj[h]=vals[i]??""});
    return normalize(obj);
  }).filter(p=>p.text);
}
function csvEsc(v){const s=String(v??"");return/[",\n]/.test(s)?`"${s.replace(/"/g,'""')}"`:`${s}`;}
function toCsv(posts){return[CSV_COLS.join(","),...posts.map(p=>CSV_COLS.map(k=>csvEsc(p[k])).join(","))].join(NL);}

function getRoleCounts(posts){
  const c={};POST_ROLES.forEach(r=>c[r]=0);
  posts.forEach(p=>c[p.role]=(c[p.role]||0)+1);return c;
}

function recommendNext(posts){
  if(!posts.length)return{role:"共感",hook:"ストーリー型",psyche:"かおちゃんみたいになりたい",reason:"まずdo精神・失敗談・自己開示から始めて人間性を見せましょう。",theme:"AIを始めたきっかけの話"};
  const counts=getRoleCounts(posts);
  const totalSales=posts.reduce((s,p)=>s+toNum(p.noteSales),0);
  const recent=[...posts].sort((a,b)=>postDT(b)-postDT(a)).slice(0,5);
  const recentRoles=getRoleCounts(recent);
  const best=[...posts].sort((a,b)=>funnelScore(b)-funnelScore(a))[0];
  if((counts["共感"]||0)>=posts.length*0.45&&(counts["信頼"]||0)<posts.length*0.25)
    return{role:"信頼",hook:"数字型",psyche:best?.readerPsyche||"AIわからない",reason:"共感が多め。保存される実務投稿（手順・ノウハウ）を挟むと、note購入前の納得が作れます。",theme:"ChatGPTで発信素材を作る5ステップ"};
  if((counts["導線"]||0)<Math.max(1,Math.floor(posts.length*0.18)))
    return{role:"導線",hook:"ストーリー型",psyche:best?.readerPsyche||"副業したい",reason:"導線投稿が少なめ。売り込まず脈絡を作り、プロフィール/noteへの橋を置くタイミングです。",theme:"最近同じ質問が多いのでまとめました"};
  if(totalSales>0&&(recentRoles["レビュー"]||0)===0)
    return{role:"レビュー",hook:"ストーリー型",psyche:"今すぐ知りたい",reason:"noteが売れています。売れた事実・感謝・追記予告を出すと人気感と安心感が積み上がります。",theme:"dododo ChatGPT、また〇部売れました"};
  return{role:"診断",hook:"診断型",psyche:best?.readerPsyche||"noteが売れない",reason:"返信・自己開示を生む診断型を出す時期。読者に『これ私だ』と思わせてから導線へつなげます。",theme:"これ当てはまる？AI活用で稼げない人の共通点"};
}

function analyzeSalesWindows(posts){
  const sorted=[...posts].sort((a,b)=>postDT(a)-postDT(b));
  return sorted.filter(p=>toNum(p.noteSales)>0).map(salePost=>{
    const before=sorted.filter(p=>p.id!==salePost.id&&daysBetween(p,salePost)>=0&&daysBetween(p,salePost)<=3);
    const after=sorted.filter(p=>p.id!==salePost.id&&daysBetween(salePost,p)>=0&&daysBetween(salePost,p)<=1.5);
    const bRoles=getRoleCounts(before);
    const domRole=Object.entries(bRoles).sort((a,b)=>b[1]-a[1])[0]?.[0]||"不明";
    const bScore=before.length?Math.round(before.reduce((s,p)=>s+funnelScore(p),0)/before.length):0;
    return{salePost,before,after,insight:before.length?`販売前3日は「${domRole}」が多め。平均導線スコア${bScore}点。`:"販売前3日のデータが少ないため流れをまだ判定しきれません。"};
  });
}

function buildAuthUrl(cfg){
  const id=String(cfg?.clientId||"").trim();
  const uri=String(cfg?.redirectUri||"").trim();
  const sc=Array.isArray(cfg?.scopes)&&cfg.scopes.length?cfg.scopes:["threads_basic"];
  if(!id||!uri)return"";
  return`https:
}

function authDiagnostics(cfg){
  const id=String(cfg?.clientId||"").trim();
  const uri=String(cfg?.redirectUri||"").trim();
  const issues=[];
  if(!id)issues.push("Threads App ID / Client ID が空です。");
  if(id&&!/^[0-9]+$/.test(id))issues.push("Client IDは通常数字のみです。App SecretやAccess Tokenを入れていないか確認を。");
  if(!uri)issues.push("リダイレクトURLが空です。");
  if(uri&&uri.includes("your-domain.com"))issues.push("リダイレクトURLが仮URLのままです。実際に公開しているURLに変更してください。");
  if(uri&&!uri.startsWith("https:
  if(!(cfg?.scopes||[]).includes("threads_basic"))issues.push("threads_basicは基本的に必要です。");
  return issues;
}

function normalizeThreadsItem(item){
  const text=item?.text||item?.caption||"";
  const created=item?.timestamp||item?.created_time||"";
  const d=new Date(created);
  const date=isNaN(d)?new Date().toISOString().slice(0,10):d.toISOString().slice(0,10);
  const time=isNaN(d)?"21:00":d.toISOString().slice(11,16);
  const ins=item?.insights||{};
  return normalize({text,date,time,
    likes:ins.likes||ins.like_count||item?.like_count||0,
    replies:ins.replies||ins.reply_count||item?.reply_count||0,
    reposts:ins.reposts||ins.repost_count||item?.repost_count||0,
    views:ins.views||ins.view_count||item?.view_count||0,
    fc:0,noteClicks:0,noteSales:0,
  });
}

const card={background:C.s1,border:`1.5px solid ${C.border}`,borderRadius:16,padding:20,boxShadow:C.shadow};
const inp={background:C.s2,border:`1.5px solid ${C.border}`,borderRadius:10,padding:"10px 14px",color:C.text,width:"100%",fontSize:14,outline:"none",boxSizing:"border-box",fontFamily:"inherit"};
const lbl={display:"block",fontSize:11,color:C.muted,marginBottom:6,fontWeight:800,letterSpacing:"0.08em",textTransform:"uppercase"};
const mkbtn=(bg=C.pink,color="#fff",extra={})=>({background:bg,color,border:"none",borderRadius:10,padding:"11px 22px",cursor:"pointer",fontWeight:800,fontSize:14,fontFamily:"inherit",transition:"all 0.15s",boxShadow:bg===C.pink?"0 4px 14px rgba(232,65,122,0.25)":bg===C.orange?"0 4px 14px rgba(240,112,48,0.2)":bg===C.purple?"0 4px 14px rgba(139,53,204,0.2)":"none",...extra});

function Badge({children,color=C.pink,bg=C.pinkBg}){
  return<span style={{fontSize:10,padding:"3px 9px",borderRadius:20,background:bg,color,fontWeight:800}}>{children}</span>;
}
function ScoreBar({score}){
  return<div style={{height:6,borderRadius:999,background:"#f4e7fb",overflow:"hidden",marginTop:6}}><div style={{height:"100%",borderRadius:999,background:`linear-gradient(90deg,${C.pink},${C.purple})`,width:`${clamp(score,0,100)}%`}}/></div>;
}
function SectionTitle({icon,title,color=C.purple}){
  return<div style={{display:"flex",alignItems:"center",gap:8,marginBottom:14}}><div style={{width:4,height:20,background:color,borderRadius:4}}/><div style={{fontWeight:800,fontSize:15,color}}>{icon} {title}</div></div>;
}
function Tooltip2({active,payload,label}){
  if(!active||!payload?.length)return null;
  return<div style={{background:"#fff",border:`1.5px solid ${C.border}`,borderRadius:10,padding:"10px 14px",boxShadow:C.shadow,fontSize:12,color:C.text}}><div style={{fontWeight:700,marginBottom:4}}>{label}</div>{payload.map((p,i)=><div key={i} style={{color:p.color||C.purple}}>{p.name||p.dataKey}: {p.value}</div>)}</div>;
}

function Mkd({text}){
  return<div style={{lineHeight:1.9,fontSize:14,color:C.text}}>
    {String(text||"").split("\n").map((line,i)=>{
      if(/^#{1,2}\s/.test(line))return<div key={i} style={{fontWeight:900,fontSize:16,margin:"22px 0 8px",color:C.purple,borderLeft:`3px solid ${C.purple}`,paddingLeft:10}}>{line.replace(/^#+\s/,"")}</div>;
      if(/^###\s/.test(line))return<div key={i} style={{fontWeight:800,fontSize:14,margin:"14px 0 5px",color:C.pink}}>{line.replace(/^###\s/,"")}</div>;
      if(/^\d+\.\s/.test(line))return<div key={i} style={{padding:"6px 12px",margin:"4px 0",background:C.purpleBg,borderRadius:8,fontWeight:700,color:C.purple,fontSize:13}}>{line}</div>;
      if(line.startsWith("- ")||line.startsWith("・"))return<div key={i} style={{paddingLeft:16,color:C.sub,margin:"3px 0",display:"flex",gap:6}}><span style={{color:C.pinkL}}>›</span><span>{line.slice(2)}</span></div>;
      if(/^[📊⏰🧠🎯💰📈✅❌🔥💡⚠️🏆📉🎪💎]/.test(line))return<div key={i} style={{fontWeight:800,fontSize:14,margin:"14px 0 5px",color:C.pink,display:"flex",gap:6}}>{line}</div>;
      if(line.trim()==="")return<div key={i} style={{height:8}}/>;
      return<div key={i} style={{color:C.text,margin:"2px 0"}}>{line}</div>;
    })}
  </div>;
}

export default function App(){
  const[posts,setPosts]=useState(SAMPLE_POSTS);
  const[apiKey,setApiKey]=useState("");
  const[apiInput,setApiInput]=useState("");
  const[keySaved,setKeySaved]=useState(false);
  const[tab,setTab]=useState("dashboard");
  const[ready,setReady]=useState(false);
  const[form,setForm]=useState({text:"",date:new Date().toISOString().slice(0,10),time:"21:00",likes:"0",replies:"0",reposts:"0",views:"0",fc:"0",noteClicks:"0",noteSales:"0",hookType:"共感型",role:"共感",readerPsyche:"その他"});
  const[autoFill,setAutoFill]=useState(true);
  const[csvText,setCsvText]=useState("");
  const[csvMsg,setCsvMsg]=useState("");
  const[aiResult,setAiResult]=useState("");
  const[aiLoading,setAiLoading]=useState(false);
  const[analysisType,setAnalysisType]=useState("full");
  const[genResult,setGenResult]=useState("");
  const[genLoading,setGenLoading]=useState(false);
  const[genForm,setGenForm]=useState({theme:"",cta:"",product:"",tone:"共感型",goal:"フォロワー増加"});
  const[copied,setCopied]=useState(false);
  const[draftTheme,setDraftTheme]=useState("モラハラ証拠の集め方");
  const[threadsConfig,setThreadsConfig]=useState({clientId:"",redirectUri:"https:
  const[threadsJson,setThreadsJson]=useState("");
  const[threadsMsg,setThreadsMsg]=useState("");
  const[syncStatus,setSyncStatus]=useState("idle");
  const[profile,setProfile]=useState({goal:"月100万円安定収益",product:FUKU_KNOWLEDGE.productLine.main,target:FUKU_KNOWLEDGE.target,funnel:FUKU_KNOWLEDGE.salesFunnelDesign,message:FUKU_KNOWLEDGE.mainMessage,cta:FUKU_KNOWLEDGE.noteBridge[0]});

  useEffect(()=>{
    async function load(){
      try{
        const p=await window.storage.get("ka_posts3");
        if(p?.value)setPosts(JSON.parse(p.value));
        const k=await window.storage.get("th_key");
        if(k?.value){setApiKey(k.value);setApiInput(k.value);}
        const pr=await window.storage.get("ka_profile");
        if(pr?.value)setProfile(JSON.parse(pr.value));
      }catch(e){}
      setReady(true);
    }
    load();
  },[]);

  useEffect(()=>{
    if(!ready)return;
    window.storage.set("ka_posts3",JSON.stringify(posts)).catch(()=>{});
  },[posts,ready]);

  async function saveKey(){
    setApiKey(apiInput);
    await window.storage.set("th_key",apiInput).catch(()=>{});
    setKeySaved(true);setTimeout(()=>setKeySaved(false),2000);
  }
  async function saveProfile(){
    await window.storage.set("ka_profile",JSON.stringify(profile)).catch(()=>{});
    alert("プロフィールを保存しました");
  }

  const stats=useMemo(()=>{
    const fSorted=[...posts].sort((a,b)=>funnelScore(b)-funnelScore(a));
    const egSorted=[...posts].sort((a,b)=>eg(b)-eg(a));
    const avgEG=posts.length?(posts.reduce((s,p)=>s+eg(p),0)/posts.length).toFixed(2):"0.00";
    const avgFunnel=posts.length?Math.round(posts.reduce((s,p)=>s+funnelScore(p),0)/posts.length):0;
    const totalClicks=posts.reduce((s,p)=>s+toNum(p.noteClicks),0);
    const totalSales=posts.reduce((s,p)=>s+toNum(p.noteSales),0);
    const totalFC=posts.reduce((s,p)=>s+toNum(p.fc),0);
    const timeline=[...posts].sort((a,b)=>String(a.date).localeCompare(String(b.date))).map(p=>({date:String(p.date||"").slice(5),eg:eg(p),funnel:funnelScore(p),sales:toNum(p.noteSales),fc:toNum(p.fc)}));
    const hookData=HOOK_TYPES.map(h=>{const g=posts.filter(p=>p.hookType===h);return{h,funnel:g.length?Math.round(g.reduce((s,p)=>s+funnelScore(p),0)/g.length):0,eg:g.length?+(g.reduce((s,p)=>s+eg(p),0)/g.length).toFixed(2):0,n:g.length};}).filter(d=>d.n>0);
    const roleData=POST_ROLES.map(r=>{const g=posts.filter(p=>p.role===r);return{r,funnel:g.length?Math.round(g.reduce((s,p)=>s+funnelScore(p),0)/g.length):0,n:g.length};}).filter(d=>d.n>0);
    const hourData=Array.from({length:24},(_,h)=>{const g=posts.filter(p=>+p.time.split(":")[0]===h);return{h:`${h}時`,eg:g.length?+(g.reduce((s,p)=>s+eg(p),0)/g.length).toFixed(2):0,funnel:g.length?Math.round(g.reduce((s,p)=>s+funnelScore(p),0)/g.length):0,n:g.length};});
    const dayData=DAYS.map((d,i)=>{const g=posts.filter(p=>p.date&&new Date(p.date+"T12:00:00").getDay()===i);return{d,eg:g.length?+(g.reduce((s,p)=>s+eg(p),0)/g.length).toFixed(2):0,n:g.length};});
    const maxHour=hourData.reduce((m,d)=>d.n>0&&d.funnel>m.funnel?d:m,{h:"",funnel:0,n:0});
    const nextRec=recommendNext(posts);
    const saleWindows=analyzeSalesWindows(posts);
    const bestHook=[...hookData].sort((a,b)=>b.funnel-a.funnel)[0];
    const bestRole=[...roleData].sort((a,b)=>b.funnel-a.funnel)[0];
    return{fSorted,egSorted,avgEG,avgFunnel,totalClicks,totalSales,totalFC,timeline,hookData,roleData,hourData,dayData,maxHour,nextRec,saleWindows,bestHook,bestRole};
  },[posts]);

  function updateFormText(v){
    const au=autoClassify(v);
    setForm(f=>autoFill?{...f,text:v,hookType:au.hookType,role:au.role,readerPsyche:au.readerPsyche}:{...f,text:v});
  }
  function addPost(){
    if(!form.text.trim())return;
    const au=autoClassify(form.text);
    setPosts(prev=>[normalize({...form,hookType:autoFill?au.hookType:form.hookType,role:autoFill?au.role:form.role,readerPsyche:autoFill?au.readerPsyche:form.readerPsyche}),...prev]);
    setForm(f=>({...f,text:"",likes:"0",replies:"0",reposts:"0",views:"0",fc:"0",noteClicks:"0",noteSales:"0"}));
  }
  function importCsv(){
    const p=parseCsv(csvText);
    if(!p.length){setCsvMsg("読み込めませんでした。ヘッダー行とデータを確認してください。");return;}
    setPosts(prev=>[...p,...prev]);setCsvMsg(`${p.length}件を取り込みました。`);
  }
  function exportCsv(){setCsvText(toCsv(posts));setCsvMsg("現在のデータをCSV欄に出力しました。");}

  async function callAPI(system,user){
    if(!apiKey)throw new Error("APIキーが未設定です。⚙️設定タブで入力してください。");
    const res=await fetch("https:
      method:"POST",
      headers:{"Content-Type":"application/json","x-api-key":apiKey,"anthropic-version":"2023-06-01"},
      body:JSON.stringify({model:"claude-sonnet-4-20250514",max_tokens:2500,system,messages:[{role:"user",content:user}]})
    });
    const data=await res.json();
    if(data.error)throw new Error(data.error.message);
    return data.content?.filter(c=>c.type==="text").map(c=>c.text).join("\n")||"";
  }

  function buildCtx(){
    const all=stats.fSorted.map(p=>`[${p.date} ${p.time}][${p.hookType}][${p.role}][EG:${eg(p)}%][F:${p.fc>0?"+":""}${p.fc}][クリック率:${clickRate(p)}%][購入率:${salesRate(p)}%][導線:${funnelScore(p)}点] 「${p.text.slice(0,55)}」`).join("\n");
    const top3=stats.fSorted.slice(0,3).map(p=>`「${p.text.slice(0,60)}」→EG${eg(p)}% 導線${funnelScore(p)}点 クリック${p.noteClicks}件 購入${p.noteSales}件`).join("\n");
    const bot3=stats.fSorted.slice(-3).map(p=>`「${p.text.slice(0,60)}」→EG${eg(p)}% 導線${funnelScore(p)}点`).join("\n");
    return{all,top3,bot3};
  }

  async function runReflection(){
    setReflectLoading(true);setReflectResult("");
    try{
      const MK2=MASTER_KNOWLEDGE;
      const system=`あなたはThreads運用振り返りコーチ（離婚・モラハラジャンル特化）。ふく（fuku.2025_hpgd）専用で分析します。
【寝稼ぎ式】${MK2.nekasegi.roadmap.slice(0,3).join("→")}
【3大フック】おさる式: ${MK2.hookMethods.osaru.core} / 寝稼ぎ式: ${MK2.hookMethods.nekasegi.core} / ヒカさん式: ${MK2.hookMethods.hika.core}
【振り返り軸】${MK2.reflectionFramework.evaluationAxes.slice(0,4).join("・")}
【勝ちパターン】${MK2.reflectionFramework.winLosePattern.win}
人間味MAX、でも数字には厳しめに。`;
      const user=`【期間】${reflectForm.period||"今日"}\n【投稿内容】${reflectForm.posts_text||"なし"}\n【数字】${reflectForm.numbers||"なし"}\n【伸びた投稿】${reflectForm.win_post||"なし"}\n【弱かった投稿】${reflectForm.lose_post||"なし"}\n【迷い】${reflectForm.concern||"なし"}\n\n分析：1.総合評価(★5段階) 2.伸びた/伸びなかった理由(3手法視点で) 3.フック診断(10点満点+改善案) 4.投稿タイプ分類 5.CTA評価 6.バズ後の橋渡し投稿確認 7.note導線評価 8.次の24時間でやること3つ 9.次に出す投稿全文 10.今日の学び一言で`;
      const result=await callAPI(system,user);
      setReflectResult(result);
    }catch(e){setReflectResult("❌ エラー: "+e.message);}
    setReflectLoading(false);
  }

  async function runGhostReview(){
    if(!ghostText.trim())return alert("レビューしたい投稿文を入力してください");
    setGhostLoading(true);setGhostResult("");
    try{
      const MK2=MASTER_KNOWLEDGE;
      const system=`あなたはGhost Reviewer専門家。${MK2.aiTechniques.ghostReviewer.howto}\n${MK2.aiTechniques.ghostReviewer.benefit}`;
      const user=`【投稿文】\n${ghostText}\n\n4視点レビュー：\n## 視点1：3年後の自分（ブランドとして正解か）\n## 視点2：競合発信者（差別化できているか）\n## 視点3：買わなかった見込み客（何が引っかかったか）\n## 視点4：購入者（信頼残高は上がるか）\n\n最後に：一番直すべき点（1つ）＋改善版の投稿全文`;
      const result=await callAPI(system,user);
      setGhostResult(result);
    }catch(e){setGhostResult("❌ エラー: "+e.message);}
    setGhostLoading(false);
  }

    const ANALYSIS_TYPES=[
    {id:"full",label:"🔍 総合コンサル診断",desc:"マーケター目線で20項目深堀り"},
    {id:"content",label:"📊 コンテンツ・発信軸",desc:"伸びた/伸びなかった原因分析"},
    {id:"mindset",label:"🧠 心理・マインド分析",desc:"ボトルネックと思い込み"},
    {id:"sales",label:"💰 売上・導線診断",desc:"note・商品の売れる仕組み"},
    {id:"action",label:"🎯 次の一手（S/A/B別）",desc:"今週・今月のアクション"},
    {id:"risk",label:"⚠️ リスク診断",desc:"顕在・潜在リスクを洗い出す"},
    {id:"fan",label:"💜 ファン化6原理診断",desc:"仲間ポジ・属人性・救済etc"},
    {id:"note",label:"📝 noteタイミング分析",desc:"5STEP設計・売れる出し方"},
  ];

  const SYSTEMS={
    full:`あなたは月商1000万円以上を継続する日本トップクラスのSNS×コンテンツマーケティングコンサルタントです。クライアントはThreadsとnoteで稼ぐ「かおり（ふく（fuku.2025_hpgd））」さんです。

【クライアント基本情報】
${JSON.stringify(FUKU_KNOWLEDGE,null,1)}

【ファン化6原理】
${EXTENDED_KNOWLEDGE.fanPrinciples.sixPrinciples.map(p=>p.name+": "+p.core).join("\n")}

【noteタイミング5STEP】
${EXTENDED_KNOWLEDGE.noteTimingSteps.fiveSteps.map(s=>"STEP"+s.step+" "+s.name+": "+s.action).join("\n")}

【影響力・共闘リプ3型】
${EXTENDED_KNOWLEDGE.influenceStrategy.replyTypes.map(r=>r.name+"→"+r.benefit).join("\n")}

【noteタイトル公式】数字×感情×ギャップ。価格：エスカレーター式。

EG率=(いいね×1+返信×3+リポスト×2)/閲覧×100。バズ≠購入を前提に分析してください。

以下20項目を徹底分析してください（離婚・モラハラジャンル特化）：
# 1. 総合診断（ふくさんの強みと今すぐ直すべき弱みを率直に）
# 2. 発信軸評価（『損しないための準備の順番を届けるママ』として一貫しているか）
# 3. 伸びた投稿の共通パターンと再現性
# 4. 伸びなかった投稿の原因と改善案
# 5. EGが高い投稿 vs 購入につながる投稿の違い
# 6. ゴールデンタイム・曜日の最適化提案
# 7. フック種類別の効果分析
# 8. 発信者心理のボトルネック（マインドブロック）
# 9. 読者心理から見えるボトルネック
# 10. 売上導線の現状と改善案
# 11. 商品ラインナップの整理提案
# 12. 認知→共感→信頼→導線→購入のファネル評価
# 13. 競合比較・市場ポジション
# 14. 顕在リスク（今すぐ対処すべき）
# 15. 潜在リスク（このまま続けると）
# 16. このまま続けた場合の失敗シナリオ
# 17. 優先度S（今週中にやること）
# 18. 優先度A（今月中にやること）
# 19. 明日からすぐできる改善3つ
# 20. 次に出すべき投稿テーマ5つ（今すぐ使えるもの）

厳しく、でも愛を持って。褒めるだけでなく「ここが弱い、こう直せ」を具体的に。`,

    content:`Threads投稿の発信軸・コンテンツ戦略専門家として分析：
クライアント：ふく（fuku.2025_hpgd）（AI×note×副業）
# 発信軸の評価（何者として認識されているか）
# コンテンツ種類別効果（遊び・自己開示・実績・ノウハウ・告知）
# フック別効果比較と最適フック提案
# バズる投稿 vs noteが売れる投稿の違い
# 「9286件」という投稿量に対する質の評価
# 30日でやるべきコンテンツ戦略`,

    mindset:`マーケター兼心理コーチとして分析：
クライアント：ふく（fuku.2025_hpgd）
# 投稿傾向から読み取れる心理パターン
# マインドブロック（無意識の回避・恐れ）
# 「やりたいこと」と「やってること」のズレ
# 遊び発信への偏り vs 収益化発信のバランス
# 承認欲求・完璧主義・比較の影響
# 月100万安定のための心理的準備`,

    sales:`月商1000万コンサルとして売上導線を徹底診断：
クライアント：ふく（fuku.2025_hpgd）（AI×note）
# 現在の発信→購入の導線マップ
# 認知→共感→信頼→導線→購入のファネル評価
# noteクリック率・購入率の改善案
# 商品ラインナップ（1,980〜98,000円）の整理
# 固定投稿・プロフィール・CTAの改善点
# 月100万安定のための具体的な仕組み
# 月300万以上を目指すロードマップ
# noteタイミング設計：種まき→★→連続投稿→宣言→執筆の5ステップ評価
# ファン化6原理（仲間ポジ・属人性・途中・信用残高・救済・止まらない）の活用度`,

    action:`行動計画専門家として優先度別に整理：
クライアント：ふく（fuku.2025_hpgd）
# 優先度S（今週中・絶対やること）
# 優先度A（今月中・重要なこと）
# 優先度B（余裕があればやること）
# やめるべきこと・減らすべきこと
# 30日後・90日後の数値目標
# 明日からすぐできる小さな改善10個`,

    fan:`ファン化×影響力専門コンサルとして分析：
クライアント：ふく（fuku.2025_hpgd）
【ファン化6原理の活用度チェック】
${EXTENDED_KNOWLEDGE.fanPrinciples.sixPrinciples.map(p=>"■"+p.name+": "+p.core).join("\n")}

# 1. 現在の投稿における「仲間ポジション」の徹底度（先生型になっていないか）
# 2. 属人性の濃度評価（名前を変えても成立する投稿が何割か）
# 3. 途中を見せる投稿の割合と効果
# 4. 信用残高の積み上げ状況（1対1の積み重ね評価）
# 5. 救済型投稿の有無と「未来を見せる」設計
# 6. 止まらない仕組みができているか（仲間の巻き込み状況）
# 7. 大手への共闘リプ設計（コバンザメ vs 共闘者の違い）
# 8. noteタイミング5ステップの実践度
# 9. 発信軸の一貫性とブランド（煽らない・責めない・盛らない）
# 10. ファン化加速のための次のアクション5つ`,

    note:`noteタイミング×売上導線専門家として分析：
クライアント：ふく（fuku.2025_hpgd）
【noteタイミング5ステップ】
${EXTENDED_KNOWLEDGE.noteTimingSteps.fiveSteps.map(s=>"STEP"+s.step+" "+s.name+": "+s.action).join("\n")}

# 1. 現在の投稿はどのSTEPに相当するか分類
# 2. 種まき→需要発見→温度上げ→宣言→執筆の各STEPの穴
# 3. バズ依存型・ノルマ型・準備過剰型のどれに陥っているか
# 4. ★をつけるべき投稿（プロフ遷移率・コメント深さ）の評価
# 5. 連続投稿での温度上げ設計の提案
# 6. 宣言投稿のタイミングと文言案
# 7. noteの値付け戦略（エスカレーター式）の提案
# 8. SNS→固定ポスト→note購入の導線評価
# 9. 今すぐ種まきすべきテーマ3つ
# 10. 次に出すべきnoteのタイミング設計（宣言まで含む）`,

    risk:`リスク管理専門家として：
クライアント：ふく（fuku.2025_hpgd）
# 顕在リスク（投稿量依存、商品の多さ、ポジション不明確）
# 潜在リスク（このまま続けると起きること）
# 失敗シナリオ
# ブランドリスク（炎上・誤解・信頼棄損）
# プラットフォームリスク
# 各リスクへの対処法`,
  };

  async function runAnalysis(){
    setAiLoading(true);setAiResult("");
    try{
      const ctx=buildCtx();
      const user=`私（ふく（fuku.2025_hpgd））のThreads投稿データ（${posts.length}件）を分析してください。

【統計サマリー】
- 平均EG率: ${stats.avgEG}%
- 平均導線スコア: ${stats.avgFunnel}点
- 累計F増加: ${stats.totalFC>0?"+":""}${stats.totalFC}
- 累計noteクリック: ${stats.totalClicks}件
- 累計note購入: ${stats.totalSales}件
- ゴールデンタイム: ${stats.maxHour.n>0?stats.maxHour.h:"データ不足"}
- 強いフック: ${stats.bestHook?.h||"データ不足"}
- 強い役割: ${stats.bestRole?.r||"データ不足"}

【導線スコアTOP3】
${ctx.top3}

【要改善投稿】
${ctx.bot3}

【全投稿データ】
${ctx.all}

データに基づいて断言してください。「〜かもしれません」より「〜です、なぜなら〜」で。`;
      const result=await callAPI(SYSTEMS[analysisType]||SYSTEMS.full,user);
      setAiResult(result);
    }catch(e){setAiResult("❌ エラー: "+e.message);}
    setAiLoading(false);
  }

  async function generatePosts(){
    if(!genForm.theme.trim())return alert("テーマを入力してください");
    setGenLoading(true);setGenResult("");
    try{
      const ctx=buildCtx();
      const result=await callAPI(
        `あなたはThreads専門の一流コピーライター。ふく（fuku.2025_hpgd）（AI×note×副業）の文体を完璧に模倣する。
ルール：冒頭1行が命・do精神・かわいい×AI×稼ぐ・売り込み感ゼロ・自然なCTA・改行効果的。
クライアントナレッジ：${JSON.stringify({winningPatterns:FUKU_KNOWLEDGE.winningPatterns,hookRules:FUKU_KNOWLEDGE.hookRules,noteBridge:FUKU_KNOWLEDGE.noteBridge,avoid:FUKU_KNOWLEDGE.avoid},null,1)}`,
        `私のThreadsに合った投稿案を生成してください。

【私のTOP投稿（トーン参考）】
${ctx.top3}

【条件】
テーマ：${genForm.theme}
フック：${genForm.tone}
CTA：${genForm.cta||"なし"}
商品：${genForm.product||"なし"}
目的：${genForm.goal}

【5パターン生成】
## パターン1：超短文インパクト型（80文字以内）
## パターン2：共感ストーリー型（180文字程度）
## パターン3：数字・実績型（150文字程度）
## パターン4：逆説・気づき型（120文字程度）
## パターン5：note導線型（200文字程度・CTAをナチュラルに）

各パターン後に：
▶ なぜこのフックが効くか（1行）
▶ 最適な投稿時間帯（1行）`
      );
      setGenResult(result);
    }catch(e){setGenResult("❌ エラー: "+e.message);}
    setGenLoading(false);
  }

  async function syncFromBackend(){
    const url=String(threadsConfig.backendUrl||"").trim().replace(/\/$/,"");
    if(!url||url.includes("your-domain.com")){setThreadsMsg("バックエンドURLが仮URLのままです。");return;}
    setSyncStatus("loading");setThreadsMsg("取得中...");
    try{
      const res=await fetch(`${url}/posts`);
      if(!res.ok)throw new Error(`HTTP ${res.status}`);
      const raw=await res.json();
      const items=Array.isArray(raw)?raw:Array.isArray(raw?.data)?raw.data:[];
      const converted=items.map(normalizeThreadsItem).filter(p=>p.text);
      if(!converted.length){setSyncStatus("error");setThreadsMsg("取り込めるデータがありませんでした。");return;}
      setPosts(prev=>[...converted,...prev]);
      setThreadsJson(JSON.stringify(raw,null,2));
      setSyncStatus("success");setThreadsMsg(`${converted.length}件を同期しました。noteクリック・購入数は手入力してください。`);
    }catch(e){setSyncStatus("error");setThreadsMsg(`同期失敗: ${e.message}`);}
  }

  function importThreadsJson(){
    try{
      const raw=JSON.parse(threadsJson);
      const items=Array.isArray(raw)?raw:Array.isArray(raw?.data)?raw.data:[];
      const converted=items.map(normalizeThreadsItem).filter(p=>p.text);
      if(!converted.length){setThreadsMsg("取り込めるデータが見つかりませんでした。");return;}
      setPosts(prev=>[...converted,...prev]);
      setThreadsMsg(`${converted.length}件を取り込みました。noteクリック・購入数は手入力してください。`);
    }catch(e){setThreadsMsg("JSONの形式を確認してください: "+e.message);}
  }

  function loadSampleJson(){
    setThreadsJson(JSON.stringify({data:[
      {text:"ChatGPTに世界観を学習させてカルーセルを10秒で作る方法。知らないと損すぎる。",timestamp:"2026-05-25T03:00:00Z",insights:{views:32000,likes:523,replies:89,reposts:145}},
      {text:"2ヶ月で売上500万円になった。でも最初の3ヶ月は1円も稼げなかった。",timestamp:"2026-05-26T12:00:00Z",insights:{views:48000,likes:789,replies:167,reposts:234}},
    ]},null,2));
  }

  const authUrl=buildAuthUrl(threadsConfig);
  const authIssues=authDiagnostics(threadsConfig);

  const TABS=[
    {id:"dashboard",label:"📊 分析"},
    {id:"input",label:"✍️ 入力"},
    {id:"csv",label:"📋 CSV"},
    {id:"reflection",label:"🔄 振り返り"},
    {id:"ghost",label:"👻 Ghost Review"},
    {id:"threads",label:"🔗 Threads連携"},
    {id:"analysis",label:"🧠 AI深層分析"},
    {id:"generate",label:"✨ 投稿生成"},
    {id:"sales",label:"💰 売れた前後"},
    {id:"knowledge",label:"📚 ナレッジ"},
    {id:"settings",label:"⚙️ 設定"},
  ];

  const GRAD="linear-gradient(135deg,#e8417a,#8b35cc)";
  const egColor=v=>v>=2?C.green:v>=1?C.gold:C.red;
  const fcColor=v=>v>0?C.green:v<0?C.red:C.muted;

  return(
    <div style={{background:C.bg,minHeight:"100vh",color:C.text,fontFamily:'"Hiragino Kaku Gothic ProN","Hiragino Sans","Yu Gothic",sans-serif',fontSize:14}}>

      <div style={{background:"linear-gradient(135deg,#fff0f8 0%,#f5eeff 50%,#fff4ee 100%)",borderBottom:`1.5px solid ${C.border}`,padding:"0 16px",position:"sticky",top:0,zIndex:100,boxShadow:"0 2px 16px rgba(180,100,220,0.08)"}}>
        <div style={{maxWidth:1200,margin:"0 auto",display:"flex",alignItems:"center",gap:6,minHeight:56,flexWrap:"wrap",padding:"8px 0"}}>
          <div style={{fontWeight:900,fontSize:18,marginRight:8,whiteSpace:"nowrap",background:GRAD,WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent"}}>
            ✦ kaori's Threads Funnel
          </div>
          <div style={{display:"flex",flexWrap:"wrap",gap:5,flex:1}}>
            {TABS.map(t=>(
              <button key={t.id} onClick={()=>setTab(t.id)} style={{
                background:tab===t.id?GRAD:"transparent",
                color:tab===t.id?"#fff":C.sub,
                border:tab===t.id?"none":`1.5px solid ${C.border}`,
                borderRadius:20,padding:"5px 12px",cursor:"pointer",fontSize:11,fontWeight:700,fontFamily:"inherit",whiteSpace:"nowrap",
                boxShadow:tab===t.id?"0 3px 12px rgba(139,53,204,0.25)":"none",
              }}>{t.label}</button>
            ))}
          </div>
          <div style={{fontSize:11,color:C.muted,background:C.purpleBg,padding:"4px 10px",borderRadius:20,whiteSpace:"nowrap"}}>{posts.length}件</div>
        </div>
      </div>

      <div style={{maxWidth:1200,margin:"0 auto",padding:16}}>

        {tab==="dashboard"&&(
          <div style={{display:"flex",flexDirection:"column",gap:12}}>

            <div style={{display:"grid",gridTemplateColumns:"repeat(6,1fr)",gap:10}}>
              {[
                {label:"投稿数",v:posts.length+"件",c:C.purple,bg:C.purpleBg,icon:"📝"},
                {label:"平均EG率",v:stats.avgEG+"%",c:C.pink,bg:C.pinkBg,icon:"💫"},
                {label:"平均導線スコア",v:stats.avgFunnel+"点",c:C.purple,bg:C.purpleBg,icon:"🎯"},
                {label:"累計note購入",v:stats.totalSales+"件",c:C.orange,bg:C.orangeBg,icon:"💰"},
                {label:"累計F増加",v:(stats.totalFC>0?"+":"")+stats.totalFC,c:C.green,bg:C.greenBg,icon:"👥"},
                {label:"ゴールデンタイム",v:stats.maxHour.n>0?stats.maxHour.h:"データ不足",c:C.gold,bg:C.goldBg,icon:"⏰"},
              ].map((k,i)=>(
                <div key={i} style={{...card,textAlign:"center",padding:14,background:`linear-gradient(135deg,#fff,${k.bg})`,borderColor:k.c+"33"}}>
                  <div style={{fontSize:18,marginBottom:3}}>{k.icon}</div>
                  <div style={{fontSize:9,color:C.muted,fontWeight:800,letterSpacing:"0.06em",marginBottom:5}}>{k.label}</div>
                  <div style={{fontSize:18,fontWeight:900,color:k.c}}>{k.v}</div>
                </div>
              ))}
            </div>

            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
              <div style={card}>
                <SectionTitle icon="📈" title="EG率・導線スコアの推移" color={C.pink}/>
                <ResponsiveContainer width="100%" height={190}>
                  <LineChart data={stats.timeline}>
                    <CartesianGrid stroke={C.border} strokeDasharray="3 3"/>
                    <XAxis dataKey="date" stroke={C.muted} tick={{fontSize:10,fill:C.muted}}/>
                    <YAxis stroke={C.muted} tick={{fontSize:10,fill:C.muted}}/>
                    <Tooltip content={<Tooltip2/>}/>
                    <Line type="monotone" dataKey="eg" stroke={C.pink} strokeWidth={2.5} dot={{fill:C.pink,r:3}} name="EG率%"/>
                    <Line type="monotone" dataKey="funnel" stroke={C.purple} strokeWidth={2.5} dot={{fill:C.purple,r:3}} name="導線スコア"/>
                  </LineChart>
                </ResponsiveContainer>
              </div>
              <div style={card}>
                <SectionTitle icon="👥" title="フォロワー増減・note購入" color={C.purple}/>
                <ResponsiveContainer width="100%" height={190}>
                  <BarChart data={stats.timeline}>
                    <CartesianGrid stroke={C.border} strokeDasharray="3 3"/>
                    <XAxis dataKey="date" stroke={C.muted} tick={{fontSize:10,fill:C.muted}}/>
                    <YAxis stroke={C.muted} tick={{fontSize:10,fill:C.muted}}/>
                    <Tooltip content={<Tooltip2/>}/>
                    <Bar dataKey="fc" name="F増減" radius={[4,4,0,0]}>{stats.timeline.map((d,i)=><Cell key={i} fill={d.fc>=0?C.green:C.red}/>)}</Bar>
                    <Bar dataKey="sales" name="note購入" fill={C.orange} radius={[4,4,0,0]}/>
                  </BarChart>
                </ResponsiveContainer>
              </div>
            </div>

            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:12}}>
              <div style={card}>
                <SectionTitle icon="⏰" title="時間帯別EG率" color={C.orange}/>
                <ResponsiveContainer width="100%" height={160}>
                  <BarChart data={stats.hourData.filter(d=>d.n>0)} layout="vertical">
                    <XAxis type="number" stroke={C.muted} tick={{fontSize:9,fill:C.muted}}/>
                    <YAxis dataKey="h" type="category" stroke={C.muted} tick={{fontSize:9,fill:C.muted}} width={30}/>
                    <Tooltip content={<Tooltip2/>}/>
                    <Bar dataKey="eg" name="EG率%" radius={[0,4,4,0]}>{stats.hourData.filter(d=>d.n>0).map((d,i)=><Cell key={i} fill={d.h===stats.maxHour.h?C.orange:C.purpleL} fillOpacity={d.h===stats.maxHour.h?1:0.6}/>)}</Bar>
                  </BarChart>
                </ResponsiveContainer>
              </div>
              <div style={card}>
                <SectionTitle icon="🎣" title="フック別・導線の強さ" color={C.pink}/>
                <ResponsiveContainer width="100%" height={160}>
                  <BarChart data={stats.hookData} layout="vertical">
                    <XAxis type="number" stroke={C.muted} tick={{fontSize:9,fill:C.muted}}/>
                    <YAxis dataKey="h" type="category" stroke={C.muted} tick={{fontSize:9,fill:C.muted}} width={60}/>
                    <Tooltip content={<Tooltip2/>}/>
                    <Bar dataKey="funnel" name="導線スコア" radius={[0,4,4,0]}>{stats.hookData.map((_,i)=><Cell key={i} fill={[C.pink,C.purple,C.orange,C.green,C.purpleL,C.pinkL,C.gold,C.orangeL][i%8]}/>)}</Bar>
                  </BarChart>
                </ResponsiveContainer>
              </div>
              <div style={card}>
                <SectionTitle icon="📅" title="曜日別EG率" color={C.purple}/>
                <ResponsiveContainer width="100%" height={160}>
                  <BarChart data={stats.dayData}>
                    <CartesianGrid stroke={C.border} strokeDasharray="3 3"/>
                    <XAxis dataKey="d" stroke={C.muted} tick={{fontSize:11,fill:C.muted}}/>
                    <YAxis stroke={C.muted} tick={{fontSize:9,fill:C.muted}}/>
                    <Tooltip content={<Tooltip2/>}/>
                    <Bar dataKey="eg" name="EG率%" radius={[4,4,0,0]}>{stats.dayData.map((d,i)=><Cell key={i} fill={C.pink} fillOpacity={d.eg>0?Math.min(0.3+d.eg*0.2,1):0.1}/>)}</Bar>
                  </BarChart>
                </ResponsiveContainer>
              </div>
            </div>

            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
              {[
                {label:"🏆 導線スコアTOP3",color:C.green,bg:C.greenBg,data:stats.fSorted.slice(0,3)},
                {label:"📉 要改善投稿",color:C.red,bg:C.redBg,data:stats.fSorted.slice(-3).reverse()},
              ].map((sec,si)=>(
                <div key={si} style={{...card,borderColor:sec.color+"33"}}>
                  <SectionTitle icon="" title={sec.label} color={sec.color}/>
                  {sec.data.map((p,i)=>(
                    <div key={p.id} style={{background:sec.bg,borderRadius:12,padding:12,marginBottom:8}}>
                      <div style={{display:"flex",justifyContent:"space-between",marginBottom:5}}>
                        <div style={{display:"flex",gap:5,flexWrap:"wrap",alignItems:"center"}}>
                          <span style={{fontSize:10,color:C.muted}}>{p.date} {p.time}</span>
                          <Badge color={C.purple} bg={C.purpleBg}>{p.hookType}</Badge>
                          <Badge color={C.orange} bg={C.orangeBg}>{p.role}</Badge>
                        </div>
                        <div style={{display:"flex",gap:6,alignItems:"center"}}>
                          <span style={{color:egColor(eg(p)),fontWeight:900,fontSize:12,background:sec.bg,padding:"2px 7px",borderRadius:8}}>EG {eg(p)}%</span>
                          <span style={{color:C.purple,fontWeight:900,fontSize:12}}>導{funnelScore(p)}点</span>
                        </div>
                      </div>
                      <div style={{fontSize:13,lineHeight:1.6,marginBottom:5}}>{p.text.slice(0,60)}{p.text.length>60?"…":""}</div>
                      <div style={{display:"flex",gap:8,fontSize:11,color:C.muted}}>
                        <span>❤️{p.likes}</span><span>💬{p.replies}</span><span>🔁{p.reposts}</span><span>👀{(p.views||0).toLocaleString()}</span>
                        <span>📎{p.noteClicks}click</span><span style={{color:C.orange,fontWeight:700}}>💰{p.noteSales}件</span>
                        {p.fc!==0&&<span style={{color:fcColor(p.fc),fontWeight:700}}>F{p.fc>0?"+":""}{p.fc}</span>}
                      </div>
                    </div>
                  ))}
                </div>
              ))}
            </div>
          </div>
        )}

        {tab==="input"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1.5fr",gap:16}}>
            <div style={card}>
              <SectionTitle icon="＋" title="投稿を追加" color={C.pink}/>
              <div style={{display:"flex",alignItems:"center",gap:8,marginBottom:12,fontSize:13,color:C.sub}}>
                <input type="checkbox" checked={autoFill} onChange={e=>setAutoFill(e.target.checked)} style={{width:16}}/>
                <span style={{fontWeight:700}}>本文から自動分類する</span>
              </div>
              <div style={{marginBottom:10}}>
                <label style={lbl}>投稿本文 *</label>
                <textarea value={form.text} onChange={e=>updateFormText(e.target.value)} style={{...inp,height:90,resize:"vertical"}} placeholder="投稿内容を入力..."/>
              </div>
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:8,marginBottom:10}}>
                <div><label style={lbl}>日付</label><input type="date" value={form.date} onChange={e=>setForm(f=>({...f,date:e.target.value}))} style={inp}/></div>
                <div><label style={lbl}>時間</label><input type="time" value={form.time} onChange={e=>setForm(f=>({...f,time:e.target.value}))} style={inp}/></div>
              </div>
              <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:8,marginBottom:10}}>
                {[["likes","❤️いいね"],["replies","💬返信"],["reposts","🔁リポスト"],["views","👀閲覧数"],["fc","F増減"],["noteClicks","📎クリック"]].map(([k,l])=>(
                  <div key={k}><label style={lbl}>{l}</label><input type="number" value={form[k]} onChange={e=>setForm(f=>({...f,[k]:e.target.value}))} style={inp} min={k==="fc"?undefined:"0"}/></div>
                ))}
              </div>
              <div style={{marginBottom:10}}>
                <label style={lbl}>💰 note購入数</label>
                <input type="number" min="0" value={form.noteSales} onChange={e=>setForm(f=>({...f,noteSales:e.target.value}))} style={inp}/>
              </div>
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:8,marginBottom:14}}>
                <div><label style={lbl}>フック</label>
                  <select value={form.hookType} onChange={e=>setForm(f=>({...f,hookType:e.target.value}))} style={{...inp,cursor:"pointer"}}>
                    {HOOK_TYPES.map(h=><option key={h}>{h}</option>)}
                  </select>
                </div>
                <div><label style={lbl}>役割</label>
                  <select value={form.role} onChange={e=>setForm(f=>({...f,role:e.target.value}))} style={{...inp,cursor:"pointer"}}>
                    {POST_ROLES.map(r=><option key={r}>{r}</option>)}
                  </select>
                </div>
                <div><label style={lbl}>読者心理</label>
                  <select value={form.readerPsyche} onChange={e=>setForm(f=>({...f,readerPsyche:e.target.value}))} style={{...inp,cursor:"pointer"}}>
                    {READER_PSYCHES.map(r=><option key={r}>{r}</option>)}
                  </select>
                </div>
              </div>
              <div style={{display:"flex",gap:8,flexWrap:"wrap"}}>
                <button onClick={addPost} style={{...mkbtn(),flex:1}}>＋ 追加</button>
                <button onClick={()=>setPosts(SAMPLE_POSTS)} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,boxShadow:"none"}}>サンプル</button>
                <button onClick={()=>{if(window.confirm("全削除しますか？"))setPosts([]);}} style={{...mkbtn(C.redBg,C.red),border:`1.5px solid ${C.red}44`,boxShadow:"none"}}>全削除</button>
              </div>
              <div style={{marginTop:12,padding:12,background:C.purpleBg,borderRadius:10,fontSize:12,color:C.sub,lineHeight:1.8}}>
                💡 Threadsアプリ → 自分の投稿 →「インサイト」から数値をコピー。noteクリック数はnoteのダッシュボードから確認できます。
              </div>
            </div>
            <div>
              <div style={{fontWeight:700,marginBottom:10,color:C.sub,fontSize:13}}>投稿一覧（{posts.length}件）導線スコア順</div>
              <div style={{maxHeight:700,overflowY:"auto",display:"flex",flexDirection:"column",gap:8}}>
                {stats.fSorted.map((p,i)=>(
                  <div key={p.id} style={{...card,padding:12,borderLeft:`4px solid ${i<3?C.green:i>=stats.fSorted.length-3?C.red:C.border}`}}>
                    <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start",marginBottom:5}}>
                      <div style={{display:"flex",gap:5,flexWrap:"wrap",alignItems:"center"}}>
                        <span style={{fontSize:10,color:C.muted}}>{p.date} {p.time}</span>
                        <Badge color={C.purple} bg={C.purpleBg}>{p.hookType}</Badge>
                        <Badge color={C.orange} bg={C.orangeBg}>{p.role}</Badge>
                        {i<3&&<Badge color={C.green} bg={C.greenBg}>TOP</Badge>}
                      </div>
                      <div style={{display:"flex",gap:6,alignItems:"center"}}>
                        <span style={{fontWeight:900,color:egColor(eg(p)),fontSize:12,padding:"2px 7px",borderRadius:8,background:C.pinkBg}}>EG {eg(p)}%</span>
                        <span style={{fontWeight:900,color:C.purple,fontSize:12}}>導{funnelScore(p)}点</span>
                        <button onClick={()=>setPosts(prev=>prev.filter(pp=>pp.id!==p.id))} style={{background:C.redBg,border:"none",color:C.red,cursor:"pointer",fontSize:12,padding:"2px 7px",borderRadius:8}}>×</button>
                      </div>
                    </div>
                    <ScoreBar score={funnelScore(p)}/>
                    <div style={{fontSize:13,lineHeight:1.6,marginTop:8,marginBottom:5}}>{p.text}</div>
                    <div style={{display:"flex",gap:8,fontSize:11,color:C.muted,flexWrap:"wrap"}}>
                      <span>❤️{p.likes}</span><span>💬{p.replies}</span><span>🔁{p.reposts}</span><span>👀{(p.views||0).toLocaleString()}</span>
                      <span style={{color:C.orange}}>📎{p.noteClicks}click</span><span style={{color:C.orange,fontWeight:700}}>💰{p.noteSales}件</span>
                      {p.fc!==0&&<span style={{color:fcColor(p.fc),fontWeight:700}}>F{p.fc>0?"+":""}{p.fc}</span>}
                    </div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        )}

        {tab==="csv"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:16}}>
            <div style={card}>
              <SectionTitle icon="📋" title="CSVインポート / エクスポート" color={C.purple}/>
              <p style={{color:C.sub,fontSize:13,marginBottom:12,lineHeight:1.7}}>ヘッダー行：text,date,time,likes,replies,reposts,views,fc,noteClicks,noteSales（hookType/role/readerPsycheは省略可・自動判定）</p>
              <textarea style={{...inp,height:280,resize:"vertical"}} value={csvText} onChange={e=>setCsvText(e.target.value)} placeholder={CSV_COLS.join(",")}/>
              <div style={{display:"flex",gap:8,marginTop:10,flexWrap:"wrap"}}>
                <button onClick={importCsv} style={mkbtn()}>取り込む</button>
                <button onClick={()=>{setCsvText(["text,date,time,likes,replies,reposts,views,fc,noteClicks,noteSales","\"ChatGPTに世界観を学習させてみた\",2026-05-25,21:00,523,89,145,32000,67,56,3"].join(NL));}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,boxShadow:"none"}}>サンプル</button>
                <button onClick={exportCsv} style={{...mkbtn(C.orangeBg,C.orange),border:`1.5px solid ${C.border}`,boxShadow:"none"}}>書き出す</button>
              </div>
              {csvMsg&&<div style={{marginTop:10,padding:12,background:C.greenBg,borderRadius:10,color:C.green,fontSize:13,fontWeight:700}}>{csvMsg}</div>}
            </div>
            <div style={card}>
              <SectionTitle icon="📖" title="CSV列の意味" color={C.orange}/>
              <div style={{display:"flex",flexDirection:"column",gap:8}}>
                {[["text","投稿本文（必須）"],["date","投稿日 YYYY-MM-DD"],["time","投稿時間 HH:MM"],["likes","いいね数"],["replies","返信数"],["reposts","リポスト数"],["views","閲覧数（インプレッション）"],["fc","フォロワー増減（±）"],["noteClicks","noteクリック数"],["noteSales","note購入数"],["hookType","フックタイプ（省略可）"],["role","投稿役割（省略可）"],["readerPsyche","読者心理（省略可）"]].map(([k,v])=>(
                  <div key={k} style={{padding:"8px 12px",background:C.s2,borderRadius:8,display:"flex",gap:12}}>
                    <code style={{color:C.purple,fontWeight:800,minWidth:90}}>{k}</code>
                    <span style={{color:C.sub,fontSize:13}}>{v}</span>
                  </div>
                ))}
              </div>
            </div>
          </div>
        )}

        {tab==="threads"&&(
          <div style={{display:"flex",flexDirection:"column",gap:12}}>
            <div style={{...card,background:"linear-gradient(135deg,#fff0f5,#f5eeff)"}}>
              <SectionTitle icon="🔗" title="Threads公式API連携" color={C.purple}/>
              <div style={{color:C.sub,fontSize:13,lineHeight:1.8}}>
                <strong style={{color:C.pink}}>重要：</strong>App SecretとAccess Tokenは絶対にReactアプリに置かない。バックエンド（Vercel/Cloudflare Workers/GAS）経由が必須です。
              </div>
              <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:10,marginTop:12}}>
                {["① Metaでデベロッパーアカウント作成→アプリ作成（Threads APIユースケース選択）","② Threadsテスターとして自分を招待→Threadsアプリ側で承認（審査不要・個人利用OK）","③ バックエンドでOAuth→code→access_token交換→Threads API呼び出し→このアプリへ返す"].map((s,i)=>(
                  <div key={i} style={{padding:"12px 14px",background:"rgba(255,255,255,0.8)",borderRadius:12,border:`1.5px solid ${C.border}`,fontSize:12,color:C.sub,lineHeight:1.7}}>
                    <span style={{fontWeight:800,color:C.purple}}>{s.split("→")[0].split("①②③"[i])}</span>{s}
                  </div>
                ))}
              </div>
            </div>

            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
              <div style={card}>
                <SectionTitle icon="🔑" title="OAuth設定" color={C.pink}/>
                <div style={{display:"flex",flexDirection:"column",gap:10}}>
                  <div>
                    <label style={lbl}>Threads App ID / Client ID</label>
                    <input value={threadsConfig.clientId} onChange={e=>setThreadsConfig(c=>({...c,clientId:e.target.value}))} style={inp} placeholder="数字だけのID（例：1234567890）"/>
                  </div>
                  <div>
                    <label style={lbl}>OAuthリダイレクトURL（バックエンド側）</label>
                    <input value={threadsConfig.redirectUri} onChange={e=>setThreadsConfig(c=>({...c,redirectUri:e.target.value}))} style={inp}/>
                  </div>
                  <div>
                    <label style={lbl}>バックエンドAPI URL</label>
                    <input value={threadsConfig.backendUrl} onChange={e=>setThreadsConfig(c=>({...c,backendUrl:e.target.value}))} style={inp} placeholder="https:
                  </div>
                  <div>
                    <label style={lbl}>利用スコープ</label>
                    {THREADS_SCOPES.map(s=>(
                      <label key={s} style={{display:"flex",alignItems:"center",gap:8,marginBottom:6,fontSize:13,color:C.sub,fontWeight:600}}>
                        <input type="checkbox" checked={threadsConfig.scopes.includes(s)} onChange={()=>setThreadsConfig(c=>({...c,scopes:c.scopes.includes(s)?c.scopes.filter(x=>x!==s):[...c.scopes,s]}))} style={{width:16}}/>{s}
                      </label>
                    ))}
                  </div>
                  <div style={{background:C.s2,borderRadius:10,padding:12,fontSize:11,fontFamily:"monospace",color:C.text,wordBreak:"break-all",lineHeight:1.7}}>
                    {authUrl||"Client IDとリダイレクトURLを入力すると認可URLが生成されます"}
                  </div>
                  {authIssues.length>0?(
                    <div style={{padding:12,background:C.pinkBg,borderRadius:10,fontSize:12,color:C.pink,fontWeight:700}}>
                      {authIssues.map(i=><div key={i}>⚠️ {i}</div>)}
                    </div>
                  ):(
                    <div style={{padding:12,background:C.greenBg,borderRadius:10,fontSize:12,color:C.green,fontWeight:700}}>✅ 認可URLが生成されています</div>
                  )}
                  <div style={{display:"flex",gap:8}}>
                    <button onClick={()=>navigator.clipboard?.writeText(authUrl||"")} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,boxShadow:"none",fontSize:12}}>URLをコピー</button>
                    <button onClick={()=>authUrl&&window.open(authUrl,"_blank")} style={{...mkbtn(),fontSize:12}}>認可URLを開く</button>
                    <button onClick={syncFromBackend} disabled={syncStatus==="loading"} style={{...mkbtn(C.orangeBg,C.orange),border:`1.5px solid ${C.border}`,boxShadow:"none",fontSize:12,opacity:syncStatus==="loading"?0.5:1}}>{syncStatus==="loading"?"同期中...":"バックエンドと同期"}</button>
                  </div>
                </div>
              </div>
              <div style={card}>
                <SectionTitle icon="📥" title="Threads APIデータを仮取り込み" color={C.orange}/>
                <p style={{color:C.sub,fontSize:12,marginBottom:10,lineHeight:1.7}}>バックエンド完成前に、Threads APIから返る想定のJSONを貼って分析できます。</p>
                <textarea style={{...inp,height:240,resize:"vertical",fontFamily:"monospace",fontSize:12}} value={threadsJson} onChange={e=>setThreadsJson(e.target.value)} placeholder='{"data":[{"text":"投稿本文","timestamp":"2026-05-25T12:00:00Z","insights":{"views":1000,"likes":20,"replies":3,"reposts":2}}]}'/>
                <div style={{display:"flex",gap:8,marginTop:10}}>
                  <button onClick={importThreadsJson} style={mkbtn()}>JSONを取り込む</button>
                  <button onClick={loadSampleJson} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,boxShadow:"none"}}>サンプルJSON</button>
                </div>
                {threadsMsg&&<div style={{marginTop:10,padding:12,background:syncStatus==="error"?C.redBg:C.greenBg,borderRadius:10,color:syncStatus==="error"?C.red:C.green,fontSize:12,fontWeight:700}}>{threadsMsg}</div>}
                <div style={{marginTop:12,display:"flex",flexDirection:"column",gap:8}}>
                  {[
                    {t:"取得できるデータ",c:C.greenBg,v:"投稿本文・投稿日・いいね・返信・リポスト・閲覧数"},
                    {t:"手入力が必要なもの",c:C.goldBg,v:"noteクリック数・note購入数（noteダッシュボードから）"},
                    {t:"⚠️ 絶対にここに貼らないもの",c:C.redBg,v:"App Secret・Access Token（バックエンドのみで使う）"},
                  ].map((item,i)=>(
                    <div key={i} style={{padding:"10px 12px",background:item.c,borderRadius:10,fontSize:12,lineHeight:1.7}}>
                      <div style={{fontWeight:800,marginBottom:2}}>{item.t}</div>
                      <div style={{color:C.sub}}>{item.v}</div>
                    </div>
                  ))}
                </div>
              </div>
            </div>

            <div style={card}>
              <SectionTitle icon="🛠️" title="バックエンド設計ガイド（Vercel / Cloudflare Workers推奨）" color={C.purple}/>
              <div style={{display:"grid",gridTemplateColumns:"repeat(4,1fr)",gap:10}}>
                {[
                  {path:"GET /auth/start",desc:"threads.net/oauth/authorizeへリダイレクト"},
                  {path:"GET /callback",desc:"codeを受け取りaccess_tokenへ交換（App Secretはここだけ）"},
                  {path:"GET /api/threads/posts",desc:"Threads API呼び出し・インサイト取得・このアプリの形式に変換して返す"},
                  {path:"ENV変数",desc:"THREADS_APP_ID / THREADS_APP_SECRET / THREADS_ACCESS_TOKEN（Reactには置かない）"},
                ].map((item,i)=>(
                  <div key={i} style={{padding:"12px 14px",background:C.purpleBg,borderRadius:12,border:`1.5px solid ${C.border}`}}>
                    <div style={{fontWeight:800,fontSize:12,color:C.purple,marginBottom:5,fontFamily:"monospace"}}>{item.path}</div>
                    <div style={{color:C.sub,fontSize:12,lineHeight:1.6}}>{item.desc}</div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        )}

        {tab==="analysis"&&(
          <div style={{display:"flex",flexDirection:"column",gap:12}}>
            <div style={card}>
              <SectionTitle icon="🧠" title="マーケターコンサル脳 × AI深層分析" color={C.purple}/>
              <p style={{color:C.sub,fontSize:13,lineHeight:1.8,marginBottom:12}}>月100万以上稼ぐマーケターの視点でかおりさんの投稿を徹底分析します。6種類から選んで実行してください。</p>
              {!apiKey&&<div style={{padding:12,background:C.pinkBg,borderRadius:10,border:`1.5px solid ${C.pink}44`,marginBottom:12,fontSize:13,color:C.pink,fontWeight:700}}>⚠️ まず「⚙️ 設定」タブでAPIキーを入力してください</div>}
              <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:8,marginBottom:14}}>
                {ANALYSIS_TYPES.map(a=>(
                  <button key={a.id} onClick={()=>setAnalysisType(a.id)} style={{
                    background:analysisType===a.id?GRAD:C.s2,
                    color:analysisType===a.id?"#fff":C.sub,
                    border:`1.5px solid ${analysisType===a.id?"transparent":C.border}`,
                    borderRadius:12,padding:"10px 12px",cursor:"pointer",textAlign:"left",
                    fontFamily:"inherit",boxShadow:analysisType===a.id?"0 3px 12px rgba(139,53,204,0.25)":"none",
                  }}>
                    <div style={{fontWeight:800,fontSize:12,marginBottom:3}}>{a.label}</div>
                    <div style={{fontSize:10,opacity:0.8}}>{a.desc}</div>
                  </button>
                ))}
              </div>
              <button onClick={runAnalysis} disabled={aiLoading||!apiKey} style={{...mkbtn(aiLoading||!apiKey?C.muted:undefined),opacity:aiLoading||!apiKey?0.5:1,width:"100%",fontSize:15,padding:13}}>
                {aiLoading?"⏳ コンサル脳が分析中...（30〜60秒かかります）":"🚀 深層分析を実行する"}
              </button>
            </div>
            {aiLoading&&<div style={{...card,textAlign:"center",padding:40}}><div style={{fontSize:36,marginBottom:12}}>✦</div><div style={{color:C.purple,fontWeight:700}}>月100万マーケター脳が{posts.length}件の投稿を分析しています...</div></div>}
            {aiResult&&!aiLoading&&(
              <div style={card}>
                <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:14}}>
                  <SectionTitle icon="✅" title="分析レポート" color={C.green}/>
                  <button onClick={()=>{navigator.clipboard.writeText(aiResult);setCopied(true);setTimeout(()=>setCopied(false),2000);}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,padding:"7px 14px",fontSize:12,boxShadow:"none"}}>{copied?"✅ コピー済":"📋 コピー"}</button>
                </div>
                <Mkd text={aiResult}/>
              </div>
            )}
            {!aiResult&&!aiLoading&&<div style={{...card,textAlign:"center",padding:50,background:`linear-gradient(135deg,${C.pinkBg},${C.purpleBg})`}}><div style={{fontSize:48,marginBottom:12}}>🧠</div><div style={{color:C.purple,fontWeight:700}}>分析の種類を選んで実行してください</div><div style={{color:C.muted,fontSize:12,marginTop:8}}>データが多いほど分析精度が上がります</div></div>}
          </div>
        )}

        {tab==="generate"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1.5fr",gap:16}}>
            <div style={card}>
              <SectionTitle icon="✨" title="AI投稿案生成" color={C.orange}/>
              {!apiKey&&<div style={{padding:12,background:C.pinkBg,borderRadius:10,border:`1.5px solid ${C.pink}44`,marginBottom:12,fontSize:12,color:C.pink,fontWeight:700}}>⚠️ 設定タブでAPIキーを入力してください</div>}
              {[["theme","投稿テーマ *","例：ChatGPTで自分のnoteを10分で書く方法"],["cta","CTA（誘導先）","例：プロフィールのnote、dododo ChatGPT"],["product","商品・サービス（任意）","例：dododo ChatGPT、Threads×note収益化教材"]].map(([k,l,ph])=>(
                <div key={k} style={{marginBottom:10}}>
                  <label style={lbl}>{l}</label>
                  <input value={genForm[k]} onChange={e=>setGenForm(f=>({...f,[k]:e.target.value}))} style={inp} placeholder={ph}/>
                </div>
              ))}
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:8,marginBottom:14}}>
                <div><label style={lbl}>フック種類</label>
                  <select value={genForm.tone} onChange={e=>setGenForm(f=>({...f,tone:e.target.value}))} style={{...inp,cursor:"pointer"}}>
                    {HOOK_TYPES.map(h=><option key={h}>{h}</option>)}
                  </select>
                </div>
                <div><label style={lbl}>投稿目的</label>
                  <select value={genForm.goal} onChange={e=>setGenForm(f=>({...f,goal:e.target.value}))} style={{...inp,cursor:"pointer"}}>
                    {["フォロワー増加","note購入促進","エンゲージメント向上","認知拡大","信頼構築"].map(g=><option key={g}>{g}</option>)}
                  </select>
                </div>
              </div>
              <button onClick={generatePosts} disabled={genLoading||!apiKey} style={{...mkbtn(genLoading||!apiKey?C.muted:C.orange),width:"100%",opacity:genLoading||!apiKey?0.5:1,boxShadow:genLoading||!apiKey?"none":"0 4px 14px rgba(240,112,48,0.25)"}}>
                {genLoading?"生成中...":"✨ かおりスタイルで5パターン生成"}
              </button>
              <div style={{marginTop:12,padding:12,background:C.orangeBg,borderRadius:10,fontSize:12,color:C.orange,lineHeight:1.8,fontWeight:600}}>
                🎯 あなたのTOP投稿のトーン・文体を学習して生成します
              </div>
            </div>
            <div>
              {genResult?(
                <div style={card}>
                  <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:12}}>
                    <SectionTitle icon="🎉" title="生成された投稿案" color={C.orange}/>
                    <button onClick={()=>{navigator.clipboard.writeText(genResult);setCopied(true);setTimeout(()=>setCopied(false),2000);}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,padding:"7px 14px",fontSize:12,boxShadow:"none"}}>{copied?"✅ コピー済":"📋 全コピー"}</button>
                  </div>
                  <Mkd text={genResult}/>
                </div>
              ):(
                <div style={{...card,textAlign:"center",padding:50,background:`linear-gradient(135deg,${C.orangeBg},${C.pinkBg})`}}>
                  <div style={{fontSize:48,marginBottom:12}}>✨</div>
                  <div style={{color:C.orange,fontWeight:700}}>テーマを入力して投稿案を生成</div>
                  <div style={{color:C.muted,fontSize:12,marginTop:8}}>あなたの文体を学習した5パターンを生成します</div>
                </div>
              )}
            </div>
          </div>
        )}

        {tab==="sales"&&(
          <div style={{display:"flex",flexDirection:"column",gap:12}}>
            <div style={card}>
              <SectionTitle icon="💰" title="売れた前後分析" color={C.orange}/>
              <p style={{color:C.sub,fontSize:13,lineHeight:1.7}}>note購入数が1以上の投稿を起点に、販売前3日・販売後1.5日の流れを分析します。どんな投稿の後に売れているかがわかります。</p>
              <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:10,marginTop:12}}>
                <div style={{padding:"12px 14px",background:C.goldBg,borderRadius:12,textAlign:"center"}}>
                  <div style={{fontSize:11,color:C.gold,fontWeight:800,marginBottom:6}}>総購入件数</div>
                  <div style={{fontSize:24,fontWeight:900,color:C.gold}}>{stats.totalSales}件</div>
                </div>
                <div style={{padding:"12px 14px",background:C.orangeBg,borderRadius:12,textAlign:"center"}}>
                  <div style={{fontSize:11,color:C.orange,fontWeight:800,marginBottom:6}}>購入ある投稿数</div>
                  <div style={{fontSize:24,fontWeight:900,color:C.orange}}>{stats.saleWindows.length}件</div>
                </div>
                <div style={{padding:"12px 14px",background:C.pinkBg,borderRadius:12,textAlign:"center"}}>
                  <div style={{fontSize:11,color:C.pink,fontWeight:800,marginBottom:6}}>平均note購入率</div>
                  <div style={{fontSize:24,fontWeight:900,color:C.pink}}>{posts.length&&stats.totalClicks?+(stats.totalSales/stats.totalClicks*100).toFixed(1):0}%</div>
                </div>
              </div>
            </div>
            {stats.saleWindows.length===0&&<div style={{...card,textAlign:"center",padding:40,color:C.muted}}>note購入数が入っている投稿がまだありません。<br/>「✍️ 入力」タブでnote購入数を入力してください。</div>}
            {stats.saleWindows.map(w=>(
              <div key={w.salePost.id} style={card}>
                <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start",marginBottom:10}}>
                  <SectionTitle icon="💰" title={`売れた投稿：${w.salePost.date} ${w.salePost.time}`} color={C.orange}/>
                  <div style={{padding:"6px 14px",background:C.orangeBg,borderRadius:20,color:C.orange,fontWeight:900,fontSize:15}}>{w.salePost.noteSales}件購入</div>
                </div>
                <div style={{padding:"10px 14px",background:C.s2,borderRadius:10,fontSize:13,lineHeight:1.7,marginBottom:10}}>{w.salePost.text}</div>
                <div style={{padding:"10px 14px",background:C.goldBg,borderRadius:10,fontSize:13,color:C.gold,fontWeight:700,marginBottom:12}}>💡 {w.insight}</div>
                <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
                  <div>
                    <div style={{fontSize:11,color:C.muted,fontWeight:800,marginBottom:8}}>販売前3日間の投稿</div>
                    {w.before.length?(
                      <div style={{display:"flex",flexDirection:"column",gap:6}}>
                        {w.before.map(p=>(
                          <div key={p.id} style={{padding:"8px 12px",background:C.pinkBg,borderRadius:10,fontSize:12}}>
                            <div style={{color:C.muted,marginBottom:3}}>{p.date} {p.time}</div>
                            <div style={{color:C.text,marginBottom:3}}>{p.text.slice(0,60)}…</div>
                            <div style={{display:"flex",gap:6}}><Badge color={C.pink} bg={C.pinkBg}>{p.role}</Badge><span style={{color:C.purple,fontWeight:700}}>導線{funnelScore(p)}点</span></div>
                          </div>
                        ))}
                      </div>
                    ):<div style={{padding:"8px 12px",background:C.s2,borderRadius:10,fontSize:12,color:C.muted}}>該当なし</div>}
                  </div>
                  <div>
                    <div style={{fontSize:11,color:C.muted,fontWeight:800,marginBottom:8}}>販売後1.5日間の投稿</div>
                    {w.after.length?(
                      <div style={{display:"flex",flexDirection:"column",gap:6}}>
                        {w.after.map(p=>(
                          <div key={p.id} style={{padding:"8px 12px",background:C.purpleBg,borderRadius:10,fontSize:12}}>
                            <div style={{color:C.muted,marginBottom:3}}>{p.date} {p.time}</div>
                            <div style={{color:C.text,marginBottom:3}}>{p.text.slice(0,60)}…</div>
                            <div style={{display:"flex",gap:6}}><Badge color={C.purple} bg={C.purpleBg}>{p.role}</Badge><span style={{color:C.purple,fontWeight:700}}>導線{funnelScore(p)}点</span></div>
                          </div>
                        ))}
                      </div>
                    ):<div style={{padding:"8px 12px",background:C.s2,borderRadius:10,fontSize:12,color:C.muted}}>該当なし</div>}
                  </div>
                </div>
              </div>
            ))}

            <div style={{...card,background:`linear-gradient(135deg,${C.pinkBg},${C.purpleBg})`}}>
              <SectionTitle icon="🎯" title="次に出すべき投稿" color={C.purple}/>
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
                <div>
                  <div style={{padding:"12px 14px",background:"rgba(255,255,255,0.8)",borderRadius:12,marginBottom:10}}>
                    <div style={{fontSize:11,color:C.muted,fontWeight:800,marginBottom:6}}>おすすめ</div>
                    <div style={{fontWeight:900,fontSize:16,color:C.purple}}>{stats.nextRec.hook} × {stats.nextRec.role}</div>
                    <div style={{fontWeight:700,color:C.pink,marginTop:4}}>テーマ：{stats.nextRec.theme}</div>
                  </div>
                  <div style={{padding:"12px 14px",background:"rgba(255,255,255,0.7)",borderRadius:12,fontSize:13,color:C.sub,lineHeight:1.7}}>{stats.nextRec.reason}</div>
                </div>
                <div style={{padding:"14px 16px",background:"rgba(255,255,255,0.9)",borderRadius:12,fontFamily:"sans-serif",fontSize:13,lineHeight:1.9,color:C.text,whiteSpace:"pre-wrap"}}>
                  {stats.nextRec.role==="信頼"?`ChatGPTで発信素材を作る5ステップ\n\n①テーマを決める\n②ChatGPTに構成を出させる\n③自分の言葉で書き直す\n④かわいい画像を添える\n⑤noteへの導線を1行置く\n\n詳しくはプロフィールのnoteに。`:
                  stats.nextRec.role==="導線"?`最近、${stats.nextRec.theme}という質問をよく見ます。\n\nだから、私がやってよかったことをまとめました。\n\n必要であればプロフィールから見てみてください。`:
                  stats.nextRec.role==="レビュー"?`dododo ChatGPT、また購入してくださった方がいました。\n\nありがとうございます。\n\n週末に追記します。使い方も一緒に。`:
                  `これ、当てはまる？\n\n① AIに興味があるが何から始めれば\n② noteを書いているが全然売れない\n③ 発信を続けているのに収益ゼロ\n\nひとつでもあるなら、順番の問題かも。`}
                </div>
              </div>
            </div>
          </div>
        )}

        {tab==="reflection"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1.6fr",gap:16}}>
            <div style={card}>
              <SectionTitle icon="🔄" title="日次/週次 振り返り分析" color={C.purple}/>
              <p style={{color:C.sub,fontSize:12,marginBottom:14,lineHeight:1.7}}>寝稼ぎ式・おさる式・ヒカさん式・3層構造フレーム全部使って振り返ります。</p>
              {!apiKey&&<div style={{padding:10,background:C.pinkBg,borderRadius:10,marginBottom:10,fontSize:12,color:C.pink,fontWeight:700}}>⚠️ 設定タブでAPIキーを入力してください</div>}
              {[["period","振り返り期間","例：2026/5/26（月）一日"],["posts_text","今日投稿した内容","各投稿のフック・時間・数字も書く"],["numbers","数字（インプ・いいね・F増減・noteクリック等）",""],["win_post","一番伸びた投稿",""],["lose_post","反応が弱かった投稿",""],["concern","迷っていること",""]].map(([k,l,ph])=>(
                <div key={k} style={{marginBottom:10}}>
                  <label style={lbl}>{l}</label>
                  <textarea value={reflectForm[k]} onChange={e=>setReflectForm(f=>({...f,[k]:e.target.value}))} style={{...inp,height:65,resize:"vertical"}} placeholder={ph}/>
                </div>
              ))}
              <button onClick={runReflection} disabled={reflectLoading||!apiKey} style={{...mkbtn(reflectLoading||!apiKey?C.muted:C.purple),opacity:reflectLoading||!apiKey?0.5:1,width:"100%"}}>
                {reflectLoading?"⏳ 振り返り分析中...":"🔄 振り返り分析を実行"}
              </button>
              <div style={{marginTop:12,padding:12,background:C.purpleBg,borderRadius:10,fontSize:11,color:C.sub,lineHeight:1.8}}>
                💡 分析項目：総合評価・フック診断・投稿タイプ分類・CTA評価・バズ翌日の橋渡し確認・note導線評価・次の投稿全文・今日の学び一言
              </div>
            </div>
            <div>
              {reflectResult?(
                <div style={card}>
                  <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:14}}>
                    <SectionTitle icon="✅" title="振り返りレポート" color={C.purple}/>
                    <button onClick={()=>{navigator.clipboard.writeText(reflectResult);setCopied(true);setTimeout(()=>setCopied(false),2000);}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,padding:"7px 14px",fontSize:12,boxShadow:"none"}}>{copied?"✅ コピー済":"📋 コピー"}</button>
                  </div>
                  <Mkd text={reflectResult}/>
                </div>
              ):(
                <div style={{...card,textAlign:"center",padding:50,background:`linear-gradient(135deg,${C.purpleBg},${C.pinkBg})`}}>
                  <div style={{fontSize:48,marginBottom:12}}>🔄</div>
                  <div style={{color:C.purple,fontWeight:700}}>左に今日の投稿データを入力して振り返り分析を実行してください</div>
                  <div style={{color:C.muted,fontSize:12,marginTop:12,lineHeight:1.8}}>
                    総合評価 / フック診断 / 投稿タイプ分類<br/>CTA評価 / 橋渡し投稿確認 / note導線評価<br/>次の24時間でやること3つ / 次の投稿全文
                  </div>
                </div>
              )}
            </div>
          </div>
        )}

        {tab==="ghost"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1.5fr",gap:16}}>
            <div style={card}>
              <SectionTitle icon="👻" title="Ghost Reviewer（4視点レビュー）" color={C.purple}/>
              <p style={{color:C.sub,fontSize:12,marginBottom:14,lineHeight:1.7}}>投稿を出す前に4つの立場から同時にリアルなフィードバック。「投稿は伸びるけど売れない」が消えます。</p>
              <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10,marginBottom:14}}>
                {["👴 3年後の自分：ブランドとして正解か","🎯 競合発信者：差別化できているか","🤔 買わなかった客：何が引っかかったか","💚 購入者：信頼残高は上がるか"].map((s,i)=>(
                  <div key={i} style={{padding:"10px 12px",background:C.purpleBg,borderRadius:10,fontSize:12,color:C.sub}}>{s}</div>
                ))}
              </div>
              {!apiKey&&<div style={{padding:10,background:C.pinkBg,borderRadius:10,marginBottom:10,fontSize:12,color:C.pink,fontWeight:700}}>⚠️ 設定タブでAPIキーを入力してください</div>}
              <label style={lbl}>レビューしたい投稿文</label>
              <textarea value={ghostText} onChange={e=>setGhostText(e.target.value)} style={{...inp,height:180,resize:"vertical",marginBottom:12}} placeholder="投稿文をここに貼り付けてください..."/>
              <button onClick={runGhostReview} disabled={ghostLoading||!apiKey} style={{...mkbtn(ghostLoading||!apiKey?C.muted:C.purple),opacity:ghostLoading||!apiKey?0.5:1,width:"100%"}}>
                {ghostLoading?"⏳ 4視点でレビュー中...":"👻 Ghost Reviewを実行"}
              </button>
            </div>
            <div>
              {ghostResult?(
                <div style={card}>
                  <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:14}}>
                    <SectionTitle icon="💡" title="4視点レビュー結果" color={C.purple}/>
                    <button onClick={()=>{navigator.clipboard.writeText(ghostResult);setCopied(true);setTimeout(()=>setCopied(false),2000);}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,padding:"7px 14px",fontSize:12,boxShadow:"none"}}>{copied?"✅ コピー済":"📋 コピー"}</button>
                  </div>
                  <Mkd text={ghostResult}/>
                </div>
              ):(
                <div style={{...card,textAlign:"center",padding:50,background:`linear-gradient(135deg,${C.purpleBg},${C.orangeBg})`}}>
                  <div style={{fontSize:48,marginBottom:12}}>👻</div>
                  <div style={{color:C.purple,fontWeight:700}}>投稿文を貼り付けてGhost Reviewを実行</div>
                  <div style={{color:C.muted,fontSize:12,marginTop:12,lineHeight:1.8}}>
                    4視点同時フィードバック<br/>（寝稼ぎ式AI5技術の最上位テクニック）
                  </div>
                </div>
              )}
            </div>
          </div>
        )}

        {tab==="knowledge"&&(
          <div style={{display:"flex",flexDirection:"column",gap:12}}>
            <div style={{...card,background:`linear-gradient(135deg,${C.pinkBg},${C.purpleBg})`}}>
              <SectionTitle icon="📚" title="統合ナレッジライブラリ（全フレームワーク）" color={C.purple}/>
              <div style={{display:"flex",gap:8,flexWrap:"wrap"}}>
                {[["kaori","🎨 かおり式"],["nekasegi","😴 寝稼ぎ式"],["hooks","🎣 3大フック"],["ai5","🤖 AI5技術"],["layers","📐 3層構造"],["reflect","🔄 振り返り"],["fuku","🌸 ふく式参考"],["fan","💜 ファン化6原理"],["noteStep","📝 noteタイミング"],["influence","👑 影響力編"]].map(([k,l])=>(
                  <button key={k} onClick={()=>setKnowledgeTab(k)} style={{background:knowledgeTab===k?GRAD:"rgba(255,255,255,0.8)",color:knowledgeTab===k?"#fff":C.sub,border:`1.5px solid ${knowledgeTab===k?"transparent":C.border}`,borderRadius:20,padding:"6px 14px",cursor:"pointer",fontSize:12,fontWeight:700,fontFamily:"inherit"}}>{l}</button>
                ))}
              </div>
              {knowledgeTab==="ai5"&&<div style={{marginTop:12,display:"grid",gridTemplateColumns:"repeat(5,1fr)",gap:8}}>{Object.values(MASTER_KNOWLEDGE.aiTechniques).map((tech,i)=><div key={i} style={{padding:"10px 12px",background:"rgba(255,255,255,0.8)",borderRadius:12,border:`1.5px solid ${C.border}`}}><div style={{fontWeight:800,fontSize:12,color:C.purple,marginBottom:5}}>{tech.name}</div><div style={{fontSize:11,color:C.sub,lineHeight:1.6}}>{tech.benefit}</div><div style={{fontSize:10,color:C.muted,marginTop:6,lineHeight:1.5}}>{tech.howto}</div></div>)}</div>}
              {knowledgeTab==="nekasegi"&&<div style={{marginTop:12}}><div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><div><div style={{fontWeight:800,color:C.purple,marginBottom:8}}>ロードマップ</div>{MASTER_KNOWLEDGE.nekasegi.roadmap.map((it,i)=><div key={i} style={{padding:"8px 12px",background:"rgba(255,255,255,0.8)",borderRadius:8,fontSize:12,color:C.sub,marginBottom:4}}>{it}</div>)}</div><div><div style={{fontWeight:800,color:C.orange,marginBottom:8}}>補講</div>{MASTER_KNOWLEDGE.nekasegi.addLectures.map((it,i)=><div key={i} style={{padding:"8px 12px",background:"rgba(255,255,255,0.8)",borderRadius:8,fontSize:12,color:C.sub,marginBottom:4}}>{it}</div>)}</div></div></div>}
              {knowledgeTab==="hooks"&&<div style={{marginTop:12,display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:10}}>{[MASTER_KNOWLEDGE.hookMethods.osaru,MASTER_KNOWLEDGE.hookMethods.nekasegi,MASTER_KNOWLEDGE.hookMethods.hika].map((m,i)=><div key={i} style={{padding:"12px",background:"rgba(255,255,255,0.85)",borderRadius:12}}><div style={{fontWeight:800,color:[C.orange,C.purple,C.pink][i],marginBottom:6}}>{m.name}</div><div style={{fontSize:12,color:C.sub,marginBottom:8}}>{m.core}</div>{(m.examples||m.patterns||[]).slice(0,3).map((ex,j)=><div key={j} style={{padding:"5px 8px",background:C.s2,borderRadius:6,fontSize:11,color:C.sub,marginBottom:3}}>{ex}</div>)}</div>)}</div>}
              {knowledgeTab==="layers"&&<div style={{marginTop:12,display:"grid",gridTemplateColumns:"1fr",gap:8}}>{[{l:"認知層",v:MASTER_KNOWLEDGE.postLayers.recognition,c:C.pink},{l:"信頼層",v:MASTER_KNOWLEDGE.postLayers.trust,c:C.purple},{l:"収益層（導線層）",v:MASTER_KNOWLEDGE.postLayers.funnel,c:C.orange}].map((s,i)=><div key={i} style={{padding:"12px 16px",background:"rgba(255,255,255,0.8)",borderRadius:12,border:`2px solid ${s.c}33`}}><div style={{fontWeight:800,color:s.c,marginBottom:4}}>{s.l}</div><div style={{fontSize:13,color:C.sub}}>{s.v}</div></div>)}<div style={{padding:"12px 16px",background:C.purpleBg,borderRadius:12,fontWeight:800,color:C.purple}}>{MASTER_KNOWLEDGE.postLayers.rule}</div></div>}
              {knowledgeTab==="reflect"&&<div style={{marginTop:12,display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><div>{MASTER_KNOWLEDGE.reflectionFramework.evaluationAxes.map((it,i)=><div key={i} style={{padding:"8px 12px",background:"rgba(255,255,255,0.8)",borderRadius:8,fontSize:12,color:C.sub,marginBottom:4}}><span style={{color:C.pink,fontWeight:900}}>{i+1}. </span>{it}</div>)}</div><div><div style={{padding:"12px",background:"rgba(255,255,255,0.8)",borderRadius:12,marginBottom:8}}><div style={{fontWeight:800,color:C.green,marginBottom:5}}>✅ 勝ちパターン</div><div style={{fontSize:12,color:C.sub}}>{MASTER_KNOWLEDGE.reflectionFramework.winLosePattern.win}</div></div><div style={{padding:"12px",background:"rgba(255,255,255,0.8)",borderRadius:12,marginBottom:8}}><div style={{fontWeight:800,color:C.gold,marginBottom:5}}>⭐ 黄金法則</div><div style={{fontSize:12,color:C.sub}}>{MASTER_KNOWLEDGE.reflectionFramework.winLosePattern.golden}</div></div></div></div>}
              {knowledgeTab==="fuku"&&<div style={{marginTop:12,display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}><div><div style={{padding:"12px 16px",background:"rgba(255,255,255,0.85)",borderRadius:12,marginBottom:8}}><div style={{fontWeight:900,color:C.pink,fontSize:13,marginBottom:8}}>{MASTER_KNOWLEDGE.fukuStyle.coreMessage}</div></div>{MASTER_KNOWLEDGE.fukuStyle.winningPatterns.map((it,i)=><div key={i} style={{padding:"8px 12px",background:"rgba(255,255,255,0.8)",borderRadius:8,fontSize:12,color:C.sub,marginBottom:4}}>{it}</div>)}</div><div>{MASTER_KNOWLEDGE.fukuStyle.ctaExamples.map((it,i)=><div key={i} style={{padding:"8px 12px",background:C.orangeBg,borderRadius:8,fontSize:12,color:C.orange,marginBottom:4,fontWeight:600}}>{it}</div>)}{MASTER_KNOWLEDGE.fukuStyle.avoid.map((it,i)=><div key={i} style={{padding:"8px 12px",background:C.redBg,borderRadius:8,fontSize:12,color:C.sub,marginBottom:4}}>{it}</div>)}</div></div>}

              <div style={{fontWeight:700,fontSize:14,lineHeight:1.8,color:C.text,marginBottom:10}}>{FUKU_KNOWLEDGE.corePosition}</div>
              <div style={{padding:"12px 16px",background:"rgba(255,255,255,0.8)",borderRadius:12}}>
                <div style={{fontSize:11,color:C.muted,fontWeight:800,marginBottom:5}}>メインメッセージ</div>
                <div style={{fontWeight:900,fontSize:16,color:C.purple}}>{FUKU_KNOWLEDGE.mainMessage}</div>
              </div>
            </div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:12}}>
              {[
                {title:"勝ちパターン",icon:"🏆",items:FUKU_KNOWLEDGE.winningPatterns,color:C.pink},
                {title:"フックルール",icon:"🎣",items:FUKU_KNOWLEDGE.hookRules,color:C.orange},
                {title:"note導線フレーズ",icon:"🔗",items:FUKU_KNOWLEDGE.noteBridge,color:C.purple},
                {title:"避けること",icon:"❌",items:FUKU_KNOWLEDGE.avoid,color:C.red},
                {title:"読者の状態",icon:"👤",items:FUKU_KNOWLEDGE.readerStates,color:C.gold},
                {title:"主なリスク",icon:"⚠️",items:FUKU_KNOWLEDGE.risks,color:C.orange},
              ].map((sec,i)=>(
                <div key={i} style={card}>
                  <SectionTitle icon={sec.icon} title={sec.title} color={sec.color}/>
                  <div style={{display:"flex",flexDirection:"column",gap:6}}>
                    {sec.items.map((item,j)=>(
                      <div key={j} style={{padding:"8px 12px",background:C.s2,borderRadius:8,fontSize:13,color:C.sub,lineHeight:1.6}}>{item}</div>
                    ))}
                  </div>

              {knowledgeTab==="fan"&&<div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:10}}>
                {EXTENDED_KNOWLEDGE.fanPrinciples.sixPrinciples.map((p,i)=>(
                  <div key={i} style={{padding:"12px 14px",background:"rgba(255,255,255,0.85)",borderRadius:14,border:`1.5px solid ${C.border}`}}>
                    <div style={{fontWeight:800,fontSize:13,color:C.purple,marginBottom:6}}>原理{p.id}：{p.name}</div>
                    <div style={{fontSize:11,color:C.text,lineHeight:1.7,marginBottom:6}}>{p.core}</div>
                    <div style={{fontSize:10,color:C.accent,background:C.s2,borderRadius:8,padding:"4px 8px"}}>▶ {p.action}</div>
                  </div>
                ))}
                <div style={{gridColumn:"1/-1",padding:"12px 14px",background:C.s2,borderRadius:12,border:`1.5px solid ${C.border}`,fontSize:11,color:C.sub}}>
                  <strong style={{color:C.purple}}>ブランドコア：</strong>{EXTENDED_KNOWLEDGE.fanPrinciples.brandCore}
                </div>
              </div>}
              {knowledgeTab==="noteStep"&&<div>
                <div style={{display:"grid",gridTemplateColumns:"repeat(5,1fr)",gap:8,marginBottom:12}}>
                  {EXTENDED_KNOWLEDGE.noteTimingSteps.fiveSteps.map((s,i)=>(
                    <div key={i} style={{padding:"12px 10px",background:"rgba(255,255,255,0.85)",borderRadius:12,border:`1.5px solid ${C.border}`,textAlign:"center"}}>
                      <div style={{fontWeight:900,fontSize:16,color:C.purple}}>STEP{s.step}</div>
                      <div style={{fontWeight:700,fontSize:11,color:C.text,margin:"4px 0"}}>{s.name}</div>
                      <div style={{fontSize:10,color:C.sub,lineHeight:1.6}}>{s.action}</div>
                    </div>
                  ))}
                </div>
                <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:8}}>
                  {EXTENDED_KNOWLEDGE.noteTimingSteps.badPatterns.map((p,i)=>(
                    <div key={i} style={{padding:"10px 12px",background:C.s2,borderRadius:10,border:`1.5px solid ${C.border}`}}>
                      <div style={{fontWeight:800,fontSize:11,color:"#e74c3c",marginBottom:4}}>❌ {p.name}</div>
                      <div style={{fontSize:10,color:C.sub,marginBottom:4}}>{p.symptom}</div>
                      <div style={{fontSize:10,color:C.accent}}>✅ {p.fix}</div>
                    </div>
                  ))}
                </div>
              </div>}
              {knowledgeTab==="influence"&&<div>
                <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:10,marginBottom:10}}>
                  {EXTENDED_KNOWLEDGE.influenceStrategy.replyTypes.map((r,i)=>(
                    <div key={i} style={{padding:"12px 14px",background:"rgba(255,255,255,0.85)",borderRadius:12,border:`1.5px solid ${C.border}`}}>
                      <div style={{fontWeight:800,fontSize:12,color:C.purple,marginBottom:6}}>{r.name}</div>
                      <div style={{fontSize:11,color:C.text,lineHeight:1.6,marginBottom:6}}>{r.pattern}</div>
                      <div style={{fontSize:10,color:C.accent}}>効果：{r.benefit}</div>
                    </div>
                  ))}
                </div>
                <div style={{padding:"12px 14px",background:C.s2,borderRadius:12,border:`1.5px solid ${C.border}`}}>
                  <div style={{fontWeight:800,fontSize:12,color:C.purple,marginBottom:8}}>距離感の4ルール</div>
                  {EXTENDED_KNOWLEDGE.influenceStrategy.distanceRules.map((r,i)=>(
                    <div key={i} style={{fontSize:11,color:C.sub,marginBottom:4}}>📌 {r}</div>
                  ))}
                </div>
              </div>}
      </div>
              ))}
            </div>
            <div style={card}>
              <SectionTitle icon="🛒" title="商品ラインナップ" color={C.orange}/>
              <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:10}}>
                {Object.entries(FUKU_KNOWLEDGE.productLine).map(([k,v])=>(
                  <div key={k} style={{padding:"12px 14px",background:C.orangeBg,borderRadius:12,border:`1.5px solid ${C.orange}22`}}>
                    <div style={{fontSize:11,color:C.orange,fontWeight:800,marginBottom:5}}>{k}</div>
                    <div style={{fontSize:13,color:C.text,lineHeight:1.6}}>{v}</div>
                  </div>
                ))}
              </div>
            </div>
          </div>
        )}

        {tab==="settings"&&(
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:16,maxWidth:900}}>
            <div>
              <div style={card}>
                <SectionTitle icon="🔑" title="APIキー設定" color={C.purple}/>
                <label style={lbl}>Claude APIキー</label>
                <input type="password" value={apiInput} onChange={e=>setApiInput(e.target.value)} style={{...inp,marginBottom:10,letterSpacing:2}} placeholder="sk-ant-api03-..."/>
                <div style={{padding:12,background:C.goldBg,border:`1.5px solid ${C.gold}44`,borderRadius:10,fontSize:12,color:C.gold,marginBottom:14,lineHeight:1.7,fontWeight:700}}>
                  ⚠️ APIキーは絶対にチャットに貼らないでください。この入力欄に直接入力してください。
                </div>
                <button onClick={saveKey} style={{...mkbtn(),width:"100%"}}>{keySaved?"✅ 保存しました！":"🔑 保存する"}</button>
                {apiKey&&<div style={{marginTop:10,fontSize:12,color:C.green,fontWeight:700}}>✅ 設定済み（{apiKey.slice(0,15)}...）</div>}
              </div>
              <div style={{...card,marginTop:14}}>
                <SectionTitle icon="🗄️" title="データ管理" color={C.orange}/>
                <div style={{color:C.sub,fontSize:13,marginBottom:12}}>{posts.length} 件の投稿データ保存中</div>
                <div style={{display:"flex",gap:8,flexDirection:"column"}}>
                  <button onClick={()=>{if(window.confirm("サンプルデータに戻しますか？"))setPosts(SAMPLE_POSTS);}} style={{...mkbtn(C.purpleBg,C.purple),border:`1.5px solid ${C.border}`,boxShadow:"none",textAlign:"center"}}>サンプルデータに戻す</button>
                  <button onClick={()=>{if(window.confirm("全投稿データを削除しますか？"))setPosts([]);}} style={{...mkbtn(C.redBg,C.red),border:`1.5px solid ${C.red}44`,boxShadow:"none",textAlign:"center"}}>全データ削除</button>
                </div>
              </div>
            </div>
            <div style={card}>
              <SectionTitle icon="👤" title="プロフィール設定" color={C.pink}/>
              <p style={{color:C.sub,fontSize:12,marginBottom:14,lineHeight:1.7}}>入力するとAI分析の精度が大幅に上がります</p>
              {[
                ["goal","収益目標","例：月100万円安定収益"],
                ["product","主な商品・サービス","例：dododo ChatGPT、note有料記事"],
                ["target","ターゲット読者","例：副業したいAI初心者"],
                ["funnel","集客導線","例：Threads→プロフィール→無料note→有料note"],
                ["message","メインメッセージ","例：AIは難しくない。まずやってみよう"],
                ["cta","基本CTA","例：プロフィールのnoteにまとめています"],
              ].map(([k,l,ph])=>(
                <div key={k} style={{marginBottom:10}}>
                  <label style={lbl}>{l}</label>
                  <input value={profile[k]||""} onChange={e=>setProfile(p=>({...p,[k]:e.target.value}))} style={inp} placeholder={ph}/>
                </div>
              ))}
              <button onClick={saveProfile} style={{...mkbtn(C.pink),width:"100%",marginTop:4}}>保存する</button>
            </div>
          </div>
        )}

      </div>
    </div>
  );
}
