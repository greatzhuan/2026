<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2026 承诺日历</title>
    <style>
        :root { --main-pink: #ffafbd; --deep-pink: #ff1493; --bg: #fffafa; }
        body { font-family: 'PingFang SC', sans-serif; background: var(--bg); margin: 0; padding: 10px; }
        .container { max-width: 900px; margin: 0 auto; }
        .config-panel { background: white; padding: 15px; border-radius: 12px; margin-bottom: 20px; box-shadow: 0 2px 8px rgba(0,0,0,0.05); font-size: 0.9em; }
        .calendar-grid { display: grid; grid-template-columns: repeat(7, 1fr); gap: 5px; }
        .month-title { grid-column: 1 / -1; padding: 20px 0 10px; color: var(--deep-pink); font-weight: bold; border-bottom: 2px solid #ffeef0; }
        .weekday-header { text-align: center; font-size: 0.7em; color: #999; padding: 5px 0; }
        .day-box { 
            background: white; border-radius: 4px; aspect-ratio: 1/1; padding: 4px;
            border: 1px solid #eee; cursor: pointer; display: flex; flex-direction: column; justify-content: space-between;
        }
        .day-box.other-month { opacity: 0.3; pointer-events: none; }
        .day-box.has-task { background: #fff0f3; border-color: var(--main-pink); }
        .day-box.completed { background: var(--main-pink); color: white; border-color: var(--deep-pink); }
        .date-num { font-size: 0.8em; font-weight: bold; }
        .task-hint { font-size: 0.5em; line-height: 1.1; overflow: hidden; }
        .modal { display:none; position:fixed; top:50%; left:50%; transform:translate(-50%, -50%); background:white; padding:20px; border-radius:15px; box-shadow:0 10px 30px rgba(0,0,0,0.2); z-index:100; width: 260px; }
        .overlay { display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.4); z-index:99; }
    </style>
</head>
<body>
<div class="container">
    <h2>🗓️ 2026 我们的专属约定</h2>
    <div class="config-panel">
        <div style="margin-bottom:10px"><b>预设：</b><input type="text" id="task-name" value="💆‍♂️ 按摩服务" style="width:100px"> 每 <input type="number" id="gap" value="2" style="width:35px"> 天一次</div>
        <button onclick="applySettings()" style="background:var(--main-pink); border:none; color:white; padding:5px 15px; border-radius:5px; cursor:pointer">更新全年预设</button>
    </div>
    <div id="calendar-body" class="calendar-grid"></div>
</div>

<div class="overlay" id="overlay" onclick="closeModal()"></div>
<div class="modal" id="modal">
    <h4 id="m-date"></h4>
    <textarea id="m-task" style="width:100%; height:60px; margin-bottom:10px;"></textarea>
    <button onclick="save()" style="width:100%; background:var(--main-pink); color:white; border:none; padding:8px; border-radius:5px;">保存记录</button>
</div>

<script>
    let config = JSON.parse(localStorage.getItem('loverConfig_2026')) || { name: "💆‍♂️ 按摩", gap: 2 };
    let records = JSON.parse(localStorage.getItem('loverRecords_2026')) || {};

    function render() {
        const body = document.getElementById('calendar-body');
        body.innerHTML = '';
        const months = ["一月", "二月", "三月", "四月", "五月", "六月", "七月", "八月", "九月", "十月", "十一月", "十二月"];
        
        for (let m = 0; m < 12; m++) {
            body.innerHTML += `<div class="month-title">${months[m]}</div>`;
            ['日','一','二','三','四','五','六'].forEach(w => body.innerHTML += `<div class="weekday-header">${w}</div>`);
            
            let firstDay = new Date(2026, m, 1).getDay();
            let daysInMonth = new Date(2026, m + 1, 0).getDate();

            for (let i = 0; i < firstDay; i++) body.innerHTML += `<div class="day-box other-month"></div>`;
            
            for (let d = 1; d <= daysInMonth; d++) {
                const dateObj = new Date(2026, m, d);
                const dStr = dateObj.toISOString().split('T')[0];
                const diffDays = Math.floor((dateObj - new Date(2026, 0, 1)) / (1000*60*60*24));
                
                let task = records[dStr] || (diffDays % config.gap === 0 ? { name: config.name, done: false } : null);
                
                const box = document.createElement('div');
                box.className = `day-box ${task ? 'has-task' : ''} ${task?.done ? 'completed' : ''}`;
                box.innerHTML = `<div class="date-num">${d}</div><div class="task-hint">${task ? task.name : ''}</div>`;
                box.onclick = () => openModal(dStr, task);
                body.appendChild(box);
            }
        }
    }

    let activeDate = '';
    function openModal(date, task) {
        activeDate = date;
        document.getElementById('m-date').innerText = date;
        document.getElementById('m-task').value = task ? task.name : "";
        document.getElementById('modal').style.display = 'block';
        document.getElementById('overlay').style.display = 'block';
    }

    function save() {
        records[activeDate] = { name: document.getElementById('m-task').value, done: true };
        localStorage.setItem('loverRecords_2026', JSON.stringify(records));
        closeModal(); render();
    }

    function applySettings() {
        config.name = document.getElementById('task-name').value;
        config.gap = parseInt(document.getElementById('gap').value);
        localStorage.setItem('loverConfig_2026', JSON.stringify(config));
        render();
    }

    function closeModal() { document.getElementById('modal').style.display = 'none'; document.getElementById('overlay').style.display = 'none'; }
    render();
</script>
</body>
</html>
