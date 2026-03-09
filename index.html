import React, { useState, useEffect } from 'react';

const App = () => {
  const [height, setHeight] = useState('');
  const [weight, setWeight] = useState('');
  const [bmiResult, setBmiResult] = useState(null);
  const [error, setError] = useState('');

  // 台灣衛福部國健署 BMI 標準與對應的現代化色彩
  const getBmiCategory = (bmi) => {
    if (bmi < 18.5) return { label: '體重過輕', color: 'text-sky-600', bg: 'bg-sky-50', ring: 'ring-sky-200', bar: 'bg-sky-400' };
    if (bmi >= 18.5 && bmi < 24) return { label: '正常範圍', color: 'text-emerald-600', bg: 'bg-emerald-50', ring: 'ring-emerald-200', bar: 'bg-emerald-400' };
    if (bmi >= 24 && bmi < 27) return { label: '過重', color: 'text-amber-600', bg: 'bg-amber-50', ring: 'ring-amber-200', bar: 'bg-amber-400' };
    if (bmi >= 27 && bmi < 30) return { label: '輕度肥胖', color: 'text-orange-600', bg: 'bg-orange-50', ring: 'ring-orange-200', bar: 'bg-orange-500' };
    if (bmi >= 30 && bmi < 35) return { label: '中度肥胖', color: 'text-rose-600', bg: 'bg-rose-50', ring: 'ring-rose-200', bar: 'bg-rose-500' };
    return { label: '重度肥胖', color: 'text-red-700', bg: 'bg-red-50', ring: 'ring-red-300', bar: 'bg-red-600' };
  };

  // 監聽身高或體重變化，即時計算 BMI
  useEffect(() => {
    setError('');
    
    // 如果兩個都沒有輸入，清空結果
    if (!height && !weight) {
      setBmiResult(null);
      return;
    }

    const h = parseFloat(height);
    const w = parseFloat(weight);

    // 如果輸入不完整或不是數字，暫不顯示結果與錯誤
    if (!height || !weight || isNaN(h) || isNaN(w)) {
      setBmiResult(null);
      return;
    }

    if (h <= 0 || w <= 0) {
      setError('請輸入大於 0 的數值！');
      setBmiResult(null);
      return;
    }

    const heightInMeters = h / 100;
    const bmiValue = w / (heightInMeters * heightInMeters);
    const roundedBmi = Math.round(bmiValue * 10) / 10; 
    
    // 計算理想體重範圍 (18.5 ~ 24)
    const idealMin = Math.round(18.5 * heightInMeters * heightInMeters * 10) / 10;
    const idealMax = Math.round(23.9 * heightInMeters * heightInMeters * 10) / 10;

    // 計算建議調整的體重
    let weightSuggestion = '';
    if (roundedBmi < 18.5) {
      const gainNeeded = (idealMin - w).toFixed(1);
      weightSuggestion = `建議增加 ${gainNeeded} kg`;
    } else if (roundedBmi >= 24) {
      const loseNeeded = (w - idealMax).toFixed(1);
      weightSuggestion = `建議減少 ${loseNeeded} kg`;
    } else {
      weightSuggestion = '太棒了，請繼續保持！';
    }

    const category = getBmiCategory(roundedBmi);

    setBmiResult({
      value: roundedBmi.toFixed(1),
      idealMin,
      idealMax,
      weightSuggestion,
      ...category
    });
  }, [height, weight]);

  const resetForm = () => {
    setHeight('');
    setWeight('');
    setBmiResult(null);
    setError('');
  };

  return (
    <div className="min-h-screen flex items-center justify-center p-4 font-sans bg-[conic-gradient(at_top_right,_var(--tw-gradient-stops))] from-indigo-50 via-slate-50 to-cyan-50 selection:bg-indigo-100">
      
      {/* 裝飾性背景光暈 */}
      <div className="fixed top-0 left-0 w-full h-full overflow-hidden pointer-events-none z-0">
        <div className="absolute top-[-10%] left-[-10%] w-96 h-96 bg-indigo-300 rounded-full mix-blend-multiply filter blur-[128px] opacity-40"></div>
        <div className="absolute bottom-[-10%] right-[-10%] w-96 h-96 bg-cyan-300 rounded-full mix-blend-multiply filter blur-[128px] opacity-40"></div>
      </div>

      <div className="relative z-10 bg-white/80 backdrop-blur-xl rounded-[2rem] shadow-[0_20px_60px_-15px_rgba(0,0,0,0.1)] border border-white/50 p-6 sm:p-10 w-full max-w-md">
        
        {/* 標題區塊 */}
        <div className="text-center mb-8">
          <div className="inline-flex items-center justify-center w-16 h-16 rounded-2xl bg-gradient-to-tr from-indigo-500 to-cyan-400 text-white shadow-lg shadow-indigo-200 mb-4 transform -rotate-3 hover:rotate-0 transition-transform duration-300">
            <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><path d="M4.5 16.5c-1.5 1.26-2 5-2 5s3.74-.5 5-2c.71-.84.7-2.13-.09-2.91a2.18 2.18 0 0 0-2.91-.09z"/><mpath d="m12 15-3-3a22 22 0 0 1 3.82-13 1.5 1.5 0 0 0 2.18 2.06L11 9l4 4 2.94-3.94a1.5 1.5 0 0 0 2.06 2.18A22 22 0 0 1 7 20z"/></svg>
          </div>
          <h1 className="text-3xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-slate-800 to-slate-600 tracking-tight">
            BMI 健康計算器
          </h1>
          <p className="text-slate-500 mt-2 text-sm font-medium">了解您的身體質量指數</p>
        </div>
        
        <div className="space-y-6">
          {/* 身高輸入框 */}
          <div className="group">
            <label htmlFor="height" className="block text-sm font-semibold text-slate-700 mb-2 ml-1">
              身高 <span className="text-slate-400 font-normal">(公分)</span>
            </label>
            <div className="relative flex items-center">
              <div className="absolute left-4 text-slate-400 group-focus-within:text-indigo-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.5" strokeLinecap="round" strokeLinejoin="round"><path d="m21 16-4 4-4-4"/><path d="M17 20V4"/><path d="m3 8 4-4 4 4"/><path d="M7 4v16"/></svg>
              </div>
              <input
                type="number"
                id="height"
                value={height}
                onChange={(e) => setHeight(e.target.value)}
                placeholder="例如: 175"
                className="w-full pl-12 pr-16 py-3.5 bg-slate-50 text-slate-800 text-lg font-medium rounded-2xl border-0 ring-1 ring-inset ring-slate-200 focus:ring-2 focus:ring-inset focus:ring-indigo-500 focus:bg-white transition-all outline-none"
              />
              <span className="absolute right-4 text-slate-400 font-medium select-none">cm</span>
            </div>
          </div>

          {/* 體重輸入框 */}
          <div className="group">
            <label htmlFor="weight" className="block text-sm font-semibold text-slate-700 mb-2 ml-1">
              體重 <span className="text-slate-400 font-normal">(公斤)</span>
            </label>
            <div className="relative flex items-center">
              <div className="absolute left-4 text-slate-400 group-focus-within:text-indigo-500 transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.5" strokeLinecap="round" strokeLinejoin="round"><path d="M6 19v-3"/><path d="M10 19v-3"/><path d="M14 19v-3"/><path d="M18 19v-3"/><path d="M8 11V9"/><path d="M16 11V9"/><path d="M12 4v-1"/><path d="M2 13h20"/><path d="M3 13a2 2 0 0 0-2 2v2a2 2 0 0 0 2 2h18a2 2 0 0 0 2-2v-2a2 2 0 0 0-2-2"/></svg>
              </div>
              <input
                type="number"
                id="weight"
                value={weight}
                onChange={(e) => setWeight(e.target.value)}
                placeholder="例如: 70"
                className="w-full pl-12 pr-16 py-3.5 bg-slate-50 text-slate-800 text-lg font-medium rounded-2xl border-0 ring-1 ring-inset ring-slate-200 focus:ring-2 focus:ring-inset focus:ring-indigo-500 focus:bg-white transition-all outline-none"
              />
              <span className="absolute right-4 text-slate-400 font-medium select-none">kg</span>
            </div>
          </div>

          {/* 錯誤訊息 */}
          {error && (
            <div className="flex items-center text-rose-500 text-sm font-medium bg-rose-50 px-4 py-3 rounded-xl">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" className="mr-2 flex-shrink-0" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2" strokeLinecap="round" strokeLinejoin="round"><circle cx="12" cy="12" r="10"/><line x1="12" y1="8" x2="12" y2="12"/><line x1="12" y1="16" x2="12.01" y2="16"/></svg>
              {error}
            </div>
          )}

          {/* 按鈕區域：即時計算，因此改為只顯示重新輸入按鈕 */}
          <div className={`pt-2 transition-all duration-300 ${height || weight ? 'opacity-100 h-auto' : 'opacity-0 h-0 overflow-hidden pointer-events-none'}`}>
            <button
              onClick={resetForm}
              className="w-full flex items-center justify-center bg-slate-100 hover:bg-slate-200 text-slate-600 font-bold py-3.5 px-4 rounded-2xl transition-all duration-200 mt-2"
              title="清除重新輸入"
            >
              <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2.5" strokeLinecap="round" strokeLinejoin="round" className="mr-2"><path d="M3 12a9 9 0 1 0 9-9 9.75 9.75 0 0 0-6.74 2.74L3 8"/><path d="M3 3v5h5"/></svg>
              清除重新輸入
            </button>
          </div>
        </div>

        {/* 結果顯示區域 */}
        {bmiResult && (
          <div className={`mt-6 overflow-hidden rounded-2xl ${bmiResult.bg} ring-1 ${bmiResult.ring} shadow-sm transition-all duration-500`}>
            <div className="p-6 relative">
              {/* 裝飾線條 */}
              <div className={`absolute top-0 left-0 w-1 h-full ${bmiResult.bar}`}></div>
              
              <div className="flex justify-between items-start">
                <div>
                  <h2 className="text-slate-500 text-sm font-semibold tracking-wider uppercase mb-1">您的 BMI 指數</h2>
                  <div className="flex items-baseline gap-2">
                    <span className="text-5xl font-black text-slate-800 tracking-tighter">{bmiResult.value}</span>
                  </div>
                </div>
                <div className={`px-4 py-2 rounded-xl font-bold text-sm ${bmiResult.color} bg-white/60 shadow-sm backdrop-blur-sm border border-white/40`}>
                  {bmiResult.label}
                </div>
              </div>

              <div className="mt-6 pt-5 border-t border-slate-200/50">
                <div className="flex justify-between items-center text-sm">
                  <span className="text-slate-500 font-medium">健康體重範圍：</span>
                  <span className="font-bold text-slate-700">{bmiResult.idealMin} ~ {bmiResult.idealMax} kg</span>
                </div>
                <div className="flex justify-between items-center text-sm mt-2">
                  <span className="text-slate-500 font-medium">體重調整建議：</span>
                  <span className={`font-bold ${bmiResult.color}`}>{bmiResult.weightSuggestion}</span>
                </div>
              </div>
            </div>
          </div>
        )}

        {/* BMI 基準對照表 */}
        <div className="mt-8 pt-6 border-t border-slate-200/60">
          <h3 className="text-sm font-bold text-slate-600 mb-3 text-center tracking-wide">BMI 基準對照表</h3>
          <div className="overflow-hidden rounded-xl border border-slate-200/60 bg-white/40 backdrop-blur-sm">
            <table className="w-full text-xs text-left text-slate-600">
              <thead className="bg-slate-100/50 text-slate-500">
                <tr>
                  <th className="px-4 py-2.5 font-semibold">狀態</th>
                  <th className="px-4 py-2.5 font-semibold">BMI 範圍</th>
                </tr>
              </thead>
              <tbody className="divide-y divide-slate-100/60">
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-sky-400"></span>體重過輕
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">&lt; 18.5</td>
                </tr>
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-emerald-400"></span>正常範圍
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">18.5 - 23.9</td>
                </tr>
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-amber-400"></span>過重
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">24.0 - 26.9</td>
                </tr>
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-orange-500"></span>輕度肥胖
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">27.0 - 29.9</td>
                </tr>
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-rose-500"></span>中度肥胖
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">30.0 - 34.9</td>
                </tr>
                <tr className="hover:bg-white/60 transition-colors">
                  <td className="px-4 py-2 flex items-center gap-2">
                    <span className="w-2 h-2 rounded-full bg-red-600"></span>重度肥胖
                  </td>
                  <td className="px-4 py-2 font-medium font-mono text-slate-500">&ge; 35.0</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>

      </div>
    </div>
  );
};

export default App;
