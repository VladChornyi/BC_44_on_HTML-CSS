<!-- Заняття 15:

Медіа-запити: media-type(all,  screen, print, speech) та media-feature(https://developer.mozilla.org/en-US/docs/Web/CSS/@media#media_features)

https://www.nytimes.com/2022/11/18/us/georgia-camden-jail-detainee-beating.html?action=click&algo=bandit-all-surfaces-time-cutoff-30_impression_cut_3_filter_new_arm_5_1&alpha=0.05&block=more_in_recirc&fellback=false&imp_id=436460703&impression_id=bf4d8c22-69de-11ed-a33d-9f0100db763d&index=2&pgtype=Article&pool=more_in_pools%2Fus&region=footer&req_id=297133067&surface=eos-more-in&variant=0_bandit-all-surfaces-time-cutoff-30_impression_cut_3_filter_new_arm_5_1


Медіа-функції min-width та max-width
Логічні оператори: and, not, or
Метатег viewport. Атрибути width=device-width та initial-scale
Chrome DevTools для роботи з мобільною версткою
Адаптивна і респонсивна верстка
Підхід mobile-first CSS
Посилання на макет -->

<!-- Послідовність виконання ДЗ
1. Налаштовуємо контейнер, оскільки від його розмірів залежать розміри дочірніх елементів
2. Коментуємо всі секції в html
3. Беремо для початку саму просту секції в роботу, розкоментуємо її і починаємо адаптувати, починаючи з мобільної версії сайту.
4. Адаптуємо стилі по черзі для усіх секцій.
5. Підключаємо мобільне меню
6. Додаємо зображення -->

<!--
Занятие 16:
- Піксельна щільність екрана (retina)

- Ретинізація растрової графіки

- Респонсивний тег img, атрибути srcset и sizes

- Різні формати зображень з тегом picture

- Ретинізація фонових зображень: медіа-функція min-resolution"

 -->

<!-- ======= Приклад застосування дескриптора х ======= -->

<!-- <img
  srcset="photo.jpg 1x, photo@2x.jpg 2x"
  src="photo.jpg"
  alt="Опис зображення"
/> -->

<!-- ======= Приклад застосування дескриптора w ======= -->

<!-- <img
  srcset="
	photo-450.jpg 450w, photo-900.jpg 900w,
	photo-354.jpg 354w, photo-708.jpg 708w,
	photo-270.jpg 270w, photo-540.jpg 540w"
  sizes="(min-width: 1200px) 270px, (min-width: 768px) 540px, (min-width: 480px) 450px, 100vw"
  src="photo-450.jpg"
  alt="Опис зображення"
/> -->

<!-- ======= Приклад застосування webp i picture ======= -->

<!-- <picture>
    <source
        srcset="
        ./images/team1-1200@1x.webp 1x,
        ./images/team1-1200@2x.webp 2x
        "
        media="(min-width: 1200px)"
        type="image/webp"
    />

    <source
        srcset="
        ./images/team1-1200@1x.jpg 1x,
        ./images/team1-1200@2x.jpg 2x
        "
        media="(min-width: 1200px)"
        type="image/jpeg"
    />
    ...............................
    <img
        class="image"
        src="./images/team-1-450@1x.jpg"
        alt="Опис зображення"
    />
</picture> -->

<!-- ======= Приклад ретинізації фонових зображень ======= -->

 <!-- background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
    url('../images/hero-480@1x.jpg');
  @include retina-bgi {
    background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
      url('../images/hero-480@2x.jpg');
  }

  @include tablet {
    background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
      url('../images/hero-768@1x.jpg');
    @include retina-bgi {
      background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
        url('../images/hero-768@1x.jpg');
    }
  }

  @include desktop {
    background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
      url('../images/hero-1200@1x.jpg');
    @include retina-bgi {
      background-image: linear-gradient(rgba(25, 28, 38, 0.2), rgba(25, 28, 38, 0.2)),
        url('../images/hero-1200@2x.jpg');
    }
  } -->
