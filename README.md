# auddhkdtjd1103-jpg.github.io
<button onclick="exportMyData()" style="position:fixed; top:10px; right:10px; z-index:9999; padding:10px 14px; background:#a78bfa; color:#000; font-weight:bold; border-radius:8px; border:none; box-shadow: 0 4px 10px rgba(0,0,0,0.5);">
  📦 데이터 추출하기
</button>

<script>
function exportMyData(){
  const data = localStorage.getItem('limen_data_v1');
  if(!data){
    alert('기기에 저장된 데이터가 없습니다!');
    return;
  }
  // 복사하기 쉬운 전용 창 띄우기
  const overlay = document.createElement('div');
  overlay.style = 'position:fixed; inset:0; background:rgba(0,0,0,0.85); z-index:10000; padding:20px; display:flex; flex-direction:column; gap:10px; align-items:center; justify-content:center;';
  overlay.innerHTML = `
    <h3 style="color:#fff; margin:0;">아래 텍스트를 전체 선택해서 복사하세요</h3>
    <textarea id="myExportText" style="width:100%; height:60vh; background:#1c1c28; color:#fff; border:1px solid #2a2a38; border-radius:10px; padding:10px; font-size:12px;"></textarea>
    <button onclick="this.parentElement.remove()" style="padding:10px 20px; background:#d9707a; color:#fff; border:none; border-radius:8px;">닫기</button>
  `;
  document.body.appendChild(overlay);
  document.getElementById('myExportText').value = data;
}
</script>
