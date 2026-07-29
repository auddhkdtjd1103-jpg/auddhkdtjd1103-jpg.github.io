# auddhkdtjd1103-jpg.github.io
<div id="exportModal" style="display:none; position:fixed; inset:0; background:rgba(0,0,0,0.9); z-index:99999; padding:20px; box-sizing:border-box; flex-direction:column; gap:10px; align-items:center; justify-content:center;">
  <h3 style="color:#fff; margin:0;">아래 전체 내용을 복사하세요</h3>
  <textarea id="exportTextarea" style="width:100%; height:70vh; background:#1c1c28; color:#a78bfa; border:1px solid #2a2a38; border-radius:10px; padding:12px; font-size:11px; font-family:monospace; word-break:break-all;"></textarea>
  <button onclick="document.getElementById('exportModal').style.display='none'" style="padding:10px 24px; background:#d9707a; color:#fff; border:none; border-radius:8px; font-weight:bold;">닫기</button>
</div>

<button onclick="openExportModal()" style="position:fixed; top:12px; right:12px; z-index:9999; padding:10px 14px; background:#a78bfa; color:#100c1e; font-weight:bold; border-radius:8px; border:none; box-shadow:0 4px 12px rgba(0,0,0,0.5);">
  📦 내 데이터 추출
</button>

<script>
function openExportModal(){
  const data = localStorage.getItem('limen_data_v1');
  if(!data){
    alert('기기에 저장된 데이터가 없습니다.');
    return;
  }
  document.getElementById('exportTextarea').value = data;
  document.getElementById('exportModal').style.display = 'flex';
}
</script>
