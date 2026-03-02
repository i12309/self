---
title: "Торжество справедливости"
layout: story
theme: black
order: 20
excerpt: >-
  Иногда всё, что нужно — выговориться и поплакать. А потом уйти, оставив
  тебя холодной скалой.
cover: "/assets/img/triumph/poster.png"
---

<button class="bg-audio-toggle" id="rain-toggle" type="button">Дождь: включить</button>
<audio id="rain-audio" preload="auto" loop>
  <source src="{{ '/assets/triumph/rain.mp3' | relative_url }}" type="audio/mpeg">
</audio>
<style>
  .bg-audio-toggle {
    position: sticky;
    top: 12px;
    z-index: 5;
    margin: 6px 0 14px;
    padding: 10px 14px;
    border-radius: 999px;
    border: 1px solid var(--border);
    background: rgba(0, 0, 0, 0.18);
    color: var(--text);
    backdrop-filter: blur(6px);
    font-weight: 600;
    cursor: pointer;
  }

  html.theme-light .bg-audio-toggle,
  body.theme-light .bg-audio-toggle {
    background: rgba(255, 255, 255, 0.55);
  }
</style>
<script>
  (function () {
    const audio = document.getElementById("rain-audio");
    const btn = document.getElementById("rain-toggle");
    const storageKey = "bg_rain_enabled";

    audio.volume = 0.35;

    function setLabel() {
      btn.textContent = audio.paused ? "Дождь: включить" : "Дождь: выключить";
    }

    async function start() {
      try {
        await audio.play();
        localStorage.setItem(storageKey, "1");
      } catch (e) {
        // Autoplay can be blocked; user can start via the button.
      } finally {
        setLabel();
      }
    }

    function stop() {
      audio.pause();
      localStorage.setItem(storageKey, "0");
      setLabel();
    }

    btn.addEventListener("click", () => {
      if (audio.paused) start();
      else stop();
    });

    const remembered = localStorage.getItem(storageKey);
    if (remembered === "1") start();
    else {
      setLabel();
      // Try to autoplay once; if blocked, button remains.
      if (remembered === null) start();
    }
  })();
</script>

> Женщина.. Иногда, всё что ей нужно - поплакать и выговориться. И она снова как новенькая.

![описание]({{ "/assets/img/triumph/1.png" | relative_url }})

Я стою под дождём, обнимая её нежное тело. 
```
Она пахнет как ангел. 
```
Мы оба мокнем.

Я не вижу слез, но чувствую её сопение у себя на груди. Глажу шёлковые волосы.

Она поднимает голову, упирается взглядом в мои глаза, и начинает что то шептать.

Приближается губами к моему уху. 

Горячий, ласковый шёпот уносит меня в страну **сладких обещаний**.

Какой у неё приятный голос. 
```
Она точно ангел.
```
![описание]({{ "/assets/img/triumph/2.png" | relative_url }})

Мы расстаемся.

Я её уже не слышу, не воспринимаю её слова. 

Я холодная скала, о которую разбиваются теплые волны её женского естества.

Эмоции волнами поднимаются вверх, а потом бьются, пенятся и уходят обратно.
```
Так надо. 
```
Так правильно. Она не верит.

Дождь стеной смывает мои чувства, в очередной раз заставляя меня понять суть неизбежности.

Через несколько лет, ты всё поймешь, станешь счастливой женой и мамой и будешь с благодарностью меня вспоминать.

А я останусь всё тем же одиноким мужчиной, в поисках чего-то неуловимого.

Я легонько отстраняю её от себя. Последний раз целую её сладкий рот. Разворачиваюсь и ухожу.


![описание]({{ "/assets/img/triumph/3.png" | relative_url }})

```
Мы расстаемся. Так правильно.
```

> Торжество справедливости - мужчина **одинок**, женщина **свободна**!

[![описание]({{ "/assets/img/sign2.png" | relative_url }})]({{ "/" | relative_url }})
