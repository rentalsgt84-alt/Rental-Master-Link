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
