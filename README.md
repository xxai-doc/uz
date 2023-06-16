<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.art

Veb-sayt kodining bir qismi ochiq manba, tarjimani optimallashtirishga yordam berish uchun xush kelibsiz.

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
