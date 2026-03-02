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

<button class="bg-audio-toggle" id="rain-toggle" type="button">
  <span class="bg-audio-icon" aria-hidden="true">
    <svg viewBox="0 0 24 24" width="18" height="18" focusable="false" aria-hidden="true">
      <path d="M12 2a7 7 0 0 0-7 7v1H4a1 1 0 0 0 0 2h1v7a1 1 0 1 0 2 0v-7h10v7a3 3 0 0 1-6 0 1 1 0 1 0-2 0 5 5 0 0 0 10 0v-7h1a1 1 0 1 0 0-2h-1V9a7 7 0 0 0-7-7Zm5 8H7V9a5 5 0 0 1 10 0v1Z"/>
    </svg>
  </span>
  <span class="bg-audio-label">Дождь: включить</span>
</button>
<audio id="rain-audio" preload="auto" loop>
  <source src="{{ '/assets/triumph/rain.mp3' | relative_url }}" type="audio/mpeg">
</audio>
<style>
  .bg-audio-toggle {
    --rain-accent: #2f81f7;
    position: sticky;
    top: 12px;
    z-index: 5;
    margin: 6px 0 14px;
    padding: 10px 14px;
    border-radius: 999px;
    border: 1px solid rgba(17, 24, 39, 0.18);
    background: rgba(235, 238, 243, 0.92);
    color: #2f343b;
    backdrop-filter: blur(10px);
    font-weight: 600;
    cursor: pointer;
    display: inline-flex;
    align-items: center;
    gap: 10px;
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.18);
  }

  .bg-audio-toggle:hover {
    background: rgba(223, 228, 235, 0.95);
  }

  .bg-audio-icon {
    display: inline-flex;
    width: 18px;
    height: 18px;
  }

  .bg-audio-icon svg {
    fill: var(--rain-accent);
  }

  .bg-audio-toggle:focus-visible {
    outline: 2px solid rgba(47, 129, 247, 0.55);
    outline-offset: 2px;
  }
</style>
<script>
  (function () {
    const audio = document.getElementById("rain-audio");
    const btn = document.getElementById("rain-toggle");
    const label = btn.querySelector(".bg-audio-label");
    const storageKey = "bg_rain_enabled";

    audio.volume = 0.35;

    function setLabel() {
      label.textContent = audio.paused ? "Дождь: включить" : "Дождь: выключить";
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
