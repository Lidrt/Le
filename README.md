<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Чтение манги</title>
</head>
<body>
    <div class="container">
        <h1>Чтение манги</h1>
        <div id="manga-viewer">
            <img id="manga-image" src="" alt="Манга">
        </div>
        <div class="controls">
            <button id="prev-button">Предыдущая</button>
            <button id="next-button">Следующая</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f9f9f9;
    text-align: center;
}

.container {
    max-width: 800px;
    margin: 0 auto;
}

#manga-viewer {
    margin: 20px 0;
}

#manga-image {
    max-width: 100%;
    height: auto;
}

.controls {
    margin: 20px 0;
}
