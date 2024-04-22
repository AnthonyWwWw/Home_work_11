## TASK_2

- [x] Є блок із текстом на сторінці та кнопку. При натисканні на кнопку текст змінює колір. При повторному натисканні повертається попередній колір

# Зміст
- [Опис](#опис)
- [Використання](#використання)

## Опис
Програма, яка міняє колір тексту при натисканні на кнопку.

## Використання
1. Додайте на вашу HTML-сторінку блок з класом `content` і вмістом наступного вигляду:
    ```html
    <div class="content">
        <div class="text" id="text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dicta quas eaque nulla blanditiis ullam dolorem, ratione placeat animi officia corrupti?</div>
        <button class="button" id="button">Змінити колір</button>
    </div>
    ```
2. Додайте скрипт, який буде обробляти натискання на кнопку і змінювати колір тексту. Наприклад:
    ```javascript
    let statysButton = true;

    document.querySelector("#button").addEventListener("click", function(){
        let text = document.querySelector("#text");

        if (statysButton){
            text.style.color = "red";
            statysButton = false;
        }else{
            text.style.color = "black";
            statysButton = true;
        }
    });
    ```
3. Виконайте відповідні дії на вашій HTML-сторінці, щоб інтегрувати цей скрипт.
