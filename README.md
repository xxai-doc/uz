<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Katalogga kirgandan so'ng avval nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , so'ngra `direnv allow` o'rnatish tavsiya etiladi (katalogga kirgandan so'ng [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) avtomatik ravishda bajariladi).

Ma'nosi: yapon, koreys, ingliz tillariga xitoycha tarjima, boshqa barcha tillarga inglizcha tarjima. Agar siz faqat xitoy va ingliz tilini qo'llab-quvvatlamoqchi bo'lsangiz, shunchaki `zh: en` yozishingiz mumkin.

## oldingi kod

* [oldingi kod](https://github.com/xxai-art/web)
* [Butun sayt uchun til paketlari](https://github.com/xxai-art/web/tree/main/i18n)
* [Kirish modullari uchun til paketlari](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Ko'p tilli veb-sayt hujjatlari](https://github.com/xxai-doc)

Front-end dasturlash tili [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) bo'lib, u coffeescript sintaksisiga asoslangan ba'zi xususiyatlarni qo'shadi, qarang [./coffee_plus.md](./coffee_plus.md) .

## Veb-saytlar va hujjatlarni xalqarolashtirish

Quyidagi 3 ta loyiha asosida quring

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Qo'shimchasi `.mdt` , siz tashqi fayllarga murojaat qilish uchun `<+ ./coffee_plus/import.js>` ga o'xshash sintaksisdan foydalanishingiz va `.md` qo'shimchasi bilan markdown yaratishingiz mumkin.

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Markdown tarjimasi kodlar va havolalarni tarjima qilmaydi va tarjima qilingan jumlalarni keshda saqlaydi. Agar tarjima o'zgartirilgan bo'lsa-da, lekin asl matn o'zgartirilmagan bo'lsa, uni qayta bajarish tarjimaning o'zgarishini qayta yozmaydi.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` tomonidan yaratilgan veb-saytlarni tarjima qilish uchun til fayllari.

### Hujjatlarni tarjima qilishni avtomatlashtirish bo'yicha ko'rsatmalar

[Xxai-art/doc](https://github.com/xxai-art/doc) kod omboriga qarang

Katalogga kirgandan so'ng avval nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) , so'ngra `direnv allow` o'rnatish tavsiya etiladi (katalogga kirgandan so'ng [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) avtomatik ravishda bajariladi).

Yuzlab tillarga tarjima qilingan katta kod bazasini oldini olish uchun men har bir til uchun alohida kod bazasini yaratdim va kod bazasini saqlash uchun tashkilot yaratdim.

`GITHUB_ACCESS_TOKEN` muhit oʻzgaruvchisini oʻrnatish va undan soʻng [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) ishga tushirish avtomatik ravishda kodlar omborini yaratadi.

Albatta, siz uni kod bazasiga ham qo'yishingiz mumkin.

Tarjima skripti havolasi [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Skript kodi quyidagicha talqin qilinadi:

[bunx](https://bun.sh/docs/cli/bunx) npx o'rnini bosadi, bu tezroq. Albatta, agar sizda bun o'rnatilmagan bo'lsa, uning o'rniga `npx` dan foydalanishingiz mumkin.

`bunx mdt zh` `.mdt` zh katalogida `.md` sifatida ko'rsatadi, quyidagi bog'langan 2 ta faylga qarang

* [coffee_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [coffee_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` tarjima uchun asosiy koddir (agar sizda faqat `nodejs` o'rnatilgan bo'lsa, lekin `bun` va `direnv` o'rnatilmagan bo'lsa, tarjima qilish uchun `npx i18n` ham ishga tushirishingiz mumkin).

U [i18n.yml ni](https://github.com/xxai-art/doc/blob/main/i18n.yml) tahlil qiladi, ushbu hujjatdagi `i18n.yml` konfiguratsiyasi quyidagicha:

```
en:
zh: ja ko en
```

Ma'nosi: yapon, koreys, ingliz tillariga xitoycha tarjima, boshqa barcha tillarga inglizcha tarjima. Agar siz faqat xitoy va ingliz tilini qo'llab-quvvatlamoqchi bo'lsangiz, shunchaki `zh: en` yozishingiz mumkin.

Oxirgisi [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) bo'lib, u `README.md` yozuvini yaratish uchun har bir tilning `README.md` faylining asosiy sarlavhasi va birinchi subtitrlari orasidagi tarkibni chiqaradi. Kod juda oddiy, uni o'zingiz ko'rishingiz mumkin.

Google API bepul tarjima uchun ishlatiladi. Agar siz Google-ga kira olmasangiz, proksi-serverni sozlang va sozlang, masalan:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Tarjima skripti `.i18n` katalogida tarjima qilingan kesh hosil qiladi, uni `git status` bilan tekshiring va takroriy tarjimalarning oldini olish uchun uni kodlar omboriga qo'shing.

Keshni yangilash uchun tarjimani har safar oʻzgartirganingizda `bunx i18n` dasturini ishga tushiring.

Agar asl matn va tarjima bir vaqtning o'zida o'zgartirilsa, kesh chalkashib ketadi, shuning uchun agar siz o'zgartirmoqchi bo'lsangiz, faqat bittasini o'zgartirishingiz mumkin, so'ngra keshni yangilash uchun `bunx i18n` dasturini ishga tushiring.
