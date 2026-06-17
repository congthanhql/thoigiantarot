

<style>
*{box-sizing:border-box;margin:0;padding:0}
:root{
  --p:#7F77DD;--p-soft:#EEEDFE;--p-text:#3C3489;
  --bg0:#faf9f7;--bg1:#ffffff;--bg2:#f3f1ed;--bg3:#e8e5de;
  --t1:#1c1b1a;--t2:#5c5a56;--t3:#9c9a96;
  --bd:rgba(0,0,0,0.09);--bd2:rgba(0,0,0,0.15);
  --r:10px;--rl:14px;
  --days-bg:#E6F1FB;--days-t:#0C447C;
  --wks-bg:#EAF3DE;--wks-t:#27500A;
  --mo-bg:#FAEEDA;--mo-t:#633806;
  --yr-bg:#FCEBEB;--yr-t:#791F1F;
}
.dk{
  --p:#9b8fe0;--p-soft:#2a2040;--p-text:#c4bef5;
  --bg0:#111010;--bg1:#1c1b1e;--bg2:#252428;--bg3:#302e35;
  --t1:#f0eee8;--t2:#a09d96;--t3:#605e58;
  --bd:rgba(255,255,255,0.09);--bd2:rgba(255,255,255,0.16);
  --days-bg:#0C2040;--days-t:#85B7EB;
  --wks-bg:#0f2010;--wks-t:#97C459;
  --mo-bg:#251800;--mo-t:#FAC775;
  --yr-bg:#200808;--yr-t:#F09595;
}
html,body{background:var(--bg0);color:var(--t1);font-family:system-ui,sans-serif;transition:background .2s,color .2s;min-height:100vh}
.page{padding:1.5rem 1.25rem}

.login-wrap{max-width:380px;margin:3rem auto 0}
.login-logo{text-align:center;margin-bottom:2rem}
.logo-circle{width:52px;height:52px;border-radius:50%;background:var(--p-soft);display:inline-flex;align-items:center;justify-content:center;margin-bottom:.75rem}
.logo-circle i{font-size:24px;color:var(--p)}
.login-logo h1{font-size:20px;font-weight:500;color:var(--t1);margin-bottom:4px}
.login-logo p{font-size:13px;color:var(--t2)}
.card{background:var(--bg1);border:0.5px solid var(--bd);border-radius:var(--rl);padding:1.75rem}
.field-label{font-size:12px;font-weight:500;color:var(--t2);letter-spacing:.04em;margin-bottom:6px;display:block}
.inp-wrap{position:relative}
.inp-wrap input{width:100%;height:40px;padding:0 40px 0 12px;border:0.5px solid var(--bd2);border-radius:var(--r);background:var(--bg2);color:var(--t1);font-size:14px;outline:none;transition:border-color .15s}
.inp-wrap input:focus{border-color:var(--p)}
.eye-btn{position:absolute;right:11px;top:50%;transform:translateY(-50%);background:none;border:none;cursor:pointer;color:var(--t3);font-size:17px;display:flex;line-height:1}
.eye-btn:hover{color:var(--t1)}
.btn-primary{width:100%;height:40px;background:var(--p);border:none;border-radius:var(--r);color:#fff;font-size:14px;font-weight:500;cursor:pointer;margin-top:1rem;display:flex;align-items:center;justify-content:center;gap:6px;transition:opacity .15s}
.btn-primary:hover{opacity:.88}
.err{font-size:12px;color:var(--yr-t);margin-top:8px;text-align:center;min-height:18px}
.theme-row{display:flex;justify-content:flex-end;margin-bottom:1.25rem}
.theme-btn{display:flex;align-items:center;gap:5px;background:var(--bg2);border:0.5px solid var(--bd);border-radius:20px;padding:5px 12px;cursor:pointer;font-size:12px;color:var(--t2);transition:background .15s}
.theme-btn:hover{background:var(--bg3)}

.app-wrap{display:none}
.topbar{display:flex;justify-content:space-between;align-items:center;margin-bottom:1.5rem;padding-bottom:1rem;border-bottom:0.5px solid var(--bd)}
.brand{display:flex;align-items:center;gap:8px}
.brand-dot{width:28px;height:28px;border-radius:8px;background:var(--p-soft);display:flex;align-items:center;justify-content:center}
.brand-dot i{font-size:15px;color:var(--p)}
.brand-name{font-size:14px;font-weight:500;color:var(--t1)}
.topbar-right{display:flex;align-items:center;gap:8px}
.icon-btn{background:none;border:0.5px solid var(--bd);border-radius:var(--r);padding:5px 10px;cursor:pointer;color:var(--t2);font-size:13px;display:flex;align-items:center;gap:5px}
.icon-btn:hover{background:var(--bg2)}

.tabs-row{display:flex;gap:4px;margin-bottom:1.25rem;flex-wrap:wrap}
.tab{padding:6px 14px;font-size:13px;border-radius:20px;cursor:pointer;background:none;border:0.5px solid transparent;color:var(--t2);transition:all .15s}
.tab:hover{background:var(--bg2)}
.tab.on{background:var(--p-soft);color:var(--p-text);border-color:transparent;font-weight:500}

.toolbar{display:flex;gap:8px;margin-bottom:1rem}
.toolbar input{flex:1;height:36px;padding:0 12px;border:0.5px solid var(--bd2);border-radius:var(--r);background:var(--bg2);color:var(--t1);font-size:13px;outline:none}
.toolbar input:focus{border-color:var(--p)}
.toolbar select{height:36px;padding:0 10px;border:0.5px solid var(--bd2);border-radius:var(--r);background:var(--bg2);color:var(--t1);font-size:13px;outline:none}

.legend{display:flex;gap:12px;flex-wrap:wrap;margin-bottom:1.25rem}
.leg{display:flex;align-items:center;gap:5px;font-size:11px;color:var(--t3)}
.dot{width:7px;height:7px;border-radius:50%}

.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:10px}
.crd{background:var(--bg1);border:0.5px solid var(--bd);border-radius:var(--rl);padding:.9rem 1rem;cursor:pointer;transition:border-color .15s}
.crd:hover{border-color:var(--p)}
.crd-name{font-size:13px;font-weight:500;color:var(--t1);margin-bottom:2px}
.crd-suite{font-size:11px;color:var(--t3);margin-bottom:6px}
.crd-time{font-size:12px;color:var(--t2);display:flex;align-items:center;gap:4px}
.pill{display:inline-block;font-size:11px;font-weight:500;padding:2px 9px;border-radius:20px;margin-top:7px}
.p-day{background:var(--days-bg);color:var(--days-t)}
.p-wk{background:var(--wks-bg);color:var(--wks-t)}
.p-mo{background:var(--mo-bg);color:var(--mo-t)}
.p-yr{background:var(--yr-bg);color:var(--yr-t)}

.detail{display:none;margin-bottom:1rem;background:var(--p-soft);border:0.5px solid var(--bd);border-radius:var(--rl);padding:1.25rem}
.detail.open{display:block}
.dh{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:.6rem}
.dh-title{font-size:15px;font-weight:500;color:var(--t1)}
.dh-sub{font-size:12px;color:var(--t2);margin-top:2px}
.close{background:none;border:none;cursor:pointer;font-size:18px;color:var(--t3);padding:0}
.close:hover{color:var(--t1)}
.d-desc{font-size:13px;color:var(--t2);line-height:1.65;margin-bottom:.75rem}
.d-meta{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.d-item{background:var(--bg1);border-radius:var(--r);padding:8px 10px;border:0.5px solid var(--bd)}
.d-label{font-size:11px;color:var(--t3);margin-bottom:2px}
.d-val{font-size:13px;font-weight:500;color:var(--t1)}

.empty{text-align:center;padding:3rem 1rem;color:var(--t3);font-size:14px}
</style>

<div class="page" id="root">
  <h2 style="position:absolute;width:1px;height:1px;overflow:hidden">Tra cứu thời gian Tarot</h2>

  <div id="loginView">
    <div class="theme-row">
      <button class="theme-btn" onclick="toggleTheme()" id="thBtn2"><i class="ti ti-moon" id="thIc2" aria-hidden="true"></i><span id="thLb2">Chế độ tối</span></button>
    </div>
    <div class="login-wrap">
      <div class="login-logo">
        <div class="logo-circle"><i class="ti ti-cards" aria-hidden="true"></i></div>
        <h1>Tarot thời gian</h1>
        <p>Tra cứu ý nghĩa thời gian 78 lá bài Tarot</p>
      </div>
      <div class="card">
        <label class="field-label">Mã kết nối</label>
        <div class="inp-wrap">
          <input type="password" id="codeIn" placeholder="Nhập mã của bạn..." />
          <button class="eye-btn" onclick="toggleEye()" aria-label="Hiện/ẩn mã"><i class="ti ti-eye" id="eyeIc" aria-hidden="true"></i></button>
        </div>
        <div class="err" id="errMsg"></div>
        <button class="btn-primary" onclick="doLogin()"><i class="ti ti-login" aria-hidden="true"></i> Vào tra cứu</button>
      </div>
    </div>
  </div>

  <div class="app-wrap" id="appView">
    <div class="topbar">
      <div class="brand">
        <div class="brand-dot"><i class="ti ti-cards" aria-hidden="true"></i></div>
        <span class="brand-name">Tarot thời gian</span>
      </div>
      <div class="topbar-right">
        <button class="icon-btn" onclick="toggleTheme()" id="thBtn"><i class="ti ti-moon" id="thIc" aria-hidden="true"></i><span id="thLb">Tối</span></button>
        <button class="icon-btn" onclick="doLogout()"><i class="ti ti-logout" aria-hidden="true"></i> Đăng xuất</button>
      </div>
    </div>

    <div class="tabs-row" id="tabsRow"></div>

    <div class="detail" id="detail"></div>

    <div class="toolbar">
      <input type="text" id="q" placeholder="Tìm tên lá bài..." oninput="render()" />
      <select id="flt" onchange="render()">
        <option value="">Tất cả</option>
        <option value="Ngày">Ngày</option>
        <option value="Tuần">Tuần</option>
        <option value="Tháng">Tháng</option>
        <option value="Năm">Năm</option>
      </select>
    </div>

    <div class="legend">
      <div class="leg"><div class="dot" style="background:var(--days-t)"></div>Ngày</div>
      <div class="leg"><div class="dot" style="background:var(--wks-t)"></div>Tuần</div>
      <div class="leg"><div class="dot" style="background:var(--mo-t)"></div>Tháng</div>
      <div class="leg"><div class="dot" style="background:var(--yr-t)"></div>Năm+</div>
    </div>

    <div class="grid" id="grid"></div>
  </div>
</div>

<script>
const CODES=["L9pHo3","Thanh123@","admin","Admin"];
let tab="major",dark=false,eyeOpen=false;

const TABS=[
  {id:"major",label:"Ẩn chính",sub:"Major Arcana"},
  {id:"cups",label:"Cốc",sub:"Cups · Nước · Thu"},
  {id:"wands",label:"Gậy",sub:"Wands · Lửa · Hè"},
  {id:"swords",label:"Kiếm",sub:"Swords · Khí · Xuân"},
  {id:"pentacles",label:"Tiền",sub:"Pentacles · Đất · Đông"},
];

const DATA={
  major:[
    {n:"0 – The Fool",t:"Ngay lập tức / 1–3 ngày",r:"Ngày",d:"Khởi đầu mới bất ngờ. Thường xảy ra trong vòng 1–3 ngày.",el:"Không khí",s:"Xuân"},
    {n:"I – The Magician",t:"1 tuần",r:"Tuần",d:"Mọi thứ đang sắp xếp để bắt đầu. Hành động trong tuần tới.",el:"Không khí",s:"Tất cả mùa"},
    {n:"II – The High Priestess",t:"1 tháng",r:"Tháng",d:"Chờ đợi và quan sát. Câu trả lời rõ dần trong 1 tháng.",el:"Nước",s:"Đông"},
    {n:"III – The Empress",t:"3–9 tháng",r:"Tháng",d:"Chu kỳ nở rộ. Gắn với 3–9 tháng, đặc biệt mùa hè.",el:"Đất",s:"Hè"},
    {n:"IV – The Emperor",t:"1 năm",r:"Năm",d:"Xây dựng cấu trúc vững chắc. Thường là 1 năm hoặc lâu hơn.",el:"Lửa",s:"Xuân"},
    {n:"V – The Hierophant",t:"3–6 tháng",r:"Tháng",d:"Truyền thống và thể chế. Thường mất 3–6 tháng.",el:"Đất",s:"Xuân"},
    {n:"VI – The Lovers",t:"6 tháng",r:"Tháng",d:"Lựa chọn quan trọng. Thường xảy ra trong 6 tháng hoặc mùa hè.",el:"Không khí",s:"Hè"},
    {n:"VII – The Chariot",t:"1 tháng",r:"Tháng",d:"Tiến nhanh. Đạt mục tiêu trong 1 tháng nếu tập trung.",el:"Nước",s:"Hè"},
    {n:"VIII – Strength",t:"2–6 tháng",r:"Tháng",d:"Rèn luyện kiên nhẫn. Cần 2–6 tháng để có kết quả bền vững.",el:"Lửa",s:"Hè"},
    {n:"IX – The Hermit",t:"6–12 tháng",r:"Năm",d:"Thu mình suy ngẫm. Khoảng 6–12 tháng cô độc cần thiết.",el:"Đất",s:"Đông"},
    {n:"X – Wheel of Fortune",t:"3 tháng",r:"Tháng",d:"Vận may xoay chuyển. Sự kiện lớn trong 3 tháng tới.",el:"Lửa",s:"Tất cả mùa"},
    {n:"XI – Justice",t:"2–4 tuần",r:"Tuần",d:"Kết quả pháp lý hay cân bằng đến trong 2–4 tuần.",el:"Không khí",s:"Thu"},
    {n:"XII – The Hanged Man",t:"3 tháng+",r:"Năm",d:"Chờ đợi bắt buộc, 3 tháng đến hơn 1 năm. Không thể vội.",el:"Nước",s:"Đông"},
    {n:"XIII – Death",t:"6 tháng",r:"Tháng",d:"Kết thúc chu kỳ cũ. Chuyển hóa hoàn toàn trong 6 tháng.",el:"Nước",s:"Thu"},
    {n:"XIV – Temperance",t:"6 tháng",r:"Tháng",d:"Chữa lành và cân bằng dài hạn. 6 tháng để đạt hài hòa.",el:"Lửa",s:"Thu"},
    {n:"XV – The Devil",t:"Không rõ",r:"Tháng",d:"Bị ràng buộc, thời gian không xác định. Có thể hàng tháng.",el:"Đất",s:"Đông"},
    {n:"XVI – The Tower",t:"Ngay lập tức",r:"Ngày",d:"Xảy ra bất ngờ trong vài ngày.",el:"Lửa",s:"Tất cả mùa"},
    {n:"XVII – The Star",t:"1 năm",r:"Năm",d:"Hy vọng dài hạn. Cần khoảng 1 năm để ước nguyện thành thật.",el:"Không khí",s:"Đông"},
    {n:"XVIII – The Moon",t:"28 ngày",r:"Tháng",d:"Chu kỳ trăng ~28 ngày. Sự thật dần lộ ra trong 1 tháng.",el:"Nước",s:"Đông"},
    {n:"XIX – The Sun",t:"1–3 tháng",r:"Tháng",d:"Thành công và niềm vui. Xuất hiện trong mùa hè hay 1–3 tháng.",el:"Lửa",s:"Hè"},
    {n:"XX – Judgement",t:"2–8 tuần",r:"Tuần",d:"Thức tỉnh hay quyết định quan trọng trong 2–8 tuần.",el:"Lửa",s:"Tất cả mùa"},
    {n:"XXI – The World",t:"1 năm",r:"Năm",d:"Hoàn thành chu kỳ lớn. Cuối năm hoặc sau đúng 1 năm.",el:"Đất",s:"Tất cả mùa"},
  ],
  cups:[
    {n:"Ace of Cups",t:"1 tuần",r:"Tuần",d:"Cảm xúc mới khởi đầu trong vòng 1 tuần.",el:"Nước",s:"Thu"},
    {n:"2 of Cups",t:"2 tuần",r:"Tuần",d:"Kết nối cảm xúc hình thành trong 2 tuần.",el:"Nước",s:"Thu"},
    {n:"3 of Cups",t:"3 tuần",r:"Tuần",d:"Lễ mừng hoặc tụ họp trong 3 tuần.",el:"Nước",s:"Thu"},
    {n:"4 of Cups",t:"4 tuần",r:"Tuần",d:"Giai đoạn chán nản kéo dài 4 tuần.",el:"Nước",s:"Thu"},
    {n:"5 of Cups",t:"5 tuần",r:"Tuần",d:"Nỗi buồn tạm thời trong 5 tuần.",el:"Nước",s:"Thu"},
    {n:"6 of Cups",t:"6 tuần",r:"Tuần",d:"Ký ức quá khứ trỗi dậy trong 6 tuần.",el:"Nước",s:"Thu"},
    {n:"7 of Cups",t:"7 tuần",r:"Tuần",d:"Mơ hồ và nhiều lựa chọn trong 7 tuần.",el:"Nước",s:"Thu"},
    {n:"8 of Cups",t:"8 tuần",r:"Tuần",d:"Rời bỏ và tìm ý nghĩa mới trong 8 tuần.",el:"Nước",s:"Thu"},
    {n:"9 of Cups",t:"9 tuần",r:"Tuần",d:"Ước nguyện thành hiện thực trong 9 tuần.",el:"Nước",s:"Thu"},
    {n:"10 of Cups",t:"10 tuần",r:"Tuần",d:"Hạnh phúc gia đình và viên mãn trong 10 tuần.",el:"Nước",s:"Thu"},
    {n:"Page of Cups",t:"1–7 ngày",r:"Ngày",d:"Thông điệp cảm xúc đến trong 1–7 ngày.",el:"Nước",s:"Thu"},
    {n:"Knight of Cups",t:"1–2 tháng",r:"Tháng",d:"Đề nghị lãng mạn hay sáng tạo trong 1–2 tháng.",el:"Nước",s:"Thu"},
    {n:"Queen of Cups",t:"3 tháng",r:"Tháng",d:"Nuôi dưỡng và chăm sóc qua một mùa (3 tháng).",el:"Nước",s:"Thu"},
    {n:"King of Cups",t:"1 năm",r:"Năm",d:"Trưởng thành cảm xúc cần ít nhất 1 năm.",el:"Nước",s:"Thu"},
  ],
  wands:[
    {n:"Ace of Wands",t:"1 tuần",r:"Tuần",d:"Cảm hứng mới bùng lên trong 1 tuần.",el:"Lửa",s:"Hè"},
    {n:"2 of Wands",t:"2 tuần",r:"Tuần",d:"Lên kế hoạch và chờ đợi trong 2 tuần.",el:"Lửa",s:"Hè"},
    {n:"3 of Wands",t:"3 tuần",r:"Tuần",d:"Kế hoạch bắt đầu triển khai trong 3 tuần.",el:"Lửa",s:"Hè"},
    {n:"4 of Wands",t:"4 tuần",r:"Tuần",d:"Lễ kỷ niệm hay mừng thành quả trong 4 tuần.",el:"Lửa",s:"Hè"},
    {n:"5 of Wands",t:"5 tuần",r:"Tuần",d:"Xung đột và cạnh tranh kéo dài 5 tuần.",el:"Lửa",s:"Hè"},
    {n:"6 of Wands",t:"6 tuần",r:"Tuần",d:"Chiến thắng được công nhận trong 6 tuần.",el:"Lửa",s:"Hè"},
    {n:"7 of Wands",t:"7 tuần",r:"Tuần",d:"Phòng thủ và kiên trì trong 7 tuần.",el:"Lửa",s:"Hè"},
    {n:"8 of Wands",t:"8 ngày",r:"Ngày",d:"Mọi thứ diễn ra rất nhanh — thường trong 8 ngày.",el:"Lửa",s:"Hè"},
    {n:"9 of Wands",t:"9 tuần",r:"Tuần",d:"Phòng thủ cuối cùng trước thành công trong 9 tuần.",el:"Lửa",s:"Hè"},
    {n:"10 of Wands",t:"10 tuần",r:"Tuần",d:"Gánh nặng và áp lực cần giải quyết trong 10 tuần.",el:"Lửa",s:"Hè"},
    {n:"Page of Wands",t:"1–7 ngày",r:"Ngày",d:"Thông điệp nhiệt huyết đến trong 1–7 ngày.",el:"Lửa",s:"Hè"},
    {n:"Knight of Wands",t:"2–4 tuần",r:"Tuần",d:"Hành động táo bạo và nhanh trong 2–4 tuần.",el:"Lửa",s:"Hè"},
    {n:"Queen of Wands",t:"3 tháng",r:"Tháng",d:"Lãnh đạo và sáng tạo phát triển qua một mùa.",el:"Lửa",s:"Hè"},
    {n:"King of Wands",t:"1 năm",r:"Năm",d:"Tầm nhìn dài hạn và dự án lớn cần 1 năm.",el:"Lửa",s:"Hè"},
  ],
  swords:[
    {n:"Ace of Swords",t:"1 tuần",r:"Tuần",d:"Sự thật và rõ ràng xuất hiện trong 1 tuần.",el:"Không khí",s:"Xuân"},
    {n:"2 of Swords",t:"2 tuần",r:"Tuần",d:"Quyết định bị trì hoãn trong 2 tuần.",el:"Không khí",s:"Xuân"},
    {n:"3 of Swords",t:"3 tuần",r:"Tuần",d:"Nỗi đau cần thời gian chữa lành trong 3 tuần.",el:"Không khí",s:"Xuân"},
    {n:"4 of Swords",t:"4 tuần",r:"Tuần",d:"Phục hồi và nghỉ ngơi cần 4 tuần.",el:"Không khí",s:"Xuân"},
    {n:"5 of Swords",t:"5 tuần",r:"Tuần",d:"Hậu quả xung đột kéo dài 5 tuần.",el:"Không khí",s:"Xuân"},
    {n:"6 of Swords",t:"6 tuần",r:"Tuần",d:"Chuyển sang bình yên hơn trong 6 tuần.",el:"Không khí",s:"Xuân"},
    {n:"7 of Swords",t:"7 tuần",r:"Tuần",d:"Cần cảnh giác và khéo léo trong 7 tuần.",el:"Không khí",s:"Xuân"},
    {n:"8 of Swords",t:"8 tuần",r:"Tuần",d:"Cảm giác mắc kẹt trong 8 tuần rồi sẽ qua.",el:"Không khí",s:"Xuân"},
    {n:"9 of Swords",t:"9 ngày",r:"Ngày",d:"Lo lắng cao độ trong 9 ngày, sau đó giảm.",el:"Không khí",s:"Xuân"},
    {n:"10 of Swords",t:"Vài ngày",r:"Ngày",d:"Một giai đoạn kết thúc đột ngột, mở ra cái mới.",el:"Không khí",s:"Xuân"},
    {n:"Page of Swords",t:"1–7 ngày",r:"Ngày",d:"Thông tin hay tin tức đến trong 1–7 ngày.",el:"Không khí",s:"Xuân"},
    {n:"Knight of Swords",t:"1–14 ngày",r:"Ngày",d:"Quyết định cực kỳ nhanh, trong 1–14 ngày.",el:"Không khí",s:"Xuân"},
    {n:"Queen of Swords",t:"3 tháng",r:"Tháng",d:"Sắc bén và độc lập phát triển qua 3 tháng.",el:"Không khí",s:"Xuân"},
    {n:"King of Swords",t:"1 năm",r:"Năm",d:"Quyết định pháp lý hay quyền lực mất đến 1 năm.",el:"Không khí",s:"Xuân"},
  ],
  pentacles:[
    {n:"Ace of Pentacles",t:"1 tháng",r:"Tháng",d:"Cơ hội tài chính hoặc vật chất đến trong 1 tháng.",el:"Đất",s:"Đông"},
    {n:"2 of Pentacles",t:"2 tháng",r:"Tháng",d:"Cân bằng tài chính cần quản lý trong 2 tháng.",el:"Đất",s:"Đông"},
    {n:"3 of Pentacles",t:"3 tháng",r:"Tháng",d:"Hợp tác và công trình đơm hoa trong 3 tháng.",el:"Đất",s:"Đông"},
    {n:"4 of Pentacles",t:"4 tháng",r:"Tháng",d:"Giai đoạn tiết kiệm hoặc giữ chặt trong 4 tháng.",el:"Đất",s:"Đông"},
    {n:"5 of Pentacles",t:"5 tháng",r:"Tháng",d:"Thiếu thốn và thử thách tài chính kéo dài 5 tháng.",el:"Đất",s:"Đông"},
    {n:"6 of Pentacles",t:"6 tuần",r:"Tuần",d:"Hào phóng và cho đi có kết quả trong 6 tuần.",el:"Đất",s:"Đông"},
    {n:"7 of Pentacles",t:"7 tháng",r:"Tháng",d:"Chờ thu hoạch thành quả trong 7 tháng.",el:"Đất",s:"Đông"},
    {n:"8 of Pentacles",t:"8 tháng",r:"Tháng",d:"Rèn kỹ năng và làm việc chăm chỉ trong 8 tháng.",el:"Đất",s:"Đông"},
    {n:"9 of Pentacles",t:"9 tháng",r:"Tháng",d:"Đạt tự túc và phong phú sau 9 tháng.",el:"Đất",s:"Đông"},
    {n:"10 of Pentacles",t:"10 năm",r:"Năm",d:"Xây dựng di sản lâu dài, thường là 10 năm hoặc cả đời.",el:"Đất",s:"Đông"},
    {n:"Page of Pentacles",t:"1–3 tuần",r:"Tuần",d:"Tin tức về tiền bạc hoặc học tập trong 1–3 tuần.",el:"Đất",s:"Đông"},
    {n:"Knight of Pentacles",t:"2–4 tháng",r:"Tháng",d:"Tiến độ chậm nhưng chắc, thường 2–4 tháng.",el:"Đất",s:"Đông"},
    {n:"Queen of Pentacles",t:"3 tháng",r:"Tháng",d:"Chăm sóc thực tế và phát triển qua 3 tháng.",el:"Đất",s:"Đông"},
    {n:"King of Pentacles",t:"1 năm+",r:"Năm",d:"Thành công tài chính bền vững cần 1 năm trở lên.",el:"Đất",s:"Đông"},
  ]
};

function pill(r){
  if(r==="Ngày") return '<span class="pill p-day">Ngày</span>';
  if(r==="Tuần") return '<span class="pill p-wk">Tuần</span>';
  if(r==="Tháng") return '<span class="pill p-mo">Tháng</span>';
  return '<span class="pill p-yr">Năm+</span>';
}

function subOf(id){return TABS.find(t=>t.id===id).sub}

function render(){
  const q=document.getElementById("q").value.toLowerCase();
  const f=document.getElementById("flt").value;
  const list=DATA[tab].filter(c=>(!q||c.n.toLowerCase().includes(q)||c.t.toLowerCase().includes(q))&&(!f||c.r===f));
  const g=document.getElementById("grid");
  if(!list.length){g.innerHTML='<div class="empty"><i class="ti ti-search" aria-hidden="true" style="font-size:28px;display:block;margin-bottom:8px"></i>Không tìm thấy lá bài phù hợp</div>';return;}
  g.innerHTML=list.map(c=>`
    <div class="crd" onclick="showDetail(${DATA[tab].indexOf(c)})">
      <div class="crd-name">${c.n}</div>
      <div class="crd-suite">${subOf(tab)}</div>
      <div class="crd-time"><i class="ti ti-clock" aria-hidden="true" style="font-size:12px"></i>${c.t}</div>
      ${pill(c.r)}
    </div>`).join("");
}

function showDetail(i){
  const c=DATA[tab][i];
  const d=document.getElementById("detail");
  d.className="detail open";
  d.innerHTML=`
    <div class="dh">
      <div><div class="dh-title">${c.n}</div><div class="dh-sub">${subOf(tab)}</div></div>
      <button class="close" onclick="closeD()" aria-label="Đóng"><i class="ti ti-x" aria-hidden="true"></i></button>
    </div>
    <p class="d-desc">${c.d}</p>
    <div class="d-meta">
      <div class="d-item"><div class="d-label">Thời gian</div><div class="d-val">${c.t}</div></div>
      <div class="d-item"><div class="d-label">Phạm vi</div><div class="d-val">${pill(c.r)}</div></div>
      <div class="d-item"><div class="d-label">Nguyên tố</div><div class="d-val">${c.el}</div></div>
      <div class="d-item"><div class="d-label">Mùa</div><div class="d-val">${c.s}</div></div>
    </div>`;
  d.scrollIntoView({behavior:"smooth",block:"nearest"});
}

function closeD(){document.getElementById("detail").className="detail";}

function buildTabs(){
  document.getElementById("tabsRow").innerHTML=TABS.map(t=>`
    <button class="tab${t.id===tab?" on":""}" onclick="switchTab('${t.id}')">${t.label}</button>`).join("");
}

function switchTab(id){
  tab=id;closeD();buildTabs();render();
}

function toggleTheme(){
  dark=!dark;
  document.getElementById("root").className=dark?"dk":"";
  const icon=dark?"ti ti-sun":"ti ti-moon";
  const lb1=dark?"Sáng":"Tối";
  const lb2=dark?"Chế độ sáng":"Chế độ tối";
  document.getElementById("thIc").className=icon;document.getElementById("thLb").textContent=lb1;
  document.getElementById("thIc2").className=icon;document.getElementById("thLb2").textContent=lb2;
}

function toggleEye(){
  eyeOpen=!eyeOpen;
  document.getElementById("codeIn").type=eyeOpen?"text":"password";
  document.getElementById("eyeIc").className=eyeOpen?"ti ti-eye-off":"ti ti-eye";
}

function doLogin(){
  const v=document.getElementById("codeIn").value.trim();
  if(CODES.includes(v)){
    document.getElementById("loginView").style.display="none";
    document.getElementById("appView").style.display="block";
    buildTabs();render();
  } else {
    document.getElementById("errMsg").textContent="Mã không đúng, vui lòng thử lại.";
  }
}

function doLogout(){
  document.getElementById("loginView").style.display="block";
  document.getElementById("appView").style.display="none";
  document.getElementById("codeIn").value="";
  document.getElementById("errMsg").textContent="";
  eyeOpen=false;document.getElementById("codeIn").type="password";
  document.getElementById("eyeIc").className="ti ti-eye";
}

document.getElementById("codeIn").addEventListener("keydown",e=>{if(e.key==="Enter")doLogin();});
</script>
