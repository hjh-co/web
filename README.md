<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>政协委员通 </title>
<link rel="stylesheet" href="https://cdn.bootcdn.net/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Microsoft Yahei", sans-serif;
}
html, body {
  height: 100%;
  background: #f5f7fa;
  color: #333;
}
.wrap {
  display: flex;
  height: 100vh;
  overflow: hidden;
}

/* 左侧菜单 */
.sidebar {
  width: 210px;
  background: #2c3e50;
  color: #fff;
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
  box-shadow: 0 0 8px rgba(0,0,0,0.15);
}
.logo {
  height: 65px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 18px;
  font-weight: bold;
  background: #1a252f;
}
.menu {
  flex: 1;
  padding: 10px 0;
  overflow-y: auto;
}
.menu-item {
  display: flex;
  align-items: center;
  gap: 10px;
  padding: 14px 20px;
  color: #cbd5e0;
  transition: all 0.25s ease;
  cursor: pointer;
}
.menu-item:hover {
  background: #34495e;
  color: #fff;
}
.menu-item.active {
  background: #3498db;
  color: #fff;
  border-left: 4px solid #fff;
}
.menu-item i {
  width: 16px;
  text-align: center;
}

/* 右侧主体 */
.main {
  flex: 1;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}
.header {
  height: 65px;
  background: #fff;
  border-bottom: 1px solid #e4e7ed;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding: 0 24px;
  gap: 20px;
  flex-shrink: 0;
}
.user-info {
  display: flex;
  align-items: center;
  gap: 10px;
}
.avatar {
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background: #3498db;
  color: #fff;
  display: grid;
  place-items: center;
  font-weight: bold;
}

/* 内容区 */
.content {
  flex: 1;
  padding: 20px;
  overflow-y: auto;
}
.bread {
  background: #fff;
  padding: 12px 16px;
  border-radius: 6px;
  margin-bottom: 20px;
  color: #666;
  font-size: 13px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
}

/* 统计卡片 */
.card-box {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 16px;
  margin-bottom: 24px;
}
.card {
  background: #fff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
  border-left: 4px solid #3498db;
}
.card.label {
  font-size: 13px;
  color: #666;
  margin-bottom: 8px;
}
.card.num {
  font-size: 26px;
  font-weight: 600;
  color: #2c3e50;
}

/* 模块标题 */
.title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.title i {
  color: #3498db;
}

/* 文件列表 */
.file-list {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
  margin-bottom: 24px;
}
.file-item {
  width: 200px;
  background: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
}
.file-preview {
  height: 120px;
  display: grid;
  place-items: center;
  background: #f8f9fa;
}
.file-info {
  padding: 12px;
}
.file-name {
  font-size: 13px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.file-time {
  font-size: 11px;
  color: #999;
  margin-top: 4px;
}

/* 动态 */
.news {
  background: #fff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.05);
}
.news-item {
  padding: 12px 0;
  border-bottom: 1px solid #f2f3f5;
  display: flex;
  gap: 12px;
}
.news-tag {
  padding: 4px 10px;
  font-size: 12px;
  border-radius: 4px;
  background: #e8f4fd;
  color: #3498db;
  white-space: nowrap;
}
.news-content {
  flex: 1;
}
.news-title {
  font-weight: 500;
  margin-bottom: 4px;
}
.news-desc {
  font-size: 12px;
  color: #666;
}
.news-date {
  font-size: 11px;
  color: #999;
  white-space: nowrap;
}
</style>
</head>
<body>

<div class="wrap">
  <!-- 左侧菜单 -->
  <div class="sidebar">
    <div class="logo">政协委员履职平台</div>
    <div class="menu">
      <div class="menu-item active" onclick="render('home')">
        <i class="fa-solid fa-house"></i>委员之家
      </div>
      <div class="menu-item" onclick="render('street')">
        <i class="fa-solid fa-street-view"></i>街道委员小组
      </div>
      <div class="menu-item" onclick="render('sector')">
        <i class="fa-solid fa-sitemap"></i>界别情况
      </div>
      <div class="menu-item" onclick="render('consult')">
        <i class="fa-solid fa-handshake"></i>协商民主
      </div>
      <div class="menu-item" onclick="render('work')">
        <i class="fa-solid fa-briefcase"></i>履职平台
      </div>
      <div class="menu-item" onclick="render('star')">
        <i class="fa-solid fa-star"></i>星级工作室
      </div>
      <div class="menu-item" onclick="render('plan')">
        <i class="fa-solid fa-calendar"></i>2026履职计划
      </div>
    </div>
  </div>

  <!-- 右侧 -->
  <div class="main">
    <div class="header">
      <div class="user-info">
        <div class="avatar">委</div>
        <span>委员用户</span>
      </div>
    </div>
    <div class="content">
      <div class="bread" id="bread">当前位置：首页 / 委员之家</div>
      <div id="page"></div>
    </div>
  </div>
</div>

<script>
// 模拟本地JSON数据
const data = {
  home: {
    name: "委员之家",
    path: "首页 / 委员之家",
    stats: { total: 0, update: "2026-05-07", category: 16 },
    files: [
      { id:1, name:"活动现场照片", icon:"fa-image", time:"2026-05-07" },
      { id:2, name:"情况介绍文档", icon:"fa-file-word", time:"2026-05-06" },
      { id:3, name:"数据统计表格", icon:"fa-file-excel", time:"2026-05-05" }
    ],
    news: [
      { id:1, title:"政协委员专题工作会议", desc:"开展专题调研与工作部署", date:"2026-05-07", tag:"会议" },
      { id:2, title:"基层履职实践活动", desc:"深入社区开展服务与协商", date:"2026-05-06", tag:"活动" }
    ]
  },
  street: { name:"街道委员小组", path:"首页 / 街道委员小组", stats:{total:0, update:"2026-05-07", category:8}, files:[], news:[] },
  sector: { name:"界别基本情况", path:"首页 / 界别基本情况", stats:{total:0, update:"2026-05-07", category:6}, files:[], news:[] },
  consult: { name:"协商民主实践", path:"首页 / 协商民主实践", stats:{total:0, update:"2026-05-07", category:5}, files:[], news:[] },
  work: { name:"委员履职平台", path:"首页 / 委员履职平台", stats:{total:0, update:"2026-05-07", category:12}, files:[], news:[] },
  star: { name:"星级工作室风采", path:"首页 / 星级工作室风采", stats:{total:0, update:"2026-05-07", category:4}, files:[], news:[] },
  plan: { name:"2026履职计划", path:"首页 / 2026履职计划", stats:{total:0, update:"2026-05-07", category:3}, files:[], news:[] }
};

// 渲染页面
function render(page) {
  const d = data[page];
  document.getElementById("bread").innerText = "当前位置：" + d.path;

  let filesHtml = d.files.map(f => `
    <div class="file-item">
      <div class="file-preview"><i class="fa-solid ${f.icon} fa-2x"></i></div>
      <div class="file-info">
        <div class="file-name">${f.name}</div>
        <div class="file-time">${f.time}</div>
      </div>
    </div>
  `).join('');

  let newsHtml = d.news.map(n => `
    <div class="news-item">
      <div class="news-tag">${n.tag}</div>
      <div class="news-content">
        <div class="news-title">${n.title}</div>
        <div class="news-desc">${n.desc}</div>
      </div>
      <div class="news-date">${n.date}</div>
    </div>
  `).join('');

  document.getElementById("page").innerHTML = `
    <div class="card-box">
      <div class="card">
        <div class="label">数据总量</div>
        <div class="num">${d.stats.total} 项</div>
      </div>
      <div class="card" style="border-left-color:#2ecc71">
        <div class="label">最近更新</div>
        <div class="num">${d.stats.update}</div>
      </div>
      <div class="card" style="border-left-color:#f39c12">
        <div class="label">分类总数</div>
        <div class="num">${d.stats.category} 类</div>
      </div>
    </div>

    <div class="title"><i class="fa-solid fa-thumbtack"></i>${d.name} - 资料文件</div>
    <div class="file-list">${filesHtml}</div>

    <div class="news">
      <div class="title"><i class="fa-solid fa-bell"></i>${d.name} - 最新动态</div>
      ${newsHtml}
    </div>
  `;

  // 菜单高亮
  document.querySelectorAll('.menu-item').forEach(el => {
    el.classList.remove('active');
  });
  document.querySelectorAll('.menu-item')[['home','street','sector','consult','work','star','plan'].indexOf(page)].classList.add('active');
}

// 初始加载
render('home');
</script>
</body>
</html>
