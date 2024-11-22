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
const mangaImages = [
    'path/to/manga/page1.jpg', // замените на фактические пути к страницам манги
    'path/to/manga/page2.jpg',
    'path/to/manga/page3.jpg',
];

let currentPage = 0;

const mangaImage = document.getElementById('manga-image');

function updateImage() {
    mangaImage.src = mangaImages[currentPage];
}

document.getElementById('prev-button').addEventListener('click', () => {
    if (currentPage > 0) {
        currentPage--;
        updateImage();
    }
});

document.getElementById('next-button').addEventListener('click', () => {
    if (currentPage < mangaImages.length - 1) {
        currentPage++;
        updateImage();
    }
});

// Инициализация с первой страницей
updateImage();
