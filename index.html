<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Photos</title>
<!-- Firebase SDKs -->
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
<style>
  body { margin:0; font-family:'Inter',sans-serif; background:#f5f5f5; color:#333; }
  header { position:fixed; top:0; left:0; right:0; height:70px; background:white; display:flex; justify-content:space-between; align-items:center; padding:0 30px; box-shadow:0 2px 10px rgba(0,0,0,0.08); z-index:100; border-bottom-left-radius:10px; border-bottom-right-radius:10px;}
  header h1 { margin:0; font-size:1.7em; font-weight:600; }
  header .auth-buttons button { margin-left:10px; padding:8px 16px; border:none; border-radius:25px; cursor:pointer; font-weight:600; background:#667eea; color:white; transition:0.3s; }
  header .auth-buttons button:hover{ transform:scale(1.05); box-shadow:0 4px 12px rgba(0,0,0,0.2); }
  header .auth-buttons button.google{ background:#DB4437; }
  #main { margin-top:90px; padding:20px; max-width:1000px; margin-left:auto; margin-right:auto; }
  #drop-area { width:100%; min-height:160px; border:2px dashed #bbb; border-radius:12px; display:flex; justify-content:center; align-items:center; color:#666; font-size:1.2em; background:white; cursor:pointer; margin-bottom:25px; transition:0.3s; box-shadow:0 2px 5px rgba(0,0,0,0.05); }
  #drop-area:hover { border-color:#667eea; box-shadow:0 8px 20px rgba(0,0,0,0.1); transform:translateY(-2px); }
  #gallery { display:grid; grid-template-columns:repeat(auto-fill,minmax(220px,1fr)); gap:15px; }
  #gallery img { width:100%; display:block; border-radius:12px; transition: transform 0.3s, box-shadow 0.3s; cursor:pointer; box-shadow:0 2px 5px rgba(0,0,0,0.05); }
  #gallery img:hover { transform: scale(1.03); box-shadow:0 10px 20px rgba(0,0,0,0.15); }
  #auth-modal { display:none; position:fixed; top:0; left:0; right:0; bottom:0; background:rgba(0,0,0,0.6); display:flex; justify-content:center; align-items:center; z-index:200; }
  #auth-modal .modal-content { background:white; padding:30px; border-radius:16px; width:320px; text-align:center; box-shadow:0 10px 25px rgba(0,0,0,0.2); }
  #auth-modal h2{ margin-top:0; margin-bottom:20px; font-weight:600; }
  #auth-modal input{ width:100%; margin-bottom:12px; padding:10px; border:1px solid #ccc; border-radius:8px; font-size:1em; }
  #auth-modal button{ width:100%; padding:10px; border:none; border-radius:25px; background:#667eea; color:white; font-weight:600; cursor:pointer; transition:0.3s; }
  #auth-modal button:hover{ transform:scale(1.03); box-shadow:0 5px 15px rgba(0,0,0,0.2); }
  #auth-modal a{ font-size:0.9em; color:#667eea; text-decoration:none; display:block; margin-top:10px; }
</style>
</head>
<body>

<header>
  <h1>My Photos</h1>
  <div class="auth-buttons">
    <button onclick="showLogin()">ログイン</button>
    <button onclick="showSignup()">新規登録</button>
    <button class="google" onclick="loginWithGoogle()">Google</button>
  </div>
</header>

<div id="main">
  <div id="drop-area">ここに画像をドラッグ＆ドロップ、またはクリック</div>
  <input type="file" id="fileElem" multiple style="display:none">
  <div id="gallery"></div>
</div>

<div id="auth-modal">
  <div class="modal-content">
    <h2 id="auth-title">ログイン</h2>
    <input type="email" id="email" placeholder="メール">
    <input type="password" id="password" placeholder="パスワード">
    <button id="auth-submit">送信</button>
    <a href="#" onclick="closeAuth()">閉じる</a>
  </div>
</div>

<script>
  // Firebase初期化
  const firebaseConfig = {
    apiKey: "AIzaSyBtHs722o6_JWvbgIo5rHuAGEcnNiGqFhg",
    authDomain: "aaaaaa-d2ab0.firebaseapp.com",
    projectId: "aaaaaa-d2ab0",
  };
  firebase.initializeApp(firebaseConfig);
  const auth = firebase.auth();

  function showLogin(){ 
    document.getElementById('auth-modal').style.display='flex'; 
    document.getElementById('auth-title').innerText='ログイン'; 
    document.getElementById('auth-submit').onclick=login; 
  }
  function showSignup(){ 
    document.getElementById('auth-modal').style.display='flex'; 
    document.getElementById('auth-title').innerText='新規登録'; 
    document.getElementById('auth-submit').onclick=signup; 
  }
  function closeAuth(){ document.getElementById('auth-modal').style.display='none'; }

  function signup(){ 
    const email = document.getElementById('email').value; 
    const pw = document.getElementById('password').value; 
    auth.createUserWithEmailAndPassword(email, pw)
      .then(()=>{ alert('登録成功'); closeAuth(); })
      .catch(e=>alert(e.message)); 
  }
  function login(){ 
    const email = document.getElementById('email').value; 
    const pw = document.getElementById('password').value; 
    auth.signInWithEmailAndPassword(email, pw)
      .then(()=>{ alert('ログイン成功'); closeAuth(); })
      .catch(e=>alert(e.message)); 
  }

  function loginWithGoogle(){
    const provider = new firebase.auth.GoogleAuthProvider();
    auth.signInWithPopup(provider)
      .then(result=>{
        alert('Googleログイン成功: ' + result.user.email);
        closeAuth();
      })
      .catch(e=>{ alert('Googleログインエラー: ' + e.message); });
  }

  auth.onAuthStateChanged(user => { 
    if(user){ console.log('ログイン中:', user.email); } 
    else { console.log('ログアウト'); } 
  });

  // Cloudinaryアップロード
  const cloudName = "dqud9tdr8";
  const uploadPreset = "annkomoti";

  const dropArea = document.getElementById('drop-area');
  const fileElem = document.getElementById('fileElem');
  dropArea.addEventListener('click',()=>fileElem.click());
  dropArea.addEventListener('dragover', e=>{ e.preventDefault(); dropArea.style.borderColor='#667eea'; });
  dropArea.addEventListener('dragleave', e=>{ e.preventDefault(); dropArea.style.borderColor='#bbb'; });
  dropArea.addEventListener('drop', e=>{ e.preventDefault(); dropArea.style.borderColor='#bbb'; handleFiles(e.dataTransfer.files); });
  fileElem.addEventListener('change', e=>handleFiles(e.target.files));

  async function handleFiles(files){
    if (!files.length) return;
    const user = auth.currentUser;
    if(!user){ alert('ログインしてください'); return; }

    for (let file of files){
      const formData = new FormData();
      formData.append('file', file);
      formData.append('upload_preset', uploadPreset);
      formData.append('folder', 'private_photos/' + user.uid);

      try{
        const res = await fetch(`https://api.cloudinary.com/v1_1/${cloudName}/upload`, {
          method:'POST',
          body: formData
        });
        const data = await res.json();
        const img = document.createElement('img');
        img.src = data.secure_url;
        document.getElementById('gallery').appendChild(img);
      }catch(err){
        alert('アップロードエラー: ' + err.message);
      }
    }
  }
</script>

</body>
</html>
