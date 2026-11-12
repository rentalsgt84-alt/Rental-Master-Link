<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Launcher Link Saya</title>
    <style>
        /* Tema Mode Gelap Khas Android (Material You Dark) */
        body {
            background-color: #121212;
            color: #e3e3e3;
            font-family: 'Roboto', -apple-system, BlinkMacSystemFont, sans-serif;
            margin: 0;
            padding: 24px 16px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .container {
            width: 100%;
            max-width: 440px;
        }
        /* Kolom Pencarian Bulat ala Google/Android */
        .search-bar {
            width: 100%;
            padding: 14px 20px;
            border-radius: 50px;
            border: none;
            background-color: #28292a;
            color: #ffffff;
            font-size: 16px;
            outline: none;
            box-sizing: border-box;
            margin-bottom: 32px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.4);
        }
        .search-bar::placeholder {
            color: #9aa0a6;
        }
        /* Grid 4 Kolom Khas Layar Utama Android */
        .app-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 24px 12px;
        }
        .app-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-decoration: none;
            color: #e3e3e3;
            transition: transform 0.15s ease;
        }
        .app-item:active {
            transform: scale(0.92);
        }
        /* Kotak Ikon Membulat (Squircle) */
        .icon-box {
            width: 60px;
            height: 60px;
            background-color: #1e1f20;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 8px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3);
            border: 1px solid #2f3031;
        }
        .icon-box img {
            width: 30px;
            height: 30px;
        }
        .app-name {
            font-size: 12px;
            text-align: center;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            max-width: 75px;
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Kolom Ketik Cari Aplikasi/Link -->
    <input type="text" id="searchInput" class="search-bar" onkeyup="cariLink()" placeholder="🔍 Ketik nama link...">

    <!-- Daftar Ikon Grid Android -->
    <div class="app-grid" id="appGrid">
        
        <a href="https://drive.google.com" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/googledrive/4285F4" alt="Drive">
            </div>
            <span class="app-name">Drive Kerja</span>
        </a>

        <a href="https://wa.me/628123456789" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/whatsapp/25D366" alt="WA">
            </div>
            <span class="app-name">WhatsApp</span>
        </a>

        <a href="https://youtube.com" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/youtube/FF0000" alt="YouTube">
            </div>
            <span class="app-name">YouTube</span>
        </a>

        <a href="https://instagram.com" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/instagram/E4405F" alt="IG">
            </div>
            <span class="app-name">Instagram</span>
        </a>

        <a href="https://notion.so" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/notion/FFFFFF" alt="Notion">
            </div>
            <span class="app-name">Catatan</span>
        </a>

        <a href="https://canva.com" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/canva/00C4CC" alt="Canva">
            </div>
            <span class="app-name">Canva</span>
        </a>

        <a href="https://sheets.google.com" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/googlesheets/34A853" alt="Sheets">
            </div>
            <span class="app-name">Laporan</span>
        </a>

        <a href="https://t.me" target="_blank" class="app-item">
            <div class="icon-box">
                <img src="https://cdn.simpleicons.org/telegram/26A5E4" alt="Telegram">
            </div>
            <span class="app-name">Telegram</span>
        </a>

    </div>
</div>

<script>
    function cariLink() {
        const input = document.getElementById('searchInput').value.toLowerCase();
        const items = document.getElementsByClassName('app-item');
        for (let i = 0; i < items.length; i++) {
            const nama = items[i].innerText.toLowerCase();
            items[i].style.display = nama.includes(input) ? "flex" : "none";
        }
    }
</script>

</body>
</html>
