<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GemStory（ジェムストーリー）- みんなで創る共創アクセサリー</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* スマホ風コンテナのスタイル */
        body {
            background-color: #f3f4f6;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
        }
        .phone-frame {
            width: 100%;
            max-width: 420px;
            height: 100vh;
            max-height: 844px;
            background-color: #ffffff;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
            display: flex;
            flex-direction: column;
            position: relative;
            overflow: hidden;
        }
        @media (min-width: 421px) {
            .phone-frame {
                border-radius: 40px;
                border: 8px solid #1f2937;
                height: 844px;
            }
        }
    </style>
</head>
<body>

    <div class="phone-frame">
        <!-- ヘッダー -->
        <header class="bg-gradient-to-r from-violet-600 to-indigo-600 text-white p-4 shadow-md flex justify-between items-center z-10">
            <div>
                <h1 class="font-bold text-lg tracking-wider">✨ GemStory</h1>
                <p class="text-[10px] text-violet-200">作家のこだわりを、みんなで磨き上げる</p>
            </div>
            <span class="text-xs bg-white/20 px-2.5 py-1 rounded-full font-medium">共創EC</span>
        </header>

        <!-- メインコンテンツ領域 -->
        <main id="main-content" class="flex-1 overflow-y-auto pb-20">
            <!-- 【画面1：ホーム（商品一覧）】 -->
            <div id="view-home" class="p-4 space-y-4">
                <div class="bg-violet-50 border border-violet-100 rounded-2xl p-4 text-violet-900 shadow-sm">
                    <h2 class="font-bold text-sm">💎 「買う」から「共創する」へ</h2>
                    <p class="text-xs mt-1 text-violet-700 leading-relaxed">仲間と一緒に原石を磨き、限定デザインを完成させよう。共同購入で特別価格に。</p>
                </div>

                <h3 class="font-bold text-gray-800 text-xs tracking-wider uppercase">注目の共創プロジェクト</h3>

                <!-- 商品カード1 -->
                <div class="bg-white border border-gray-100 rounded-2xl shadow-sm overflow-hidden hover:shadow-md transition">
                    <div class="bg-stone-900 h-44 flex items-center justify-center text-4xl relative">
                        💍
                        <span class="absolute top-3 left-3 text-[10px] bg-amber-400 text-stone-900 font-bold px-2 py-0.5 rounded-full">残り2人で成立</span>
                    </div>
                    <div class="p-4 space-y-3">
                        <div>
                            <span class="text-[10px] text-violet-600 font-bold bg-violet-50 px-2 py-0.5 rounded-md">Atelier Lumière 作</span>
                            <h4 class="font-bold text-gray-800 text-sm mt-1">月夜の雫 琥珀ガラスリング</h4>
                            <p class="text-[11px] text-gray-500 mt-0.5 line-clamp-2">「深海の青と夕暮れの琥珀を閉じ込めました。みんなでクロスで磨き上げて輝きを最高潮に！」</p>
                        </div>
                        <div class="flex justify-between items-end pt-2 border-t border-gray-50">
                            <div>
                                <span class="text-xs text-gray-400 line-through">通常 ¥4,800</span>
                                <div class="text-violet-600 font-bold text-base">共同価格 ¥2,400</div>
                            </div>
                            <button onclick="startGroup('月夜の雫 琥珀ガラスリング', 'Atelier Lumière', 4800, 2400)" class="bg-gradient-to-r from-violet-600 to-indigo-600 text-white text-xs font-bold px-4 py-2.5 rounded-xl shadow hover:opacity-90 active:scale-95 transition">
                                プロジェクトに参加
                            </button>
                        </div>
                    </div>
                </div>

                <!-- 商品カード2 -->
                <div class="bg-white border border-gray-100 rounded-2xl shadow-sm overflow-hidden hover:shadow-md transition">
                    <div class="bg-stone-900 h-44 flex items-center justify-center text-4xl relative">
                        💎
                        <span class="absolute top-3 left-3 text-[10px] bg-amber-400 text-stone-900 font-bold px-2 py-0.5 rounded-full">残り1人で成立</span>
                    </div>
                    <div class="p-4 space-y-3">
                        <div>
                            <span class="text-[10px] text-violet-600 font-bold bg-violet-50 px-2 py-0.5 rounded-md">SilverCraft Miki 作</span>
                            <h4 class="font-bold text-gray-800 text-sm mt-1">星屑のシルバーネックレス</h4>
                            <p class="text-[11px] text-gray-500 mt-0.5 line-clamp-2">「職人が一つずつ削り出した純銀ベース。みんなで仕上げのポリッシュを行って特別仕様に。」</p>
                        </div>
                        <div class="flex justify-between items-end pt-2 border-t border-gray-50">
                            <div>
                                <span class="text-xs text-gray-400 line-through">通常 ¥6,200</span>
                                <div class="text-violet-600 font-bold text-base">共同価格 ¥3,100</div>
                            </div>
                            <button onclick="startGroup('星屑のシルバーネックレス', 'SilverCraft Miki', 6200, 3100)" class="bg-gradient-to-r from-violet-600 to-indigo-600 text-white text-xs font-bold px-4 py-2.5 rounded-xl shadow hover:opacity-90 active:scale-95 transition">
                                プロジェクトに参加
                            </button>
                        </div>
                    </div>
                </div>
            </div>

            <!-- 【画面2：育成・共創（磨く機能）】 -->
            <div id="view-grow" class="p-4 space-y-4 hidden">
                <div class="text-center space-y-1 py-1">
                    <span class="text-[10px] bg-violet-100 text-violet-700 font-bold px-3 py-1 rounded-full">✨ 共同磨き上げプロジェクト進行中</span>
                    <h2 id="current-item-title" class="font-bold text-gray-800 text-base pt-1">月夜の雫 琥珀ガラスリング</h2>
                    <p id="current-author" class="text-xs text-violet-600 font-medium">Atelier Lumière</p>
                </div>

                <!-- 育成・磨きビジュアルエリア -->
                <div class="bg-gradient-to-b from-stone-900 to-slate-900 rounded-3xl p-6 text-white text-center relative overflow-hidden shadow-inner border border-stone-800">
                    <div id="gem-icon" class="text-6xl my-4 transition-transform duration-300 transform scale-100">
                        ✨💍✨
                    </div>
                    <div class="text-xs text-amber-300 font-semibold mb-2">輝き度合 (ポリッシュ): <span id="progress-text">40</span>%</div>
                    
                    <!-- プログレスバー -->
                    <div class="w-full bg-stone-800 h-3 rounded-full overflow-hidden p-0.5 border border-stone-700">
                        <div id="progress-bar" class="bg-gradient-to-r from-amber-400 to-violet-400 h-full rounded-full transition-all duration-300" style="width: 40%;"></div>
                    </div>

                    <p id="status-message" class="text-[11px] text-stone-300 mt-3 leading-relaxed">あと2人の参加、または「クロスで磨く」で輝きがアップ！100%で作家への正式オーダーが確定します。</p>
                </div>

                <!-- 磨くアクションボタン -->
                <button onclick="polishGem()" class="w-full bg-gradient-to-r from-violet-600 to-indigo-600 text-white font-bold py-3.5 rounded-2xl shadow-md hover:opacity-90 active:scale-95 transition flex items-center justify-center gap-2 text-sm">
                    🧽 ジュエリークロスで磨く (+15%)
                </button>

                <!-- 友達へのシェアセクション -->
                <div class="bg-violet-50/60 border border-violet-100 rounded-2xl p-4 space-y-3">
                    <h3 class="font-bold text-xs text-violet-900">💬 仲間を招待して一緒に磨き上げよう！</h3>
                    <div class="flex gap-2">
                        <input type="text" readonly value="https://gemstory.app/invite?project=xyz999" class="bg-white border border-violet-200 text-xs px-3 py-2 rounded-xl flex-1 text-gray-600 outline-none">
                        <button onclick="copyLink()" class="bg-violet-600 text-white text-xs font-bold px-4 py-2 rounded-xl hover:bg-violet-700 transition">URLコピー</button>
                    </div>
                </div>
            </div>

            <!-- 【画面3：マイページ】 -->
            <div id="view-mypage" class="p-4 space-y-4 hidden">
                <div class="bg-white border border-gray-100 rounded-2xl p-4 flex items-center gap-3 shadow-sm">
                    <div class="w-12 h-12 bg-violet-100 rounded-full flex items-center justify-center text-xl text-violet-700 font-bold">
                        💎
                    </div>
                    <div>
                        <h3 class="font-bold text-gray-800 text-sm">ゲストユーザー</h3>
                        <p class="text-xs text-gray-400">参加プロジェクト: 1件</p>
                    </div>
                </div>

                <div class="bg-white border border-gray-100 rounded-2xl p-4 space-y-3 shadow-sm">
                    <h3 class="font-bold text-gray-800 text-xs">参加中の共創プロジェクト</h3>
                    <div class="border-l-4 border-violet-600 pl-3 py-1">
                        <div class="font-bold text-xs text-gray-800">月夜の雫 琥珀ガラスリング</div>
                        <div class="text-[11px] text-gray-500">作家：Atelier Lumière / 輝き度 40%</div>
                    </div>
                </div>

                <div class="bg-white border border-gray-100 rounded-2xl p-4 space-y-3 shadow-sm">
                    <h3 class="font-bold text-gray-800 text-xs">成立したオーダー・作家への通知</h3>
                    <p class="text-xs text-gray-400">現在成立しているオーダーはありません。</p>
                </div>
            </div>
        </main>

        <!-- ボトムナビゲーション -->
        <nav class="absolute bottom-0 left-0 right-0 bg-white border-t border-gray-200 flex justify-around py-3 z-20 shadow-lg">
            <button onclick="switchTab('home')" id="nav-home" class="flex flex-col items-center text-violet-600 transition">
                <span class="text-lg">🏠</span>
                <span class="text-[10px] font-bold mt-1">ホーム</span>
            </button>
            <button onclick="switchTab('grow')" id="nav-grow" class="flex flex-col items-center text-gray-400 transition">
                <span class="text-lg">🧽</span>
                <span class="text-[10px] font-bold mt-1">磨く・共創</span>
            </button>
            <button onclick="switchTab('mypage')" id="nav-mypage" class="flex flex-col items-center text-gray-400 transition">
                <span class="text-lg">👤</span>
                <span class="text-[10px] font-bold mt-1">マイページ</span>
            </button>
        </nav>
    </div>

    <script>
        let progress = 40;

        function switchTab(tabName) {
            document.getElementById('view-home').classList.add('hidden');
            document.getElementById('view-grow').classList.add('hidden');
            document.getElementById('view-mypage').classList.add('hidden');

            document.getElementById('nav-home').className = "flex flex-col items-center text-gray-400 transition";
            document.getElementById('nav-grow').className = "flex flex-col items-center text-gray-400 transition";
            document.getElementById('nav-mypage').className = "flex flex-col items-center text-gray-400 transition";

            document.getElementById('view-' + tabName).classList.remove('hidden');
            document.getElementById('nav-' + tabName).className = "flex flex-col items-center text-violet-600 transition";
        }

        function startGroup(title, author, normalPrice, groupPrice) {
            document.getElementById('current-item-title').innerText = title;
            document.getElementById('current-author').innerText = author;
            switchTab('grow');
        }

        function polishGem() {
            progress += 15;
            if (progress > 100) progress = 100;

            document.getElementById('progress-bar').style.width = progress + '%';
            document.getElementById('progress-text').innerText = progress;

            const icon = document.getElementById('gem-icon');
            icon.classList.add('scale-125');
            setTimeout(() => icon.classList.remove('scale-125'), 200);

            if (progress === 100) {
                document.getElementById('status-message').innerText = "🎉 輝き度が100%になりました！共創プロジェクト成立です！作家へ制作依頼が通知されました。";
                document.getElementById('status-message').className = "text-[11px] text-amber-300 font-bold mt-3 leading-relaxed";
            }
        }

        function copyLink() {
            alert("共創プロジェクトの招待リンクをコピーしました！友達にシェアして一緒に磨いてもらおう！");
        }
    </script>
</body>
</html>
