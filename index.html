<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Refiner Pro: Albion Edition</title>
    <style>
        :root {
            --gold: #f1c40f;
            --green: #2ecc71;
            --red: #e74c3c;
            --bg: #121212;
            --card-bg: #1e1e1e;
        }

        body { 
            background: var(--bg); 
            color: #eee; 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            direction: rtl; 
            padding: 10px;
            margin: 0;
            display: flex;
            justify-content: center;
        }

        .card { 
            background: var(--card-bg); 
            border-radius: 20px; 
            padding: 20px; 
            width: 100%;
            max-width: 500px; 
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            border: 1px solid #333;
        }

        .header { text-align: center; margin-bottom: 25px; }
        h2 { color: var(--gold); margin: 0; font-size: 1.5rem; }
        small { color: #888; }

        .section-title { 
            font-size: 0.85rem; 
            color: var(--gold); 
            margin: 20px 0 10px; 
            padding-bottom: 5px; 
            border-bottom: 1px solid #333;
        }

        .input-grid { 
            display: grid; 
            grid-template-columns: 1fr 1fr; 
            gap: 15px; 
        }

        .input-group { margin-bottom: 15px; }
        label { display: block; font-size: 0.75rem; color: #bbb; margin-bottom: 5px; }

        input, select { 
            width: 100%; 
            padding: 12px; 
            background: #252525; 
            border: 1px solid #444; 
            border-radius: 10px; 
            color: var(--green); 
            font-weight: bold; 
            box-sizing: border-box;
            font-size: 1rem;
        }

        input:focus { border-color: var(--gold); outline: none; }

        .result-card { 
            background: #000; 
            border-radius: 15px; 
            padding: 20px; 
            margin-top: 25px; 
            border: 2px solid var(--gold);
        }

        .res-item { 
            display: flex; 
            justify-content: space-between; 
            align-items: center; 
            margin-bottom: 10px; 
        }

        .profit-val { font-size: 1.6rem; font-weight: 900; }
        #roiVal { font-weight: bold; }
        .roi-good { color: var(--green); }
        .roi-bad { color: var(--red); }
    </small>
    </style>
</head>
<body>

<div class="card">
    <div class="header">
        <h2>Refiner Pro: Albion Edition ⚔️</h2>
        <small>تحليل الموارد والأرباح الاحترافي</small>
    </div>

    <div class="section-title">📦 إعدادات المورد (Resource Tier)</div>
    <div class="input-grid">
        <div class="input-group">
            <label>المستوى (Tier):</label>
            <select id="tier" onchange="calculate()">
                <option value="4">Tier 4 (2 raw)</option>
                <option value="5">Tier 5 (3 raw)</option>
                <option value="6">Tier 6 (4 raw)</option>
                <option value="7">Tier 7 (5 raw)</option>
                <option value="8">Tier 8 (5 raw)</option>
            </select>
        </div>
        <div class="input-group">
            <label>التطوير (Enchant):</label>
            <select id="enchant" onchange="calculate()">
                <option value="0">.0</option>
                <option value="1">.1</option>
                <option value="2">.2</option>
                <option value="3">.3</option>
                <option value="4">.4</option>
            </select>
        </div>
    </div>

    <div class="section-title">💸 أسعار السوق (Market Prices)</div>
    <div class="input-grid">
        <div class="input-group">
            <label>سعر الخام (Raw):</label>
            <input type="number" id="rawPrice" value="150" oninput="calculate()">
        </div>
        <div class="input-group">
            <label>سعر الـ (Tier - 1):</label>
            <input type="number" id="prevRefined" value="50" oninput="calculate()">
        </div>
    </div>
    <div class="input-group">
        <label>سعر بيع المنتج النهائي:</label>
        <input type="number" id="sellPrice" value="1000" oninput="calculate()">
    </div>

    <div class="section-title">⚙️ الضرائب والمكافآت</div>
    <div class="input-grid">
        <div class="input-group">
            <label>ضريبة المحطة (Fee):</label>
            <input type="number" id="stationFee" value="500" oninput="calculate()">
        </div>
        <div class="input-grid">
            <div class="input-group">
                <label>ضريبة السوق:</label>
                <select id="marketTax" onchange="calculate()">
                    <option value="0.04">Premium (4%)</option>
                    <option value="0.08">No Premium (8%)</option>
                </select>
            </div>
        </div>
    </div>

    <div class="input-group">
        <label>مكان التكرير / فوكس:</label>
        <select id="rrr" onchange="calculate()">
            <option value="0.152">مدينة عادية (15.2%)</option>
            <option value="0.367" selected>المدينة المناسبة (36.7%)</option>
            <option value="0.539">المدينة المناسبة + Focus (53.9%)</option>
        </select>
    </div>

    <div id="resultBox" class="result-card">
        <div class="res-item">
            <span>صافي الربح:</span>
            <span id="totalProfit" class="profit-val">0</span>
        </div>
        <div class="res-item">
            <span>العائد على الاستثمار (ROI):</span>
            <span id="roiVal">0%</span>
        </div>
        <div class="res-item">
            <span>تكلفة القطعة الواحدة:</span>
            <span id="unitCost">0</span>
        </div>
    </div>
</div>

<script>
function calculate() {
    const tier = parseInt(document.getElementById('tier').value);
    const rawPrice = parseFloat(document.getElementById('rawPrice').value) || 0;
    const prevRefined = parseFloat(document.getElementById('prevRefined').value) || 0;
    const sellPrice = parseFloat(document.getElementById('sellPrice').value) || 0;
    const rrr = parseFloat(document.getElementById('rrr').value);
    const stationFee = parseFloat(document.getElementById('stationFee').value) || 0;
    const marketTax = parseFloat(document.getElementById('marketTax').value);

    let rawNeeded = 2;
    if (tier === 5) rawNeeded = 3;
    if (tier === 6) rawNeeded = 4;
    if (tier >= 7) rawNeeded = 5;

    const baseResourceCost = (rawPrice * rawNeeded) + prevRefined;
    const nutritionTable = { 4: 22, 5: 44, 6: 88, 7: 176, 8: 352 };
    const feeCost = (stationFee / 100) * (nutritionTable[tier] || 22) * 0.112;

    const totalInputCost = baseResourceCost + feeCost;
    const effectiveCost = totalInputCost * (1 - rrr);

    const taxAmount = sellPrice * marketTax;
    const netProfit = sellPrice - effectiveCost - taxAmount;
    const roi = (netProfit / effectiveCost) * 100;

    const totalProfitEl = document.getElementById('totalProfit');
    const roiValEl = document.getElementById('roiVal');
    const unitCostEl = document.getElementById('unitCost');

    totalProfitEl.innerText = Math.floor(netProfit).toLocaleString();
    unitCostEl.innerText = Math.floor(effectiveCost).toLocaleString() + " سيلفر";
    
    roiValEl.innerText = isFinite(roi) ? roi.toFixed(1) + "%" : "0%";
    
    if (netProfit > 0) {
        totalProfitEl.style.color = "#2ecc71";
        roiValEl.style.color = "#2ecc71";
    } else {
        totalProfitEl.style.color = "#e74c3c";
        roiValEl.style.color = "#e74c3c";
    }
}
window.onload = calculate;
</script>

</body>
</html>
