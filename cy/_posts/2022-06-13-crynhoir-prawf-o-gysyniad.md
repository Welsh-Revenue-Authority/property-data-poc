---
title: Crynhoi'r Prawf o Gysyniad
lang: cy
ref: proof-of-concept
layout: post
author: Anthony Pritchard, Richard Pope
---
Dyma grynodeb o’r gwaith a gyflwynwyd gennym yn yr arddangosfa yn ystod wythnos 12 ar gyfer y prawf o gysyniad y llwyfan data tir ac eiddo.

![Sleid gyda’r testun: Mae angen i Awdurdod Cyllid Cymru gefnogi trethi tir ac eiddo sy’n amrywio’n ddaearyddol. Rydym yn ystyried a allai defnyddio platfform data ar gyfer tir ac eiddo yng Nghymru osod sylfaen ar gyfer rhywbeth mwy.](/property-data-poc/assets/images/poc-mission-cy.png)

Mae’n gyfnod cyffrous i drethi sydd wedi’u datganoli yng Nghymru. Mae’n debygol y bydd angen i Awdurdod Cyllid Cymru gefnogi trethi tir ac eiddo sy’n amrywio’n ddaearyddol. Mae gwaith i’w wneud hefyd ar [Ddiwygio’r Dreth Gyngor](https://llyw.cymru/cynlluniau-i-ddiwygior-dreth-gyngor) a dechrau cynnal trafodaethau am Ardoll Twristiaeth.

Roeddem am ddysgu sut y gall ACC gefnogi trethi daearyddol amrywiol a thrwy fabwysiadu dull platfform a ‘dysgu drwy greu’, roeddem eisiau dechrau deall a allai hyn osod y sylfaen ledled Cymru.

I’ch atgoffa, wrth sôn am ‘blatfformau’, rydym yn cyfeirio at bethau sy’n hwyluso’r broses o ddarparu gwasanaethau cyhoeddus a chyflawni bwriad y polisi.

![Sleid yn cynnwys delwedd o blatfform llorweddol sy’n cefnogi sawl gwasanaeth a’r testun: Cofiwch: mae platfformau’n hwyluso’r broses o ddarparu gwell gwasanaethau a rhoi bwriad y polisi ar waith](/property-data-poc/assets/images/platform-model-cy.png)

Gwnaethom weithredu drwy edrych ar sleisen fechan o swyddogaethau a data i’n helpu i archwilio’r cyfleoedd a’r heriau sy’n gysylltiedig â defnyddio platfform data tir ac eiddo er mwyn deall sut y gallai hynny weithio yng Nghymru.

![Sleid gyda delwedd debyg i’r sleid flaenorol, gydag un gwasanaeth a phlatfformau ‘rheolau’ a ‘data’ wedi’u dewis, gyda’r testun canlynol: Noder: gwnaethom edrych ar sleisen fechan](/property-data-poc/assets/images/platform-slice-cy.png)

![Sleid yn cynnwys delwedd sy’n dangos gwasanaethau, rheolau a data enghreifftiol, fel ffiniau eiddo. Mae’n cynnwys y testun: i ddeall sut y gall hynny weithio yng Nghymru.](/property-data-poc/assets/images/platform-vision-cy.png)

Yn olaf, nodyn i’ch atgoffa bod ein gwaith yn ddamcaniaethol a bod yr holl ddata a ddefnyddiwyd gennym yn synthetig. Roedd enwau lleoedd a lleoliadau [wedi’u hysbrydoli gan gofnod ar Wikipedia](https://en.wikipedia.org/wiki/Category:Fictional_populated_places_in_Wales) a chawsant eu lleoli ar dir milwrol/cyn-filwrol. Roeddem hefyd wedi creu dau ‘barth treth’ (yn y Gogledd Ddwyrain a’r De Orllewin) i ddangos y syniad o gyflwyno trethi amrywiol yn lleol. Eto, parthau dychmygol oedd y rhan - nid oeddem am agor unrhyw drafodaethau mawr yn ystod y prawf o gysyniad!

![Cofiwch: gwnaethom ddefnyddio data synthetig i greu prototeipiau](/property-data-poc/assets/images/synthetic-data-cy.png)

Gwnaethom osod 4 nod gyda’r bwriad i’w cyflawni o fewn 12 wythnos. Byddwn yn rhoi enghreifftiau o’r gwaith rydym wedi’i wneud a’r hyn rydym wedi’i ddysgu.

![Sleid gyda’r testun: 1) Rhoi bywyd i’r cyfleoedd a’r heriau 2) Rhoi opsiynau polisi posibl i Weinidogion 3) Dangos ffyrdd newydd o weithio 4) Bod yn glir am yr uchelgais a’r man dechrau](/property-data-poc/assets/images/poc-objectives-cy.png)

## 1. Rhoi bywyd i’r cyfleoedd a’r heriau

Gwnaethom ddefnyddio data synthetig i greu [prototeip platfform](https://land-property-platform.herokuapp.com/). Gwnaethom adeiladu ei god gweithio ac mae’n fodel o’r peth go iawn. Mae hyn wedi ein helpu i ddychmygu sut y [gall platfform data ar gyfer tir ac eiddo](https://welsh-revenue-authority.github.io/property-data-poc/cy/2022/03/02/beth-yw-llwyfan-data.html) weithio.

![Gif sy’n clicio drwy nodweddion gwefan y platfform. Caiff y nodweddion eu hegluro yn y testun o dan y ddelwedd hon.](/property-data-poc/assets/images/platform-prototype.gif)

Rydym yn gwybod bod platfformau da yn gwneud ychydig o bethau syml yn dda. Drwy wneud gwaith ymchwil, gwnaethom ddysgu ei bod hi’n hollbwysig ein bod yn gwneud y pethau syml hyn yn glir i ddefnyddwyr posibl.

Er enghraifft, gwnaethom restru’i [nodweddion](https://land-property-platform.herokuapp.com/features) gan geisio egluro sut maent yn helpu defnyddwyr i ddatrys eu problemau:
- Cadarnhau a yw’r eiddo yng Nghymru ai peidio. Mae hyn yn haws dweud na gwneud.
- Rhoi cyfraddau treth ar gyfer Treth Trafodiadau Tir dychmygol
- Chwilio am unrhyw eiddo yng Nghymru yn seiliedig ar Gyfeirnod Eiddo Unigryw (UPRN)

Rydym yn gwybod y bydd defnyddwyr posibl yn awyddus gael golwg cyn [dechrau arni](https://land-property-platform.herokuapp.com/getting-started) felly gwnaethom ychwanegu [dogfennaeth](https://welsh-revenue-authority.github.io/property_platform_app/) a rhoi ffordd o [archwilio rhyngwyneb rhaglennu cymwysiadau (APIs)](https://land-property-platform.herokuapp.com/docs).

Er mwyn profi’r platfform, gwnaethom adeiladu gwasanaeth syml iawn ar ei ben o’r enw [A yw’r eiddo yng Nghymru?](http://www.isitin.wales/) Do, rydych chi wedi dyfalu’n gywir: mae’n dweud wrthych chi a yw’r eiddo yng Nghymru, yn rhannol yng Nghymru neu os nad yw’r eiddo yng Nghymru.

![Gif yn dangos Cyfeirnodau Eiddo Unigryw (UPRN) yn cael eu mewnbynnu i’r wefan ‘A yw’r eiddo yng Nghymru?’ a gwahanol ymatebion yn ymddangos.](/property-data-poc/assets/images/isitin.wales.gif)

Mae’n swnio’n syml iawn, ond mewn gwirionedd, oherwydd amwysedd a chymhlethdod gwahanol setiau data sy’n bodoli ar hyn o bryd, ‘dyw hi ddim bob tro’n hawdd cael ateb i’r cwestiwn hwn. Mae’r platfform yn tynnu oddi ar ddilysrwydd yr atebion.

### Defnyddio platfform i ddangos gwybodaeth ar wahanol gamau o’r broses brynu

Mae platfformau’n galluogi’r defnydd o sawl gwasanaeth, felly roeddem am roi ystyriaeth i sut y mae modd dangos gwybodaeth ar wahanol gamau o’r broses o brynu eiddo.

Gwnaethom edrych ar sut y gallai peiriannau chwilio eiddo, fel Rightmove, gyflwyno trethi daearyddol amrywiol. Sut y byddai hynny’n gwneud i berson sydd am brynu cartref deimlo? A allem egluro trethi tir ac eiddo lleol i bobl mewn modd dealladwy?

![Ffug dudalen ar wefan Rightmove sy’n dangos dolenni i drethi posibl ar gyfer eiddo sydd ar werth. Caiff ei ddangos ar iphone ar fwrdd pren.](/property-data-poc/assets/images/rightmove-prototype.png)

Sut y byddai’n teimlo wrth i bobl newid o chwilio am dŷ i’w brynu? Dyma gyfrifiannell treth ffug sy’n dangos sut y gallai hynny weithio.

![Tudalen ganlyniadau ffug o gyfrifiannell dan frand Llywodraeth Cymru sy’n dangos ‘parth treth’ yr eiddo.](/property-data-poc/assets/images/digital-proof.gif)

Yn olaf, roeddem am archwilio’r syniad o greu prawf digidol o drafodiad. Mae’n bosibl mai ar blatfform tir ac eiddo yw’r lle cyntaf y caiff y broses o drosglwyddo perchnogaeth ei chofnodi. A allai hynny fod yn fan cychwyn ar gyfer gwasanaethau cydgysylltedig yn y dyfodol?

![Tystysgrif Treth Trafodiadau Tir ffug yn Gymraeg ac yn Saesneg. Mae’n cynnwys cod QR wedi’i arwyddo a chod untro y gellid ei ddefnyddio fel rhan o wasanaeth ‘rhoi gwybod i ni unwaith’ ar gyfer symud cartref.](/property-data-poc/assets/images/digital-proof.gif)

### Eiddo-fesul-tudalen

Dychmygwch allu teipio cod post yn [LLYW.CYMRU](https://llyw.cymru/?_ga=2.268615991.770389225.1653403013-1893143058.1653299578) a gallu gweld gwybodaeth am yr eiddo hwnnw a’r ardal leol - yn debyg i’r hyn y mae chwiliad Google yn ei wneud ar gyfer mapiau. Gallai fod yn rhan o dudalen lansio i wasanaethau cenedlaethol a gwasanaethau lleol ynghyd â rhagor o wybodaeth ddefnyddiol. 

Byddai platfform data eiddo yn hwyluso’r broses o gyflawni hyn ac yn ffordd rad o’i gynnal.

![Gif wedi’i animeiddio o god post yn cael ei fewnbynnu i flwch chwilio ar llyw.cymru. Dengys restr o gyfeiriadau, ac yna mae modd i’r defnyddiwr lywio drwyddynt i weld gwybodaeth am yr eiddo hwnnw, gan gynnwys ei gostau ynni a’r diwrnod casglu biniau.](/property-data-poc/assets/images/page-per-property.gif)

Mae’r holl enghreifftiau hyn yn brototeipiau damcaniaethol. Eu pwrpas yw dangos yr ystod o wasanaethau y gellid eu cefnogi gan blatfform a rhai o’r cyfleoedd y gellid eu cynnig.

## 2. Rhoi opsiynau polisi posibl i Weinidogion

Mae llywodraeth Cymru wedi cynnal llawer o drafodaethau am [sut olwg fydd ar drethi datganoledig yn y dyfodol](https://ymchwil.senedd.cymru/erthyglau-ymchwil/trethu-yn-y-chweched-senedd/). Un o’n hamcanion oedd archwilio’r opsiynau polisi posibl y gallai platfform tir ac eiddo eu gwneud yn bosibl a sut y gallai’r platfform hwnnw gefnogi’r [fframwaith trethi datganoledig](https://llyw.cymru/fframwaith-polisi-trethi-html?_ga=2.100976071.770389225.1653403013-1893143058.1653299578) sy’n sail iddo.

Mae platfform cyffredin ar gyfer tir ac eiddo yng Nghymru yn dod â mathau newydd o wasanaethau ac opsiynau polisi a oedd yn amhosibl o’r blaen (neu’n anodd) yn realiti.

### Patrymau newydd ar gyfer dyluniad gwasanaethau

Yn gyntaf, o edrych ar ddyluniad gwasanaeth, mae gwasanaeth digidol nodweddiadol y llywodraeth yn edrych fel y canlynol:

![Ffrâm wifren wedi’i sylmleiddio o ffurflen gyffredinol 7 cam y llywodraeth, gan gynnwys yr opsiwn i adolygu’r atebion a nodwyd a chyfeirnod ar y dudalen ddiwethaf.](/property-data-poc/assets/images/transactional-services.png)

Fel arfer, efallai y byddwch yn mewnbynnu ychydig o ddata ar ffurflen we, ei chyflwyno ac yna yn aros i rywbeth ddigwydd. Yn y cyfamser, efallai y cewch gadarnhad e-bost a byddwch yn gallu dilyn unrhyw gynnydd. Yn yr achos hwn, disgwylir i bobl gofnodi gwybodaeth y gallent fod eisoes wedi’i rhoi i’r llywodraeth. Hefyd, mae angen iddynt aros i rywbeth ddigwydd

Mae platfformau’n rhoi’r cyfle i gynnig mwy o wasanaethau amser real sy’n lleihau’r baich gweinyddol hwn ac yn arbed amser. Efallai, drwy wneud hyn, y bydd modd ailddefnyddio gwybodaeth sydd eisoes gennym (gan sicrhau goruchwyliaeth a chael caniatâd priodol): 

![Ffrâm wifren wedi’i symleiddio o ffurflen we 3 cam y llywodraeth lle caiff data sydd eisoes ym meddiant y llywodraeth ei chwarae yn ôl i ddefnyddiwr a rhoddir cod QR iddynt fel prawf digidol.](/property-data-poc/assets/images/real-time-services.png)

Cyfuno gwybodaeth o bob rhan o’r llywodraeth mewn un gwasanaeth:

![Ffrâm wifren wedi’i symleiddio o dudalen cychwyn gwasanaeth y llywodraeth o’r enw. Teitl y dudalen yw: Mewngofnodi er mwyn rheoli eich cyfrif cartref.](/property-data-poc/assets/images/household-account.png)

neu helpu pobl i ryngweithio â Llywodraeth Cymru ac awdurdodau lleol ar yr un pryd:

![Ffrâm wifren wedi’i symleiddio o dudalen we o wasanaeth llywodraeth o dan y teitl: Edrychwch ar y data sydd gennym amdanoch. Mae ganddo ddwy linell sy’n arwain at ‘llywodraeth leol’ a ‘llywodraeth Cymru’](/property-data-poc/assets/images/joined-up-services.png)

Un maes y gwnaethom ei drafod wrth gynnal y prawf o gysyniad, yw’r posibilrwydd o gefnogi Ardoll Twristiaeth lle mae busnesau llety yng Nghymru yn cofrestru i gasglu ardoll twristiaeth eu hunain. Gallai hyn gael ei gefnogi gan blatfform tir ac eiddo sy’n dwyn ynghyd gwybodaeth o wahanol rannau o’r llywodraeth, neu sy’n cefnogi sefydliadau’r sector preifat (e.e. Airbnb) gyda’r caniatâd priodol i ddefnyddio’r rhywfaint o’r data hwn hefyd.

![Ffrâm wifren wedi’i symleiddio o wasanaeth y llywodraeth o’r enw ‘Cyfrif llety twristiaeth cofrestredig’. Mae’n cynnwys rhestr wirio o wybodaeth y mae defnyddwyr eisoes wedi’i ddarparu, ac un eitem heb ei chwblhau. AR ochr dde’r sgrin, mae opsiynau i roi gwybod am newidiadau, i ddiweddaru dewisiadau cyswllt, i weld a thalu swm yr ardoll ymwelwyr, a chysylltu’r cyfrir i AirBnB.](/property-data-poc/assets/images/tourism-account.png)

Neu dychmygwch sut mae cael dynodydd cyffredin a rennir ar gyfer busnes twristiaeth yn amlygu effaith polisïau. Dyma sticer ffug cwbl ddychmygol a fyddai’n galluogi pobl i sganio cod QR i weld sut y caiff yr Ardoll Twristiaeth ei wario yn yr ardal leol.

![Sticer dwyieithog ffug dan frand y llywodraeth ar ffenest drws gwyrdd.](/property-data-poc/assets/images/door-sticker.png)

Nid yw’r enghreifftiau hyn yn ceisio rhoi’r ateb - daw’r ateb hwnnw o wneud gwaith ymchwil cynyddrannol. Y gobaith yw eu bod yn amlygu rhai o’r pethau a allai gael eu hwyluso drwy ddefnyddio un platfform cyffredin.

### Offer polisi newydd

Gallai’r platfform tir ac eiddo alluogi ffyrdd newydd o gynllunio a phrofi polisi. 
Gwnaethom arbrofi gydag offeryn o’r enw [Llyfr Nodiadau Jupyter](https://jupyter.org/) i edrych ar sut y gallem weithredu ‘polisi fel cod’.

![Gif wedi’i animeiddio o Lyfr Nodiadau Jupyer sy’n dangos cyfrifiannell treth leol a mapiau o Gymru.](/property-data-poc/assets/images/Jupyter-notebook.gif)

Mae’r syniad o godio polisi drwy gyfuno testun a chod yn ei wneud yn ddealladwy i bobl a chyfrifiaduron. Mae ganddo’r potensial i alluogi llunwyr polisi i brofi effaith eu cynllun polisi.

Yn ystod y broses o brawf o gysyniad, rydym yn ei ddefnyddio i brofi syniadau ‘Treth Trafodiadau Tir’ drwy [baratoi nifer o enghreifftiau](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/2022-01-31) a [modelu ffiniau daearyddol dychmygol](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/2022-02-07).

### Ysgogiadau polisi newydd

Pa fath o ysgogiadau polisi fyddai’n cael eu galluogi gan ddull digidol yn gyntaf? Rydym wedi disgrifio’r rhain fel ‘patrymau polisi’ - sef rhestr o fathau o opsiynau polisi y gallai platfform eu gwneud yn bosibl. Rydym wedi bod yn defnyddio’r rhain i’n helpu i ddatblygu rhywfaith o ieithwedd a rennir rhwng arbenigwyr polisi a digidol.

![Picogramiau a thestun sy’n dangos gwahanol batrymau polisi, a gaiff eu hegluro yn y testun isod.](/property-data-poc/assets/images/patterns.gif)

Er enghraifft, gallai platfform llwyfan data eiddo gynnwys alluogi’r canlynol:

- Mae **parthau treth** yn seiliedig ar unrhyw ardal y gallech ei osod ar fap: cod post, Awdurdod Lleol, parc Cenedlaethol, 10 milltir o’r môr
- **Cyd-destun y farchnad:** cysylltu cyfraddau treth â setiau data eraill fel amlygrwydd ail-gartrefi. Byddai hynny’n anodd iawn ei wneud ar system analog.
- Byddai **cyfradd tapr** yn rhoi rheolaeth i lunwyr polisi dros amrywiaeth treth a’u gwneud yn decach
- Gallai **priodoleddau ffisegol** tir ac eiddo, fel paneli solar, gael eu hychwanegu at y platfform a’u defnyddio fel sail ar gyfer trethiant. Dros amser, bydd y data ychwanegol a gaiff ei ychwanegu at y platfform yn agor mwy o opsiynau polisi

## 3. Dangos ffyrdd newydd o weithio

Rydym yn gosod y nod i’n hunain o ddangos ffyrdd newydd o weithio. Drwy gydol y 12 wythnos o’r prawf o gysyniad, gweithiodd y tîm mewn sbrintiau wythnosol (‘ystwyth’) gan ymrwymo i weithio’n agored i rannu cynnydd wrth i ni fynd ymlaen.

### Gweithio’n agored

![Gif wedi’i animeiddio o dudalen we sy’n sgrolio yn dangos nodiadau wythnosol ein tîm a gwefan y prosiect.](/property-data-poc/assets/images/team-website.gif)

Un o’r pethau cyntaf y gwnaethom oedd creu [gwefan i’r tîm](https://welsh-revenue-authority.github.io/property-data-poc/cy/2022/03/02/beth-yw-llwyfan-data.html) a oedd yn cael ei ddefnyddio gennym i rannu cynnydd drwy [ddefnyddio nodiadau wythnosol](https://welsh-revenue-authority.github.io/weeknotes/property-data-poc/2022-02-07) a [blogiau](https://welsh-revenue-authority.github.io/property-data-poc/cy/2022/04/05/beth-rydym-wedi-ei-ddysgu-o-weithio-n-agored.html). Roedd hyn yn effeithiol i ni egluro’r hyn rydym yn ei wneud i bobl y tu allan i’n tîm a'n sefydliad. Rydym yn credu eu bod wedi gwella’r ffordd rydym yn cyfathrebu ac yn cydweithio ac rydyn ni’n sylwi ar lwythi o [fanteision gweithio’n agored](https://welsh-revenue-authority.github.io/property-data-poc/cy/2022/04/05/beth-rydym-wedi-ei-ddysgu-o-weithio-n-agored.html).

Rydym wedi defnyddio Github i ddechrau adeiladu llyfrgell ymchwil defnyddwyr preifat - sylfaen wybodaeth o’r hyn rydym wedi’i ddysgu drwy siarad â defnyddwyr a’u goruchwylio.

![Tudalen o GitHub gyda’r teitl: Ymchwil i ddefnyddwyr platfform Tir ac Eiddo](/property-data-poc/assets/images/research-library.png)

### Sesiynau Dangos a Dweud

Rydym wedi defnyddio sesiynau Dangos a Dweud gyda phobl o ACC a phobl y tu allan i ACC sydd â diddordeb yn y prosiect cyfredol. Maent yn rhan bwysig o’n llywodraethant. 

![Sleid yn dangos diagram cylchol o’n rhythm wythnosol. Cynhelir gwaith cynllunio ar ddydd Mawrth, cyfarfodydd byr ar droed ar ddydd Mercher, dydd Iau a dydd Gwener a sesiynau dangos a dweud ar ddydd Llun. ](/property-data-poc/assets/images/show-tell-cy.png)

Am 30 munud bob dydd Llun, mae'r tîm yn dangos eu cynnydd (gwaith a wnaed, pethau a ddysgwyd) i bobl sy’n mynychu. Mae’n rhoi’r cyfle i randdeiliaid, cydweithredwyr ac arbenigwyr yn y maes… i ofyn cwestiynau a herio’r tîm.

Mae’r fforwm yn annog gwaith craffu annibynnol a'r gobaith yw ei fod yn meithrin hyder ac ymddiriedaeth yn y tîm. Mae’n galluogi noddwyr i asesu cyfraniad y tîm.

Mae sesiynau Dangos a Dweud yn helpu i sicrhau bod y tîm yn darparu’r peth cywir yn y ffordd gywir drwy ychwanegu ymgysylltiad at lywodraethant.

### Dull cyflawni fesul cam

Bob wythnos, mae angen i’r tîm gadw cydbwysedd rhwng dysgu, diwallu anghenion defnyddwyr, rhoi dull gweithredu polisi ar waith ac ehangu’r gallu sefydliadol. Drwy weithredu fesul cam, mae’r tîm yn anelu at gyflawni rhywbeth o [werth posibl](https://richardpope.org/blog/2022/03/16/UPC-measure-value-digital-service-work/) bob wythnos.

![Graff 3 echel gyda’r labeli ‘anghenion defnyddwyr’, ‘gallu i weithredu’ a ‘bwriad y polisi’. Mae dolen yn dangos bod pob un ohonynt yn cynyddu dros amser. Y teitl ar yr ochr dde yw “cydbwyso anghenion, bwriad y polisi a meithrin gallu”.](/property-data-poc/assets/images/ucp-cy.png)

## 4. Yr uchelgais a’r man dechrau

Nod terfynol y prawf o gysyniad oedd bod yn gliriach ynghylch yr uchelgais a’r man dechrau. Yn seiliedig ar yr hyn rydym wedi’i ddysgu, dyma ein dull arfaethedig, lefel uchel o ymdrin â’r broses o feithrin gallu:

![Tudalen fapio yn cynnwys adrannau dros dro (dysgu defnyddio platfform syml), 3-6 mis (ychwanegu ein gwasanaeth cyntaf) a 9-12 mis (ehangu nifer y defnyddwyr allanol).](/property-data-poc/assets/images/roadmap-cy.png)


![Tudalen fapio sy’n dangos un ‘tîm platfform a gwasanaethau’ a gaiff ei rannu’n dîm platfform a thîm gwasanaeth. Yna, ar ôl 9 mis, rhaniad pellach o bosibl.](/property-data-poc/assets/images/team-cy.png)

Amserlen ddamcaniaethol yw hon ond mae’n dangos mai dim ond megis dechrau yw hyn.

### Camau bach i ddechrau, gan anelu’n uchel

Nid yw uchelgais y platfform tir ac eiddo yn ymwneud ag un polisi neu fenter yn unig. Mae hyn ar gyfer y tymor hir. Ac mae hyn i Gymru. Gallai platfform llwyfan data tir ac eiddo olygu gwell canlyniadau polisi a dull gwahanol o gynllunio gwasanaethau cyhoeddus.

![Sleid yn cynnwys delwedd sy’n dangos gwasanaethau, esiampl o reolau a data, megis ffiniau eiddo. Mae’n cynnwys y testun canlynol: Gwasanaethau cydgysylltiedig, amser real. Canolog, lleol, cyhoeddus a phreifat. Gosod rheolau drwy god sy’n meithrin dulliau digidol o ymdrin â pholisi. Cofnodi data ar y cyd, a weithredir fel seilwaith ar gyfer y tymor hir ledled Cymru gyfan.](/property-data-poc/assets/images/ambition-cy.png)

Os oes gennych gwestiynau neu os hoffech glywed mwy am y gwaith hwn, mae croeso i chi [gysylltu â ni](mailto:dataproject@wra.gov.wales)