<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <style>
        body { background-color: #201319; color: white; font-family: sans-serif; display: flex; margin: 0; height: 100vh; }
        
        /* Menu Laterale */
        #sidebar { width: 250px; padding: 20px; }
        .menu-item { background: #301a24; padding: 15px; margin-bottom: 10px; cursor: pointer; border-radius: 8px; }
        .menu-item:hover { background: #5a263e; }
        
        /* Contenuto Principale */
        #content { flex-grow: 1; padding: 50px; overflow-y: auto; }
        .card { background: #120b0e; padding: 20px; border-radius: 10px; border: 1px solid #333; margin-bottom: 20px; }
        
        /* Link Stile */
        .grid { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .exp-card { background: #1a1a1a; padding: 15px; border-radius: 8px; border: 1px solid #333; text-decoration: none; color: white; display: block; }
        .exp-card:hover { border-color: #b30026; }
    </style>
</head>
<body>

    <div id="sidebar">
        <div class="menu-item" onclick="show('bio')">👤 Bio</div>
        <div class="menu-item" onclick="show('staff')">💼 Staff Experience</div>
    </div>

    <div id="content">
        <div id="bio" class="page">
            <div class="card" style="text-align: center;">
                <h2>Filmografo</h2>
                <p>🔍 DFIR & PC Checker</p>
            </div>
        </div>

        <div id="staff" class="page" style="display:none;">
            <h2>Staff Experience</h2>
            <div class="grid">
                <a href="URL_DEL_TUO_IMGUR" class="exp-card" target="_blank">
                    <h3>Hollow Bypass</h3>
                    <p>2025 - HEADQUARTERS</p>
                </a>
                <a href="URL_DEL_TUO_IMGUR" class="exp-card" target="_blank">
                    <h3>FruitMC</h3>
                    <p>2025 - SR. MOD</p>
                </a>
            </div>
        </div>
    </div>

    <audio id="bg-music" loop>
        <source src="TUO_FILE_AUDIO.mp3" type="audio/mpeg">
    </audio>

    <script>
        function show(id) {
            document.querySelectorAll('.page').forEach(p => p.style.display = 'none');
            document.getElementById(id).style.display = 'block';
            // Avvia musica al primo click
            document.getElementById('bg-music').play();
        }
    </script>
</body>
</html>
