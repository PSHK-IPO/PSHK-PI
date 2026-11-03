<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
  <title>PSHK 專業投資者認證 - Optimized Flow</title>
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; background: #f0f2f5; color: #111; font-size: 14px; line-height: 1.55; }
    .app { max-width: 480px; margin: 0 auto; background: #fff; min-height: 100vh; position: relative; box-shadow: 0 0 24px rgba(0,0,0,0.08); }
    header { background: #111; color: #fff; padding: 12px 16px; font-size: 16px; font-weight: 600; display: flex; align-items: center; justify-content: space-between; position: sticky; top: 0; z-index: 20; }
    header .back { font-size: 22px; cursor: pointer; padding: 4px 8px; line-height: 1; }
    .progress { height: 3px; background: #e5e7eb; }
    .progress-bar { height: 100%; background: #111; transition: width 0.25s ease; }
    .screen { display: none; padding: 20px 16px 120px; }
    .screen.active { display: block; }
    h2 { font-size: 18px; font-weight: 600; margin-bottom: 14px; }
    h3 { font-size: 15px; margin: 16px 0 8px; }
    p { margin-bottom: 10px; }
    ul { margin: 8px 0 12px 18px; }
    li { margin-bottom: 4px; }
    .card { background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 12px; padding: 14px; margin: 12px 0; }
    .btn-group { position: fixed; bottom: 0; left: 0; right: 0; max-width: 480px; margin: 0 auto; background: #fff; padding: 12px 16px 24px; display: flex; gap: 10px; box-shadow: 0 -4px 16px rgba(0,0,0,0.06); z-index: 30; }
    .btn { flex: 1; padding: 14px; border-radius: 28px; font-size: 15px; font-weight: 600; border: none; cursor: pointer; }
    .btn-primary { background: #111; color: #fff; }
    .btn-secondary { background: #fff; color: #111; border: 1.5px solid #d1d5db; }
    .btn:disabled { background: #9ca3af; color: #fff; cursor: not-allowed; }
    label { display: flex; align-items: flex-start; gap: 10px; margin: 12px 0; font-size: 14px; }
    input[type="radio"], input[type="checkbox"] { margin-top: 3px; accent-color: #111; width: 18px; height: 18px; flex-shrink: 0; }
    input[type="tel"], input[type="text"] { width: 100%; padding: 12px 14px; border: 1.5px solid #d1d5db; border-radius: 10px; font-size: 15px; margin-top: 6px; }
    .value { font-size: 24px; font-weight: 700; margin: 6px 0; color: #111; }
    .note { font-size: 12px; color: #6b7280; }
    .tag { display: inline-block; background: #e0f2fe; color: #0369a1; font-size: 11px; padding: 2px 8px; border-radius: 20px; margin-left: 6px; }
    .rep-card { display: flex; align-items: center; gap: 12px; background: #f8fafc; border-radius: 12px; padding: 12px; margin-bottom: 14px; border: 1px solid #e2e8f0; }
    .consent-scroll { max-height: 220px; overflow-y: auto; border: 1.5px solid #e5e7eb; border-radius: 10px; padding: 14px; background: #f9fafb; font-size: 13px; margin: 12px 0; }
    .otp-box { display: flex; gap: 8px; justify-content: center; margin: 18px 0; }
    .otp-box input { width: 42px; height: 48px; text-align: center; font-size: 20px; border: 1.5px solid #d1d5db; border-radius: 10px; }
    .otp-error { color: #dc2626; font-size: 13px; text-align: center; margin-top: 8px; display: none; }
    .review-item { display: flex; justify-content: space-between; padding: 10px 0; border-bottom: 1px solid #f1f5f9; font-size: 13px; }
    .review-item:last-child { border-bottom: none; }
    .status-icon { font-size: 48px; text-align: center; margin: 24px 0 12px; }
  </style>
</head>
<body>
<div class="app">
  <header>
    <span class="back" id="headerBack">←</span>
    <span>專業投資者認證</span>
    <span style="width:28px"></span>
  </header>
  <div class="progress"><div class="progress-bar" id="progressBar" style="width:8%"></div></div>

  <!-- 0. Entry Points -->
  <div class="screen active" id="s0">
    <h2>0. 專業投資者介紹</h2>
    <div class="card">
      <p><strong>什麼是專業投資者？</strong></p>
      <p>根據《證券及期貨條例》，個人專業投資者需持有 <strong>Net Portfolio ≥ HKD 8,000,000</strong>（或等值外幣）。</p>
      <p><strong>可計算項目</strong>：證券、現金、存款證（由保管人持有）</p>
      <p><strong>不計算項目</strong>：物業、私人公司股份、保險、非證券加密貨幣、無抵押債務</p>
      <p class="note">系統會自動加載您現有的戶口資料（個人 / 聯名 / 法團）。</p>
    </div>
    <div class="btn-group">
      <button class="btn btn-primary" onclick="go(1)">立即認證</button>
    </div>
  </div>

  <!-- 1. Education -->
  <div class="screen" id="s1">
    <h2>1. 合規告知與免責宣導</h2>
    <div class="card">
      <p><strong>門檻</strong><br>Net Portfolio ≥ <strong>HKD 8,000,000</strong>（總市值扣除 margin / share-pledge 貸款後的淨值）</p>
      <p><strong>保障變更公告</strong><br>成為個人專業投資者後，適合性義務（Suitability）仍然適用。僅《操守準則》第 15.5 段的部分要求可獲豁免。</p>
      <p><strong>可計算 vs 不計算</strong><br>可計算：證券、現金、CD<br>不計算：房產、非證券加密貨幣、私人公司股份</p>
    </div>
    <div class="card">
      <p class="note">如有疑問，可預約持牌代表電話解釋。</p>
      <button class="btn btn-secondary" style="margin-top:8px;" onclick="alert('已記錄回撥請求（示範）')">一鍵預約電話回撥</button>
    </div>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(0)">上一步</button>
      <button class="btn btn-primary" onclick="go(2)">下一步</button>
    </div>
  </div>

  <!-- 2. Eligibility Self-check -->
  <div class="screen" id="s2">
    <h2>2. 客戶身分初篩</h2>
    <div class="card">
      <label><input type="radio" name="ctype" value="individual" checked> 個人 / 聯名帳戶</label>
      <label><input type="radio" name="ctype" value="corporate"> 法團 / 合夥 / 信託</label>
    </div>
    <div class="card" id="jointBox">
      <p><strong>聯名帳戶處理</strong></p>
      <label><input type="checkbox"> 包含與配偶或子女的聯名帳戶（可合併計算）</label>
      <label><input type="checkbox"> 包含與非關聯人的聯名帳戶（需確認份額）</label>
    </div>
    <p class="note">此步驟僅作引導，最終以資產證明為準。</p>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(1)">上一步</button>
      <button class="btn btn-primary" onclick="go(3)">下一步</button>
    </div>
  </div>

  <!-- 3. Choose Path -->
  <div class="screen" id="s3">
    <h2>3. 選擇認證路徑</h2>
    <div class="card">
      <label>
        <input type="radio" name="path" value="A" checked>
        <div>
          <strong>Path A – 輝立內部資產即時核驗</strong> <span class="tag">最快</span><br>
          <span class="note">系統自動計算 Net Portfolio，扣除內部 margin / 質押貸款</span>
        </div>
      </label>
      <label style="margin-top:16px;">
        <input type="radio" name="path" value="B">
        <div>
          <strong>Path B – 上載外部資產證明</strong><br>
          <span class="note">銀行/證券結單、CPA 證書、公開檔案（近 12 個月）</span>
        </div>
      </label>
    </div>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(2)">上一步</button>
      <button class="btn btn-primary" onclick="choosePath()">下一步</button>
    </div>
  </div>

  <!-- 4A. Path A -->
  <div class="screen" id="s4a">
    <h2>4A. 內部資產即時核驗</h2>
    <div class="card">
      <p>系統計算的 <strong>Net Portfolio</strong></p>
      <div class="value">HKD 9,420,000</div>
      <p class="note">
        估值日期：2026-10-31<br>
        已自動扣除內部 Margin 欠款與質押借貸<br>
        外幣已按當日收盤價折算（Cap. 571D s.2A）
      </p>
    </div>
    <label><input type="checkbox" id="confirmA"> 本人確認以上 Net 價值正確</label>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(3)">上一步</button>
      <button class="btn btn-primary" id="btn4a" disabled onclick="go(5)">下一步</button>
    </div>
  </div>

  <!-- 4B. Path B -->
  <div class="screen" id="s4b">
    <h2>4B. 上載外部資產證明</h2>
    <div class="card">
      <p><strong>接受文件</strong></p>
      <ul>
        <li>銀行 / 證券 / 信託結單（近 12 個月，建議近 3 個月）</li>
        <li>CPA / 核數師證明書</li>
        <li>公開檔案</li>
        <li>法團 / 信託可提供 16 個月內審計財務報告</li>
      </ul>
      <p class="note">必須清晰顯示：客戶姓名、發行機構、合格資產、有效日期。不接受局部截圖。</p>
    </div>
    <div class="card" style="text-align:center; color:#6b7280; padding:28px; border-style:dashed;">
      點擊上載文件<br>
      <span class="note">支援 PDF、JPG、PNG</span>
    </div>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(3)">上一步</button>
      <button class="btn btn-primary" onclick="go(5)">下一步</button>
    </div>
  </div>

  <!-- 5. 15.3B Risk Disclosure -->
  <div class="screen" id="s5">
    <h2>5. 法定風險與豁免後果揭示</h2>
    <div class="rep-card">
      <div style="width:48px;height:48px;border-radius:50%;background:#e5e7eb;display:flex;align-items:center;justify-content:center;font-size:20px;">👤</div>
      <div>
        <div style="font-weight:600;">持牌代表: [TO INSERT]</div>
        <div class="note">牌照號: [TO INSERT]</div>
      </div>
    </div>

    <div class="consent-scroll" id="consentScroll">
      <p><strong>成為個人專業投資者後的主要變更</strong></p>
      <p>本公司可獲豁免履行《操守準則》第 15.5 段及《成交單據規則》中的部分要求，包括：</p>
      <ul>
        <li>無需提供有關本公司業務及僱員身份與受僱狀況的資料（para 8.1）</li>
        <li>無需盡快確認交易重點（para 8.2）</li>
        <li>無需提供納斯達克－美國證券交易所試驗計劃的資料文件</li>
        <li>無需提供《成交單據規則》所要求的成交單據、戶口結單或收據</li>
      </ul>
      <p>適合性義務及其他第 15.5 段以外的規定仍然適用。</p>
      <p>您可隨時以書面通知撤回專業投資者身份，目前通知期為 <strong>10 個營業日</strong>。</p>
      <p style="margin-top:12px; color:#9ca3af; font-size:12px;">（請滑動至底部以啟用同意框）</p>
    </div>

    <label><input type="checkbox" class="cbox" disabled> 我已完全理解 15.3B 披露之風險與免除法定保護的後果</label>
    <label><input type="checkbox" class="cbox" disabled> 我自願接受專業投資者身份</label>
    <label><input type="checkbox" class="cbox" disabled> 我確認知悉可隨時以書面撤回此身份或變更適用範圍</label>

    <div class="btn-group">
      <button class="btn btn-secondary" onclick="goBackToPath()">上一步</button>
      <button class="btn btn-primary" id="btn5" disabled onclick="go(6)">下一步</button>
    </div>
  </div>

  <!-- 6. Review + OTP -->
  <div class="screen" id="s6">
    <h2>6. 申請摘要與電子驗證</h2>

    <div class="card">
      <p style="font-weight:600; margin-bottom:8px;">申請摘要</p>
      <div class="review-item"><span>客戶類型</span><span id="revType">個人 / 聯名</span></div>
      <div class="review-item"><span>認證路徑</span><span id="revPath">Path A</span></div>
      <div class="review-item"><span>估值方式</span><span>Net Portfolio</span></div>
      <div class="review-item"><span>同意狀態</span><span>已同意（3 項）</span></div>
    </div>

    <div class="card">
      <p style="font-weight:600;">手機號碼</p>
      <input type="tel" id="phoneInput" placeholder="+852 請輸入手機號碼" value="+852 6012 3456">
      <p class="note" style="margin-top:6px;">驗證碼將發送至此號碼（聯名帳戶各持有人需各自驗證）</p>
    </div>

    <div class="card">
      <p style="font-weight:600;">輸入驗證碼</p>
      <p class="note">測試驗證碼：<strong>123456</strong></p>
      <div class="otp-box">
        <input maxlength="1" class="otp" oninput="moveOtp(this,0)">
        <input maxlength="1" class="otp" oninput="moveOtp(this,1)">
        <input maxlength="1" class="otp" oninput="moveOtp(this,2)">
        <input maxlength="1" class="otp" oninput="moveOtp(this,3)">
        <input maxlength="1" class="otp" oninput="moveOtp(this,4)">
        <input maxlength="1" class="otp" oninput="moveOtp(this,5)">
      </div>
      <div class="otp-error" id="otpError">驗證碼不正確，請重新輸入</div>
      <p style="text-align:center; margin-top:12px;">
        <a href="#" onclick="resendOtp();return false;" style="color:#111; font-size:13px;">重新發送驗證碼</a>
      </p>
    </div>

    <div class="card">
      <label><input type="checkbox" id="truthCheck"> 本人確認申報資料真實，若有變更將主動匯報。輝立保留最終拒絕權。</label>
    </div>

    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(5)">上一步</button>
      <button class="btn btn-primary" onclick="verifyOtp()">提交申請</button>
    </div>
  </div>

  <!-- 7. Status Centre -->
  <div class="screen" id="s7">
    <div class="status-icon">📄</div>
    <h2 style="text-align:center;">申請已提交</h2>
    <div class="card">
      <p><strong>參考編號</strong>：PI-20261103-00821</p>
      <p><strong>路徑</strong>：<span id="finalPath">A</span></p>
      <p><strong>狀態</strong>：Under Review</p>
      <p class="note">
        SLA：Path A 接近即時核准；Path B 一般 1 個工作天內完成人工審批。
      </p>
    </div>
    <div class="btn-group">
      <button class="btn btn-secondary" onclick="go(3)">Need more info → 返回路徑</button>
      <button class="btn btn-primary" onclick="go(8)">模擬審批通過</button>
    </div>
  </div>

  <!-- 8. Post-Approval -->
  <div class="screen" id="s8">
    <div class="status-icon">✅</div>
    <h2 style="text-align:center;">認證成功</h2>
    <div class="card">
      <p>• 專業投資者產品已即時解鎖</p>
      <p>• 系統已安排 12 個月後重新確認提醒</p>
      <p>• 帳戶設定內可隨時申請撤回身份（10 個營業日通知期）</p>
      <p>• 過期後重新認證可自動預填歷史資料</p>
    </div>
    <div class="btn-group">
      <button class="btn btn-primary" onclick="location.reload()">完成</button>
    </div>
  </div>
</div>

<script>
  let current = 0;
  let path = 'A';
  const totalSteps = 8;

  function go(n) {
    document.querySelectorAll('.screen').forEach(el => el.classList.remove('active'));
    const target = document.getElementById('s' + n);
    if (!target) return;
    target.classList.add('active');
    current = n;
    document.getElementById('progressBar').style.width = Math.min((n / totalSteps) * 100, 100) + '%';
    window.scrollTo(0, 0);

    if (n === 6) {
      document.getElementById('revPath').textContent = path === 'A' ? 'Path A（內部資產）' : 'Path B（上載證明）';
      const ctype = document.querySelector('input[name="ctype"]:checked')?.value;
      document.getElementById('revType').textContent = ctype === 'corporate' ? '法團 / 合夥 / 信託' : '個人 / 聯名';
    }
    if (n === 7) {
      document.getElementById('finalPath').textContent = path === 'A' ? 'Path A' : 'Path B';
    }
  }

  function choosePath() {
    path = document.querySelector('input[name="path"]:checked').value;
    if (path === 'A') go('4a');
    else go('4b');
  }

  function goBackToPath() {
    go(3);
  }

  // Header back
  document.getElementById('headerBack').onclick = function () {
    if (current === '4a' || current === '4b') go(3);
    else if (current === 5) goBackToPath();
    else if (typeof current === 'number' && current > 0) go(current - 1);
  };

  // Path A confirm
  document.getElementById('confirmA').addEventListener('change', function (e) {
    document.getElementById('btn4a').disabled = !e.target.checked;
  });

  // Consent boxes – only enable after scroll to bottom
  const scrollBox = document.getElementById('consentScroll');
  const cboxes = document.querySelectorAll('.cbox');
  const btn5 = document.getElementById('btn5');

  scrollBox.addEventListener('scroll', function () {
    if (scrollBox.scrollTop + scrollBox.clientHeight >= scrollBox.scrollHeight - 20) {
      cboxes.forEach(cb => cb.disabled = false);
    }
  });

  cboxes.forEach(cb => {
    cb.addEventListener('change', function () {
      const all = [...cboxes].every(c => c.checked);
      btn5.disabled = !all;
    });
  });

  // OTP
  function moveOtp(el, idx) {
    if (el.value && idx < 5) {
      const next = el.nextElementSibling;
      if (next) next.focus();
    }
  }

  function verifyOtp() {
    const code = [...document.querySelectorAll('.otp')].map(i => i.value).join('');
    const truth = document.getElementById('truthCheck').checked;
    if (!truth) {
      alert('請勾選資料真實性聲明');
      return;
    }
    if (code === '123456') {
      document.getElementById('otpError').style.display = 'none';
      go(7);
    } else {
      document.getElementById('otpError').style.display = 'block';
    }
  }

  function resendOtp() {
    document.getElementById('otpError').style.display = 'none';
    document.querySelectorAll('.otp').forEach(i => i.value = '');
    alert('驗證碼已重新發送（測試碼仍為 123456）');
  }
</script>
</body>
</html>
