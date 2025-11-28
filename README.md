# 2400031867-SkillEndSemExam
<div class="gallery">
  <img src="p1.jpg" class="item">
  <img src="p2.jpg" class="item">
  <img src="p3.jpg" class="item">
</div>

<div id="modal" class="modal">
  <span class="close">&times;</span>
  <img id="modal-img">
</div>
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 12px;
}
.item { width: 100%; cursor: pointer; border-radius: 8px; }
.modal {
  display: none; position: fixed; inset: 0;
  background: rgba(0,0,0,0.7);
  justify-content: center; align-items: center;
}
#modal-img { width: 80%; max-width: 600px; }
.close { position: absolute; top: 20px; right: 30px; color: #fff; font-size: 35px; cursor: pointer; }
document.querySelectorAll(".item").forEach(img => {
  img.onclick = () => {
    modal.style.display = "flex";
    modal_img.src = img.src;
  };
});
close.onclick = () => modal.style.display = "none";
