## TASK_3

- [x] Покласти в папку будь-які зображення 1.jpg, 2.jpg, 3.jpg, 4.jpg, 5.jpg, 6.jpg, 7.jpg, 8.jpg, 9.jpg. Вивести зображення, отримане випадковим чином (Math.random)

# Зміст
- [Опис](#опис)
- [Використання](#використання)

## Опис
Програма, яка виводить випадкове зображення з папки, яка містить файли 1.jpg, 2.jpg, ..., 9.jpg.

## Використання
1. Покладіть у папку зображення з назвами 1.jpg, 2.jpg, ..., 9.jpg.
2. Додайте на вашу HTML-сторінку блок з класом `content` і кнопкою з id `button`:
    ```html
    <div class="content" id="content">
        <button class="button" id="button">НАТИСНИ</button>
    </div>
    ```
3. Додайте скрипт, який буде генерувати випадкове зображення при натисканні на кнопку:
    ```javascript
    let divContent = document.querySelector("#content");
    let createIMG = document.createElement("img");

    document.querySelector("#button").addEventListener("click", showRandomImage);
       
    function showRandomImage(event){
        event.stopPropagation();
        let randomNumber = Math.floor(Math.random() * 9) + 1;

        let srcURL = "./sours/img/" + randomNumber + ".png";
        createIMG.src = srcURL;
        createIMG.classList.add("custom-image");
            
        divContent.appendChild(createIMG);
    }
    ```
4. Виконайте відповідні дії на вашій HTML-сторінці, щоб інтегрувати цей скрипт.


