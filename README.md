<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Ezali recommandé ko installer nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) liboso, mpe sima `direnv allow` sima ya kokota na répertoire ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) eko exécuter automatiquement sima ya kokota na répertoire).

Ndimbola ezali: Bobongoli ya Chinois na Japonais, Coréen, Lingelesi, Lingelesi libongoli na minoko mosusu nyonso. Soki olingi kaka ko soutenir Chinois na Anglais, okoki kaka kokoma `zh: en` .

Ndimbola ezali: Bobongoli ya Chinois na Japonais, Coréen, Lingelesi, Lingelesi libongoli na minoko mosusu nyonso. Soki olingi kaka ko soutenir Chinois na Anglais, okoki kaka kokoma `zh: en` .

* [code ya liboso](https://github.com/xxai-art/web)
* [Ba paquets ya langue pona site na mobimba na yango](https://github.com/xxai-art/web/tree/main/i18n)
* [Ba paquets ya langue pona ba modules ya login](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Site Internet Mikanda ya minoko mingi](https://github.com/xxai-doc)

Langue ya programmation ya liboso ezali [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , oyo ebakisi mwa makambo oyo esalemi na syntaxe ya coffeescript, tala [./coffee_plus.md](./coffee_plus.md) .

## Internationalisation ya ba sites internet na mikanda

Tongela na ba projets 3 oyo elandi

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Suffixe ezali `.mdt` , okoki kosalela syntaxe oyo ekokani na `<+ ./coffee_plus/import.js>` mpo na kolobela ba fichiers ya libanda, mpe kobimisa markdown na suffixe `.md` .

* [@w5/trmd na biso](https://www.npmjs.com/package/@w5/trmd)

  Bobongoli ya Markdown ekobongola ba code mpe ba liens te, mpe eko cacher ba phrases oyo ebongolami. Soki libongoli ebongwani kasi makomi ya ebandeli ebongisami te, kosala yango lisusu ekokoma lisusu te mbongwana ya libongoli.

* [@w5/i18n ezali](https://www.npmjs.com/package/@w5/i18n)

  Ba fichiers ya langue pona ko traduire ba sites internet oyo esalemi na `yaml` .

### Malako ya Automatisation ya Bobongoli ya Mikanda

Tala ebombelo ya code [xxai-art/doc](https://github.com/xxai-art/doc)

Ezali recommandé ko installer nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) liboso, mpe sima `direnv allow` sima ya kokota na répertoire ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) eko exécuter automatiquement sima ya kokota na répertoire).

Mpo na koboya base ya code ya monene oyo ebongolami na bankama ya minoko, nasalaki base ya code ekeseni mpo na monoko moko na moko mpe nasalaki ebongiseli mpo na kobomba base ya code

Kobongisa variable ya environnement `GITHUB_ACCESS_TOKEN` mpe sima kosala [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) ekosala automatiquement ebombelo ya code.

Ya solo, okoki mpe kotya yango na base ya code.

Référence ya script ya bobongoli [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

Code ya script e interprété boye:

[bunx](https://bun.sh/docs/cli/bunx) ezali remplacement ya npx, oyo ezali mbangu koleka. Ya solo, soki ozali na bun installé te, okoki kosalela `npx` na esika na yango.

`bunx mdt zh` ezongisaka `.mdt` na répertoire zh lokola `.md` , tala ba fichiers 2 oyo ezali na lien na se

* [kafe_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [kafe_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ezali code ya moboko mpo na kobongola (soki ozali kaka na `nodejs` installés, kasi `bun` mpe `direnv` ezali installé te, okoki mpe kosala `npx i18n` mpo na kobongola).

Eko parser [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , configuration ya `i18n.yml` na mokanda oyo ezali boye:

```
en:
zh: ja ko en
```

Ndimbola ezali: Bobongoli ya Chinois na Japonais, Coréen, Lingelesi, Lingelesi libongoli na minoko mosusu nyonso. Soki olingi kaka ko soutenir Chinois na Anglais, okoki kaka kokoma `zh: en` .

Ya nsuka ezali [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , oyo ebimisaka makambo kati na motó ya likambo monene mpe sous-titre ya liboso ya `README.md` ya monɔkɔ mokomoko mpo na kobimisa bokoti `README.md` . Code eza très simple, okoki kotala yango yo moko.

Google API esalelamaka mpo na kobongola ofele. Soki okoki te kokɔta na Google, tosɛngi yo obongisa mpe tyá proxy, na ndakisa:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Script ya bobongoli ekosala cache oyo ebongolami na répertoire `.i18n` , svp tala yango na `git status` mpe bakisa yango na ebombelo ya code mpo na koboya mabongoli oyo ezongelami.

Svp bosala `bunx i18n` mbala nionso bo modifier traduction pona ko mettre à jour cache.

Soki texte original na traduction e modifier en même temps, cache ekozala confuse, donc soki olingi o modifier, okoki ko modifier kaka moko, et puis kosala `bunx i18n` pona ko mettre à jour cache.
