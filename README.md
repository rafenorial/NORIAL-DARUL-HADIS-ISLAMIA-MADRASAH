[নড়িয়াল দারুল হাদীস ইসলামিয়া মাদ্রাসা.html](https://github.com/user-attachments/files/24909333/default.html)
<!DOCTYPE html>
<html lang="bn">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>অ্যাডমিশন ও এক্সাম পোর্টাল | নড়িয়াল মাদ্রাসা</title>

    <!-- Font Awesome & Google Fonts -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Hind+Siliguri:wght@300;400;600;700&display=swap" rel="stylesheet">

    <style>
        :root { 
            --primary: #003366; 
            --accent: #fbc02d; 
            --bg: #f4f7f9; 
            --white: #ffffff;
            --success: #28a745;
            --info: #17a2b8;
        }

        body { font-family: 'Hind Siliguri', sans-serif; background: var(--bg); margin: 0; padding: 0; color: #333; line-height: 1.6; }

        /* Header Style */
        header { 
            background: var(--white); border-top: 6px solid var(--primary); padding: 20px; 
            text-align: center; box-shadow: 0 2px 10px rgba(0,0,0,0.1); position: relative; 
        }

        .estd-tag { 
            position: absolute; top: 10px; left: 20px; background: var(--primary); 
            color: white; padding: 4px 12px; border-radius: 4px; font-weight: bold; font-size: 13px; 
        }

        .header-top-info {
            display: flex; justify-content: center; gap: 40px; margin-top: 15px; flex-wrap: wrap;
        }
        .leader-card {
            display: flex; align-items: center; gap: 10px; background: #f9f9f9; padding: 8px 15px; border-radius: 50px; border: 1px solid #eee;
        }
        .leader-card img {
            width: 45px; height: 45px; border-radius: 50%; object-fit: cover; border: 2px solid var(--primary); background: #ddd;
        }
        .leader-info { text-align: left; line-height: 1.2; }
        .leader-info small { font-size: 11px; color: #666; font-weight: bold; }
        .leader-info div { font-size: 14px; font-weight: bold; color: var(--primary); }

        nav { 
            background: var(--primary); display: flex; justify-content: center; flex-wrap: wrap;
            position: sticky; top: 0; z-index: 1000; box-shadow: 0 2px 5px rgba(0,0,0,0.2); 
        }
        nav a { 
            color: white; text-decoration: none; font-weight: bold; padding: 15px 20px; 
            transition: 0.3s; cursor: pointer; border-right: 1px solid rgba(255,255,255,0.1); 
        }
        nav a:hover { background: var(--accent); color: var(--primary); }

        .container { max-width: 1100px; margin: 30px auto; background: white; padding: 40px; border-radius: 12px; box-shadow: 0 5px 25px rgba(0,0,0,0.08); }
        .hidden { display: none; }

        /* Notice Board */
        .notice-wrapper { background: #fffbe6; border: 1px solid #ffe58f; padding: 15px; border-radius: 8px; margin-bottom: 30px; display: flex; align-items: center; gap: 15px; }
        .notice-label { background: #f5222d; color: white; padding: 4px 12px; border-radius: 4px; font-weight: bold; animation: blinker 1.5s linear infinite; }
        @keyframes blinker { 50% { opacity: 0; } }

        /* Step Progress */
        .steps-bar { display: flex; justify-content: space-between; margin-bottom: 40px; background: #f8f9fa; padding: 20px; border-radius: 50px; border: 1px solid #eee; }
        .step-item { display: flex; align-items: center; gap: 10px; color: #999; font-weight: bold; font-size: 16px; }
        .step-item.active { color: var(--primary); }
        .step-item.done { color: var(--success); }

        /* Form Styling */
        .form-section { border: 1px solid #eee; margin-bottom: 25px; border-radius: 8px; overflow: hidden; }
        .form-section-title { background: #f0f4f8; padding: 12px 20px; border-bottom: 1px solid #eee; font-weight: bold; color: var(--primary); }
        .form-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; padding: 20px; }
        input, select, textarea { width: 100%; padding: 12px; border: 1px solid #ccc; border-radius: 6px; box-sizing: border-box; font-family: 'Hind Siliguri'; font-size: 15px; }

        .btn-nu { background: var(--primary); color: white; padding: 12px 20px; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; transition: 0.3s; }
        .btn-nu:hover { opacity: 0.9; transform: translateY(-1px); }
        .btn-full { width: 100%; font-size: 18px; padding: 15px; margin-top: 10px; }

        .nu-table { width: 100%; border-collapse: collapse; margin-top: 15px; }
        .nu-table th { background: var(--primary); color: white; padding: 12px; text-align: left; }
        .nu-table td { padding: 10px; border-bottom: 1px solid #eee; }

        #photoPreview { width: 100px; height: 120px; border: 2px dashed #ccc; display: flex; align-items: center; justify-content: center; margin-top: 10px; }
        #photoPreview img { width: 100%; height: 100%; object-fit: cover; }

        @media print {
            nav, header, .btn-nu, .admin-controls-ui, .steps-bar, #no-print { display: none !important; }
        }
    </style>
</head>
<body>

<header>
    <div class="estd-tag">স্থাপিত: ১৯২৭ ইং</div>
    <h1 style="margin:0;">নড়িয়াল দারুল হাদীস ইসলামিয়া মাদ্রাসা</h1>
    <p style="font-weight: bold; color: var(--primary); margin:5px 0;">সেশন: <span id="headerSession"></span></p>
    
    <div class="header-top-info">
        <div class="leader-card">
            <img id="headImgDisp" src="" alt="">
            <div class="leader-info">
                <small>প্রধান শিক্ষক</small>
                <div id="headNameDisp">লোড হচ্ছে...</div>
                <div id="headNumDisp">...</div>
            </div>
        </div>
        <div class="leader-card">
            <img id="presImgDisp" src="" alt="">
            <div class="leader-info">
                <small>সভাপতি</small>
                <div id="presNameDisp">লোড হচ্ছে...</div>
                <div id="presNumDisp">...</div>
            </div>
        </div>
    </div>
</header>

<nav id="no-print">
    <a onclick="showSection('home')"><i class="fas fa-home"></i> মূল পাতা</a>
    <a onclick="showSection('admission')"><i class="fas fa-user-plus"></i> অনলাইন ভর্তি</a>
    <a onclick="showSection('tracking')"><i class="fas fa-search"></i> আবেদনের অবস্থা</a>
    <a onclick="showSection('admit-card-sec')"><i class="fas fa-id-card"></i> এডমিট কার্ড</a>
    <a onclick="showSection('result-sec')"><i class="fas fa-file-invoice"></i> ফলাফল</a>
    <a onclick="navAdmin()"><i class="fas fa-lock"></i> এডমিন</a>
</nav>

<!-- Home Section -->
<div class="container" id="home">
    <div class="notice-wrapper">
        <div class="notice-label">নোটিশ :</div>
        <div id="displayNotice">লোড হচ্ছে...</div>
    </div>

    <div style="background:var(--primary); color:white; padding:10px; text-align:center; font-weight:bold; border-radius:8px 8px 0 0;">About Us</div>
    <div style="border:1px solid #ddd; padding:25px; text-align:justify; background:#fff; font-size:16px; line-height: 1.8;">
        শিক্ষা মানব সমাজের সবচেয়ে মূল্যবান সম্পদ। ভালো চাকরি প্রাপ্তি, দারিদ্র্যমুক্ত সমাজ প্রতিষ্ঠা, উন্নত দেশ গঠন, সভ্য জাতি বিনির্মাণ সবকিছুর মূলমন্ত্র হচ্ছে শিক্ষা। বর্তমানে দেশে আগের তুলনায় শিক্ষিতের হার অনেক বেড়েছে। এখন সবাই শিক্ষার গুরুত্ব বুঝেন। পিতা-মাতা নিজের অর্জিত অধিকাংশ সম্পদ সন্তানের লেখাপড়ায় ব্যয় করেন। এস.এস.সি, এইচ.এস.সি পরীক্ষায় সন্তানের জি.পি.এ-৫ অর্জনের জন্য নির্দ্বিধায় টাকা ব্যয় করে যান। তাদেরকে বিভিন্ন সরকারি-বেসরকারি বিশ্ববিদ্যালয়, মেডিকেল ও ইঞ্জিনিয়ারিং বিশ্ববিদ্যালয় ও কলেজে ভর্তি করাতে লক্ষ লক্ষ টাকা খরচ করেন। আইন, চিকিৎসা বিজ্ঞান, ইঞ্জিনিয়ারিং, বি.বি.এ, এম.বি.এ ইত্যাদি বিষয়ে উচ্চ ডিগ্রি অর্জনের জন্য তাদের বিদেশে পাঠান। কিন্তু এত কিছুর ফলাফল কী? এদেশে প্রয়োজন এমন শিক্ষা প্রতিষ্ঠান, যা সাড়ে চৌদ্দশত বছর পূর্বের শিরক-বিদ’আত মুক্ত ইসলামকে সমাজে প্রতিষ্ঠা করবে। যে প্রতিষ্ঠানের শিক্ষার্থীরা হবে সত্য ও ন্যায়ের উজ্জ্বল নক্ষত্র। পবিত্র কুরআন ও ছহীহ হাদীছের আদর্শে উজ্জীবিত দুর্জয় কারী। সালাফে-ছালেহীনের আদর্শের ধারক-বাহক এবং ইসলামের বিশুদ্ধ আকীদা রক্ষার অতন্দ্র প্রহরী। একবিংশ শতাব্দীতে ইসলাম বিরোধী যে কোনো চ্যালেঞ্জ মোকাবেলা করতে সক্ষম হবে। মিথ্যা ও ভ্রান্তি থেকে উত্তরণের ক্ষেত্রে মুক্তিকামী মানুষের আস্থার প্রতীক। প্রগতি ও অবাধ স্বাধীনতার বিষাক্ত ছোবলে আক্রান্ত জনতাকে তারা মুক্তির মোহনায় পৌঁছিয়ে দেবে এবং পাপ-পঙ্কিলতা আর অন্যায়ে নিমজ্জিত জনগোষ্ঠীকে ইসলামের ছায়াতলে আশ্রয় দেবে। এই প্রতিষ্ঠান থেকে লেখক, গবেষক, বাগ্মী বের হবে এবং কুরআন ও ছহীহ হাদীছের পতাকা নিয়ে দেশে-বিদেশে ছুটে বেড়াবে। বাংলাদেশসহ বিশ্বের প্রতিটি ঘরে ঘরে সত্যিকার ইসলামের দা’ওয়াত পৌঁছানোর বিরামহীন প্রচেষ্টা চালাবে।
    </div>
</div>

<!-- Admission Workflow -->
<div class="container hidden" id="admission">
    <div class="steps-bar">
        <div class="step-item active" id="st1">১. তথ্য প্রদান</div>
        <div class="step-item" id="st2">২. পেমেন্ট</div>
        <div class="step-item" id="st3">৩. সম্পন্ন</div>
    </div>

    <div id="admissionFormArea">
        <div class="form-section">
            <div class="form-section-title">ব্যক্তিগত তথ্য (সেশন: <span class="autoSession"></span>)</div>
            <div class="form-grid">
                <input type="text" id="sNameBN" placeholder="শিক্ষার্থীর নাম (বাংলা) *">
                <input type="text" id="sNameEN" placeholder="Student Name (English) *">
                <div class="form-group"><label>জন্ম তারিখ *</label><input type="date" id="sDOB"></div>
                <input type="number" id="sBirthReg" placeholder="জন্ম নিবন্ধন নং *">
                <select id="sClass">
                    <option value="">শ্রেণি নির্বাচন করুন *</option>
                    <option>Class-1</option><option>Class-2</option><option>Class-3</option><option>নুরানী</option><option>হেফজ</option>
                </select>
                <select id="sBranch"><option>বালক শাখা</option><option>বালিকা শাখা</option></select>
                <div class="form-group"><label>ছবি আপলোড *</label><input type="file" id="sPhoto" accept="image/*"><div id="photoPreview">ছবি</div></div>
            </div>
        </div>
        <div class="form-section">
            <div class="form-section-title">অভিভাবক ও ঠিকানা</div>
            <div class="form-grid">
                <input type="text" id="fName" placeholder="পিতার নাম *">
                <input type="number" id="fPhone" placeholder="পিতার মোবাইল নং *">
                <input type="text" id="mName" placeholder="মাতার নাম *">
                <textarea id="addrGram" placeholder="পূর্ণ ঠিকানা (গ্রাম, ডাকঘর, উপজেলা, জেলা) *" rows="2"></textarea>
            </div>
        </div>
        <button class="btn-nu btn-full" onclick="goToPayment()">পরবর্তী ধাপ (পেমেন্ট)</button>
    </div>

    <div id="admissionPaymentArea" class="hidden" style="text-align:center;">
        <h3>ভর্তি ফি: ৩০০ টাকা</h3>
        <p>টাকা পাঠানোর জন্য ওপরের প্রধান শিক্ষক বা সভাপতির নম্বরে যোগাযোগ করুন।</p>
        <div style="max-width:400px; margin:auto; text-align:left; border:1px solid #ddd; padding:20px; border-radius:10px;">
            <select id="payMethod" style="margin-bottom:10px;"><option>বিকাশ</option><option>নগদ</option></select>
            <input type="number" id="paySender" placeholder="প্রেরক মোবাইল নম্বর *" style="margin-bottom:10px;">
            <input type="text" id="payTrx" placeholder="Transaction ID (TrxID) *" style="margin-bottom:10px; text-transform:uppercase;">
            <button class="btn-nu btn-full" onclick="finalSubmit()">আবেদন সম্পন্ন করুন</button>
        </div>
    </div>

    <div id="admissionSuccessArea" class="hidden" style="text-align:center; padding:50px;">
        <i class="fas fa-check-circle" style="font-size:70px; color:var(--success);"></i>
        <h2>আবেদন সফল হয়েছে!</h2>
        <p>রোল নম্বর: <b id="successRoll" style="font-size:24px; color:var(--primary);"></b></p>
        <button class="btn-nu" onclick="printFullFormWithReceipt()">ভর্তি ফরম ও রিসিট প্রিন্ট</button>
    </div>
</div>

<!-- Admit Card Section -->
<div class="container hidden" id="admit-card-sec">
    <h2 style="text-align:center;"><i class="fas fa-id-card"></i> প্রবেশপত্র ডাউনলোড</h2>
    <div style="max-width:500px; margin:40px auto; border:1px solid #eee; padding:30px; border-radius:10px; background:#f9f9f9;">
        <input type="number" id="admitRollInp" placeholder="রোল নম্বর দিন" style="margin-bottom:20px;">
        <div style="display:grid; grid-template-columns: 1fr 1fr; gap:10px;">
            <button class="btn-nu" onclick="publicPrintAdmit('অর্ধবার্ষিক')" style="background:var(--info);">অর্ধবার্ষিক</button>
            <button class="btn-nu" onclick="publicPrintAdmit('বার্ষিক')" style="background:var(--primary);">বার্ষিক</button>
        </div>
    </div>
    <div id="admitStatusMsg" style="text-align:center; margin-top:10px;"></div>
</div>

<!-- Admin Panel -->
<div class="container hidden" id="login-sec">
    <div style="max-width:350px; margin:auto; text-align:center;">
        <h3>এডমিন লগইন</h3>
        <input type="password" id="admPass" placeholder="পাসওয়ার্ড" style="margin-bottom:15px;">
        <button class="btn-nu btn-full" onclick="login()">প্রবেশ</button>
    </div>
</div>

<div class="container hidden" id="admin">
    <button onclick="logout()" style="float:right;" class="btn-nu">লগআউট</button>
    <h2>এডমিন ড্যাশবোর্ড</h2>
    
    <!-- Config Section -->
    <div class="form-section">
        <div class="form-section-title">হেডার ও কন্ট্রাক্ট আপডেট</div>
        <div class="form-grid">
            <div><label>প্রধান শিক্ষক নাম</label><input type="text" id="setHeadName"></div>
            <div><label>প্রধান শিক্ষক মোবাইল</label><input type="text" id="setHeadNum"></div>
            <div><label>প্রধান শিক্ষক ছবি (File)</label><input type="file" id="setHeadImg" accept="image/*"></div>
            
            <div><label>সভাপতি নাম</label><input type="text" id="setPresName"></div>
            <div><label>সভাপতি মোবাইল</label><input type="text" id="setPresNum"></div>
            <div><label>সভাপতি ছবি (File)</label><input type="file" id="setPresImg" accept="image/*"></div>

            <div style="grid-column: span 1;"><label>নোটিশ আপডেট</label><input type="text" id="setNotice"></div>
        </div>
        <button class="btn-nu" style="width:150px; margin:15px;" onclick="saveConfig()">সব আপডেট করুন</button>
    </div>

    <div class="form-section">
        <div class="form-section-title">আবেদনকারী তালিকা</div>
        <div style="overflow-x:auto;"><table class="nu-table"><thead><tr><th>রোল</th><th>নাম</th><th>শ্রেণি</th><th>অবস্থা</th><th>অ্যাকশন</th></tr></thead><tbody id="admStuBody"></tbody></table></div>
    </div>

    <div class="form-section">
        <div class="form-section-title">মার্কস এন্ট্রি (১৩টি বিষয়)</div>
        <div id="subInputs" class="form-grid" style="grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));"></div>
        <div style="padding:20px;"><input type="number" id="mRoll" placeholder="রোল" style="width:150px; margin-right:10px;"><button class="btn-nu" onclick="saveMarks()">সেভ মার্কস</button></div>
    </div>
</div>

<!-- Extra Sections -->
<div class="container hidden" id="tracking">
    <h2 style="text-align:center;">আবেদনের অবস্থা</h2>
    <div style="max-width:500px; margin:auto; display:flex; gap:10px;"><input type="text" id="trackInp" placeholder="রোল নম্বর"><button class="btn-nu" onclick="checkStatus()">খুঁজুন</button></div>
    <div id="trackResult" style="margin-top:30px;"></div>
</div>
<div class="container hidden" id="result-sec">
    <h2 style="text-align:center;">ফলাফল অনুসন্ধান</h2>
    <div style="max-width:500px; margin:auto; display:flex; gap:10px;"><input type="number" id="resRoll" placeholder="রোল নম্বর"><button class="btn-nu" onclick="searchResult()">খুঁজুন</button></div>
    <div id="resultDisplay"></div>
</div>

<script>
    const subList = ["কালিমা ও আসমা-উল হুসনা", "আরবী লেখা / আরবী শিক্ষা", "হাদীস শরীফ", "মাসায়িল", "হিফজুল কোরআন", "আদইয়ায়ে মাসনুন", "তাজবীদ ও মাখরাজ", "বাংলা", "গণিত", "ইংরেজী", "পরিবেশ পরিচিতি", "সমাজ", "বিজ্ঞান"];
    
    const Guard = {
        save: (key, val) => localStorage.setItem(key, btoa(unescape(encodeURIComponent(JSON.stringify(val))))),
        load: (key) => {
            const data = localStorage.getItem(key);
            if(!data) return null;
            try { return JSON.parse(decodeURIComponent(escape(atob(data)))); } catch(e) { return null; }
        }
    };

    let students = Guard.load('nu_mad_v9') || [];
    let marks = Guard.load('nu_marks_v9') || {};
    let config = Guard.load('nu_conf_v9') || { 
        notice: "ভর্তি চলছে।", 
        headName: "মাওলানা আব্দুল্লাহ", headNum: "01340-666396", headImg: "",
        presName: "আলহাজ্ব আব্দুর রহমান", presNum: "01724-399963", presImg: ""
    };
    let tempPhoto = "";
    let tempHeadImg = config.headImg;
    let tempPresImg = config.presImg;

    function getSession() { return `${new Date().getFullYear()}-${(new Date().getFullYear()+1).toString().slice(-2)}`; }

    function showSection(id) {
        document.querySelectorAll('.container').forEach(c => c.classList.add('hidden'));
        document.getElementById(id).classList.remove('hidden');
        if(id === 'home') loadHeaderConfig();
        if(id === 'admin') renderAdminTable();
        window.scrollTo(0,0);
    }

    // Photo Handlers
    document.getElementById('sPhoto').addEventListener('change', (e) => {
        const reader = new FileReader();
        reader.onload = () => { tempPhoto = reader.result; document.getElementById('photoPreview').innerHTML = `<img src="${tempPhoto}">`; };
        reader.readAsDataURL(e.target.files[0]);
    });
    document.getElementById('setHeadImg').addEventListener('change', (e) => {
        const reader = new FileReader();
        reader.onload = () => { tempHeadImg = reader.result; };
        reader.readAsDataURL(e.target.files[0]);
    });
    document.getElementById('setPresImg').addEventListener('change', (e) => {
        const reader = new FileReader();
        reader.onload = () => { tempPresImg = reader.result; };
        reader.readAsDataURL(e.target.files[0]);
    });

    function loadHeaderConfig() {
        document.getElementById('displayNotice').innerText = config.notice;
        document.getElementById('headNameDisp').innerText = config.headName;
        document.getElementById('headNumDisp').innerText = config.headNum;
        document.getElementById('headImgDisp').src = config.headImg || 'https://via.placeholder.com/50';
        
        document.getElementById('presNameDisp').innerText = config.presName;
        document.getElementById('presNumDisp').innerText = config.presNum;
        document.getElementById('presImgDisp').src = config.presImg || 'https://via.placeholder.com/50';
    }

    function saveConfig() {
        config.headName = document.getElementById('setHeadName').value;
        config.headNum = document.getElementById('setHeadNum').value;
        config.headImg = tempHeadImg;
        config.presName = document.getElementById('setPresName').value;
        config.presNum = document.getElementById('setPresNum').value;
        config.presImg = tempPresImg;
        config.notice = document.getElementById('setNotice').value;
        Guard.save('nu_conf_v9', config);
        alert("সব আপডেট হয়েছে!");
        loadHeaderConfig();
    }

    // Previous Logic Integration
    function goToPayment() {
        if(!document.getElementById('sNameBN').value || !tempPhoto) return alert("তথ্য অসম্পূর্ণ!");
        document.getElementById('admissionFormArea').classList.add('hidden');
        document.getElementById('admissionPaymentArea').classList.remove('hidden');
        document.getElementById('st1').classList.replace('active', 'done');
        document.getElementById('st2').classList.add('active');
    }

    function finalSubmit() {
        if(!document.getElementById('payTrx').value) return alert("TrxID দিন!");
        const roll = students.length + 10001;
        const stu = {
            roll: roll, nameBN: document.getElementById('sNameBN').value, nameEN: document.getElementById('sNameEN').value,
            class: document.getElementById('sClass').value, branch: document.getElementById('sBranch').value,
            dob: document.getElementById('sDOB').value, reg: document.getElementById('sBirthReg').value,
            fName: document.getElementById('fName').value, mName: document.getElementById('mName').value,
            fPhone: document.getElementById('fPhone').value, addr: document.getElementById('addrGram').value,
            photo: tempPhoto, trx: document.getElementById('payTrx').value, status: 'Pending', session: getSession(), date: new Date().toLocaleDateString('bn-BD')
        };
        students.push(stu); Guard.save('nu_mad_v9', students);
        document.getElementById('successRoll').innerText = roll;
        document.getElementById('admissionPaymentArea').classList.add('hidden');
        document.getElementById('admissionSuccessArea').classList.remove('hidden');
    }

    function publicPrintAdmit(type) {
        const roll = document.getElementById('admitRollInp').value;
        const s = students.find(x => x.roll == roll);
        if(!s || s.status !== 'Verified') return alert("রোল নেই বা ভেরিফাই হয়নি!");
        printExamAdmitLogic(s, type);
    }

    function printExamAdmitLogic(s, type) {
        const win = window.open('', '', 'width=800,height=900');
        let subRows = subList.map((sub, i) => `<tr><td style="border:1px solid #000; padding:5px; text-align:center;">${i+1}</td><td style="border:1px solid #000; padding:5px;">${sub}</td><td style="border:1px solid #000; padding:5px;"></td></tr>`).join('');
        win.document.write(`<html><body style="font-family:'Hind Siliguri'; padding:20px;"><div style="border:5px double #003366; padding:20px; position:relative; min-height:90vh;"><center><h2>নড়িয়াল দারুল হাদীস ইসলামিয়া মাদ্রাসা</h2><p>সেশন: ${s.session}</p><h3 style="background:#eee; padding:5px;">প্রবেশপত্র: ${type} পরীক্ষা</h3></center><img src="${s.photo}" style="position:absolute; top:80px; right:30px; width:100px; height:120px; border:1px solid #000;"><div style="margin-top:30px;"><p><b>নাম:</b> ${s.nameBN}</p><p><b>রোল:</b> ${s.roll} &nbsp;&nbsp; <b>শ্রেণি:</b> ${s.class}</p></div><table style="width:100%; border-collapse:collapse; margin-top:20px;"><thead><tr style="background:#f2f2f2;"><th style="border:1px solid #000; width:10%;">নং</th><th style="border:1px solid #000; text-align:left; padding:5px;">বিষয়সমূহ</th><th style="border:1px solid #000; width:25%;">স্বাক্ষর</th></tr></thead><tbody>${subRows}</tbody></table></div><script>window.onload=function(){window.print();window.close();}<\/script></body></html>`);
    }

    function navAdmin() { if(localStorage.getItem('_adm_v9')) { populateAdminConfig(); showSection('admin'); } else showSection('login-sec'); }
    function login() { if(document.getElementById('admPass').value === '127117') { localStorage.setItem('_adm_v9', 'true'); populateAdminConfig(); showSection('admin'); } else alert("ভুল!"); }
    function logout() { localStorage.removeItem('_adm_v9'); showSection('home'); }

    function populateAdminConfig() {
        document.getElementById('setHeadName').value = config.headName;
        document.getElementById('setHeadNum').value = config.headNum;
        document.getElementById('setPresName').value = config.presName;
        document.getElementById('setPresNum').value = config.presNum;
        document.getElementById('setNotice').value = config.notice;
    }

    function renderAdminTable() {
        const tbody = document.getElementById('admStuBody'); tbody.innerHTML = '';
        students.forEach((s, i) => {
            tbody.innerHTML += `<tr><td>${s.roll}</td><td>${s.nameBN}</td><td>${s.class}</td><td>${s.status}</td><td><button class="btn-nu" style="background:green; padding:5px;" onclick="verifyStu(${i})">Verify</button></td></tr>`;
        });
    }
    function verifyStu(i) { students[i].status = 'Verified'; Guard.save('nu_mad_v9', students); renderAdminTable(); }

    const si = document.getElementById('subInputs'); subList.forEach(s => si.innerHTML += `<div><label style="font-size:11px; font-weight:bold;">${s}</label><input type="number" class="m-val"></div>`);
    function saveMarks() {
        const r = document.getElementById('mRoll').value; const s = students.find(x => x.roll == r);
        if(!s) return alert("রোল নেই!");
        let mArr = []; document.querySelectorAll('.m-val').forEach(v => mArr.push(v.value || 0));
        marks[r + "_" + s.session] = mArr; Guard.save('nu_marks_v9', marks); alert("সেভ হয়েছে!");
    }

    function searchResult() {
        const r = document.getElementById('resRoll').value; const s = students.find(x => x.roll == r);
        if(!s) return alert("পাওয়া যায়নি!");
        const d = marks[r + "_" + s.session]; if(!d) return alert("রেজাল্ট নেই!");
        let rows = subList.map((sub, i) => `<tr><td>${sub}</td><td>${d[i]}</td></tr>`).join('');
        document.getElementById('resultDisplay').innerHTML = `<div style="border:2px solid var(--primary); padding:20px;"><h3>মার্কশীট: ${s.nameBN}</h3><table class="nu-table">${rows}</table></div>`;
    }

    function printFullFormWithReceipt() {
        const r = document.getElementById('successRoll').innerText;
        const s = students.find(x => x.roll == r);
        const win = window.open('', '', 'width=800,height=900');
        win.document.write(`<html><body style="font-family:'Hind Siliguri'; padding:30px;"><div style="border:2px solid #000; padding:20px;"><h2>ভর্তি আবেদন ফরম - ${s.session}</h2><p>রোল: ${s.roll}</p><p>নাম: ${s.nameBN}</p><hr><p>৩০০/- টাকা পরিশোধিত।</p></div><script>window.onload=function(){window.print();window.close();}<\/script></body></html>`);
    }

    window.onload = () => {
        document.getElementById('headerSession').innerText = getSession();
        document.querySelectorAll('.autoSession').forEach(e => e.innerText = getSession());
        loadHeaderConfig();
        showSection('home');
    };
</script>
</body>
</html>
