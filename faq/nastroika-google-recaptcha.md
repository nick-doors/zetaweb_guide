# Настройка Google ReCaptcha

На сайте есть возможность использования проверки пользователя с помощью  [ReCaptcha от Google](https://www.google.com/recaptcha/intro/v3beta.html). Для настройки необходимо получить ключи: ключ и секретный ключ.

Перейдите на страницу [Управления ключами ReCaptcha API](https://www.google.com/recaptcha/admin#list), предварительно необходимо иметь аккаунт Google и авторизоваться. 

В форме Регистрации сайта укажите название сайта,  выберите тип  reCAPTCHA v2, укажите домены и домен localhost, примите условия использования. После нажатия кнопки Регистрация, Вам станут доступны ключи для настройки на сайте. 

![&#x424;&#x43E;&#x440;&#x43C;&#x430; &#x440;&#x435;&#x433;&#x438;&#x441;&#x442;&#x440;&#x430;&#x446;&#x438;&#x438; &#x441;&#x430;&#x439;&#x442;&#x430;](../.gitbook/assets/image%20%2839%29.png)

{% hint style="info" %}
Домен localhost необходим для режима отладки на сайте. 
{% endhint %}

![&#x41A;&#x43B;&#x44E;&#x447;&#x438; &#x434;&#x43B;&#x44F; &#x43D;&#x430;&#x441;&#x442;&#x440;&#x43E;&#x439;&#x43A;&#x438; &#x43D;&#x430; &#x441;&#x430;&#x439;&#x442;&#x435;](../.gitbook/assets/image%20%2811%29.png)

В шаблоне контрола разместите часть \[GRecaptcha\]. В качестве значения параметра sitekey укажите **Ключ**, для параметра key - **Секретный ключ**.

![](../.gitbook/assets/image%20%2881%29.png)

```text
[GRecaptcha options="{ 'sitekey': '<...ключ...>' }" key="<...секретный ключ...>"]
    @Значение
[/GRecaptcha]
```

{% hint style="info" %}
В типовом дизайне GRecaptcha используется в шаблонах:

* Регистрация нового веб-пользователя - Физ. лица. + GRecaptcha
* Регистрация нового веб-пользователя - Юр. лица + GRecaptcha
* Личный кабинет. Анкета, запрос по VIN. Анонимный пользователь. + GRecaptcha
* Обратная связь. Детальный просмотр товара. Всплывающее окно.+GRecaptcha
* Обратная связь. Корзина - шаг 3. Всплывающее окно. +GRecaptcha
* Личный кабинет. Сообщения. Форма отправки сообщения. Анонимный пользователь.+GRecaptcha
{% endhint %}

Так как типовой дизайн использует собственные ключи GRecaptcha во время стилизации создаются копии шаблонов с указанием ключей для текущего домена. На соответствующих страницах указываются новые шаблоны в параметре Шаблон отображения для размещенного контрола.


