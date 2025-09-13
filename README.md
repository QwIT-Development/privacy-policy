# Adatvédelmi Tájékoztató

🇭🇺 Ez a dokumentáció magyarul van.  
🇬🇧 English version: [README_en.md](https://github.com/QwIT-Development/privacy-policy/blob/master/README_en.md)

## 0. Rövid összefoglalás
- A Firka nem tárol semmilyen adatot szerveren - minden adat csak a te készülékeden marad.
- Az adatok a KRÉTA rendszeréből származnak, ők az eredeti adatkezelők.
- A Firka az adatokat csak megjeleníti, és nem fér hozzá olyan kritikus adatokhoz, mint például a jelszavad.
- Hibabejelentéskor te döntöd el, hogy megosztasz-e velünk képernyőképet vagy naplót - ezek a problémamegoldás után törlődnek.
- Ha a KRÉTA-ban tárolt adatodat szeretnéd módosítani vagy törölni, azt az iskoládon vagy a KRÉTA ügyfélszolgálatán keresztül tudod intézni.

## 1. Bevezetés
A Firka Napló (a továbbiakban: „alkalmazás” vagy „Firka”) célja, hogy a KRÉTA rendszeréből lekért tanulói adatokat letisztult, áttekinthető formában jelenítse meg a felhasználó készülékén.

## 2. Adatkezelő azonosítása
**Adatkezelő:** Firka Management Csapat (nem jogi személy)

**Kapcsolattartó e-mail:** legal@firka.app

Megjegyzés: a csapat nem kívánja egyes tagok személyes adatait nyilvánossá tenni; a fenti e-mail címen keresztül intézhető minden, az adatvédelemmel kapcsolatos ügy.

DPO (Adatvédelmi tisztviselő): **nem került kijelölésre**. Adatvédelmi ügyekben a kapcsolattartó e-mail címen lehet érdeklődni.

## 3. Milyen adatokat kezelünk és honnan?
Az alkalmazás az alábbi, a KRÉTA rendszeréből érkező adatokat jeleníti meg és tárolja lokálisan a felhasználó készülékén:
- tanulói profiladatok (név, oktatási azonosító, iskolai adatok),
- órarend,
- jegyek,
- iskolai üzenetek, értesítések.

Ezek az adatok nem a Firka szerverein, hanem kizárólag a felhasználó készülékén, helyileg kerülnek tárolásra.

Ahhoz, hogy híreket tudjunk közölni az alkalmazáson belül, a Firkának hozzá kell férnie egy, a saját szerverinken futó API-hoz (Application Programming Interface - magyarul "alkalmazásprogramozási felület"), melynek működése során a rendszer automatikusan naplózhatja a következő technikai adatokat:
- a kliens eszköz által megadott "User-Agent", mely a Firka használata során tartalmazza az aktuális alkalmazásverziót,
- a kérést indító eszköz IP-címe,
- valamint az API kérés során egyéb, technikailag szükséges HTTP-fejlécek (pl. tartalomtípus, nyelvi beállítások).
Ezeket az adatokat nem kapcsoljuk össze felhasználói fiókokkal vagy személyazonosító adatokkal, ezek kizárólag az API megfelelő működésének biztosítása, hibakeresés és visszélések megelőzése érdekében kerülhetnek ideiglenesen naplózásra.

**Fontos:** az API-nak nem küld az alkalmazás a szükségesnél több adatot, és a küldött adatokat semmilyen esetben sem adjuk tovább harmadik félnek.

## 4. Adataid tárolásának helye és biztonsága
- Az alkalmazás a KRÉTA szervereivel titkosított csatornán (HTTPS) kommunikál.
- A lekért adatok csak a felhasználó telefonján/eszközén tárolódnak, harmadik félnek (kivéve a KRÉTA és a kapcsolódó szolgáltatók a hibabejelentések kapcsán) NEM kerülnek továbbításra marketing vagy tárolási célból.
- A fejlesztők nem férnek hozzá a felhasználók bejelentkezési jelszavaihoz - azokat az alkalmazás nem tárolja.

Biztonsági intézkedések: alkalmazzuk a kommunikáció titkosítását, a minimalizált hozzáférést és a hibakezelés során az adatmegőrzés korlátozását (lásd alább).

## 5. Az adatkezelés céljai és jogalapjai
1. **KRÉTA-adatok megjelenítése az alkalmazásban** - cél: az alkalmazás alapfunkciója (szerződés teljesítése a felhasználóval). **Jogalap:** a szerződés teljesítése (GDPR 6. cikk (1) b)) vagy az érintett kifejezett kérése az alkalmazás használatához. *Ezek az adatok kizárólag a felhasználó eszközén kerülnek ideiglenesen tárolásra, és sem az alkalmazás fejlesztői, sem harmadik felek nem férnek hozzájuk. A Firka Management Csapat (mint adatkezelő) ezen adatokhoz semmilyen formában nem jut hozzá.*

2. **Hibajelentések kezelése** - cél: az alkalmazás működésének javítása. **Jogalap:** az érintett kifejezett hozzájárulása (GDPR 6. cikk (1) a)), mivel a hibajelentés során a felhasználó önkéntesen megoszt adatokat (pl. képernyőképet, hibanaplót).

3. **Szükséges technikai naplók kezelése (rendszeres működés biztosítása)** - cél: üzemeltetési/naplózási okok (hibakeresés rövid távon). **Jogalap:** jogos érdek (GDPR 6. cikk (1) f)), de csak minimális ideig és célhoz kötötten.

4. **Firka által biztosított online hírközlések** - cél: az API működésének ellenőrzése, hibák felderítése, valamint az app fejlesztői által fontosnak vélt hírek közlése. **Jogalap:** jogos érdek (GDPR 6. cikk (1) f)).

## 6. Adatmegőrzési időtartam
- **Lokálisan tárolt KRÉTA-adatok:** addig maradnak a készüléken, amíg az alkalmazást nem törli. A felhasználó maga önkényesen törölheti a lokálisan eltárolt adatokat.
- **Hibajegyek / hibajelentések (Discord / TestFlight):** a hibajegyeket a problémamegoldás idejére tároljuk, majd a jegy lezárása után azonnal törlésre kerülnek. (A felhasználó külön kérésére a törlést hamarabb is végrehajtjuk.)
- **Az API használata során közölt információk:** az IP-cím, valamint az API kérés fejlécei legfeljebb 90 napra kerülnek megőrzésre hibakeresési célból, majd automatikusan törlésre kerülnek. Indokolt esetben (pl. biztonsági incidens vizsgálatakor) ennél hosszabb megőrzés is lehetséges a jogszabályban előírt kötelezettségek teljesítése érdekében. Amennyiben nincs hiba vagy incidens, ezen naplókat nem tekintjük meg, és nem kerülnek feldolgozásra.

## 7. Adattovábbítás harmadik feleknek és nemzetközi adattovábbítás
- **KRÉTA (Educational Development Zrt.)**: az alkalmazás a KRÉTA rendszereiből szerzi az adatokat - ők az eredeti adatkezelők.
- **Hibabejelentések:** Androidon a fejlesztők részére a Discord szerverre feltöltött hibajegyek kerülhetnek továbbításra; iOS-en a TestFlight/Apple rendszeren keresztül érkezhetnek visszajelzések (az Apple adatszolgáltatási gyakorlata szerint). Ezek harmadik felek szolgáltatásai, amelyeknél fennállhat a nemzetközi adattovábbítás lehetősége (pl. Apple, Discord üzemeltetői infrastruktúra külföldön). Az ilyen esetekben a jogszerűségért a szolgáltató (pl. Discord, Apple) felel, illetve a szükséges jogi garanciák (pl. megfelelő adattovádelmi mechanizmusok) alkalmazását igyekszünk biztosítani.
- **Marketing, elemzés:** az alkalmazás nem továbbít adatokat marketing- vagy analitikai célokra harmadik feleknek.

## 8. Az érintett jogai és ezek gyakorlása
Az érintett az alábbi jogokkal rendelkezik:
- **Hozzáférés joga** az általa kezelt személyes adatokhoz;
- **Helyesbítés joga** (pontatlan adatok javítása);
- **Törlés joga** („elfeledtetés joga”), amennyiben nincs jogi ok az adatok további kezelése mellett;
- **Adatkezelés korlátozásának joga**;
- **Adathordozhatóság joga** (amennyiben az adatkezelés automatizált formában, strukturált, géppel olvasható formátumban történik és jogalapja szerződés vagy hozzájárulás);
- **Tiltakozás joga** a személyes adatok kezelése ellen, különösen jogos érdek alapján történő kezelés esetén;
- **Hozzájárulás visszavonása** (amennyiben az adatkezelés hozzájáruláson alapult), ami a jövőbeni további adatkezelést érinti, de nem érinti a visszavonás előtti kezelés jogszerűségét.

A jogok gyakorlásához kérjük, írj a **legal@firka.app** címre. A kérelem beérkezését követően ésszerű időn belül, de legkésőbb 1 hónapon belül válaszolunk; összetett ügy vagy különleges esetben a válaszadási határidőt további 2 hónappal meghosszabbíthatjuk, erről értesítést küldünk.

**Fontos**: a KRÉTA rendszerben tárolt adatok kezeléséért és megőrzéséért minden esetben az a köznevelési intézmény felel, ahol a gyerek tanul. A Firka alkalmazás csak megjeleníti azokat az eszközön, és nem tartja meg saját szerverein. Ezért a KRÉTA-adatok módosításával vagy törlésével kapcsolatban az iskolád (és annak általában a rendszergazdája vagy igazgatója) illetékes.

## 9. Panasz és jogorvoslat (jogi halandzsa)
Amennyiben az érintett úgy ítéli meg, hogy jogai sérültek, panasszal fordulhat a felügyeleti hatósághoz:

**Nemzeti Adatvédelmi és Információszabadság Hatóság (NAIH)**
- Székhely: 1055 Budapest, Falk Miksa utca 9-11
- Honlap: www.naih.hu
- E-mail: ugyfelszolgalat@naih.hu
- Levelezési cím: 1363 Budapest, Pf.: 9.

Az érintett ezen felül bírósági úton is érvényesítheti igényét.

## 10. Automatizált döntéshozatal és profilalkotás
Az alkalmazás nem alkalmaz automatizált döntéshozatalt vagy profilalkotást olyan módon, amely jogi hatással lenne az érintettre.

## 11. Egyéb rendelkezések
- A tájékoztató frissítése: a tájékoztatót szükség szerint frissítjük; fontos változás esetén a frissítést az alkalmazáson belül és a Firka szerverein (hírek) is jelezzük.
- Kapcsolat: minden adatvédelmi kérdéssel kapcsolatban a **legal@firka.app** címen keresztül várjuk a megkereséseket.

---

KRÉTA Adatvédelmi Tájékoztató: https://tudasbazis.ekreta.hu/pages/viewpage.action?pageId=4064926

Apple TestFlight Béta Tesztelő megosztott adatok listája: https://developer.apple.com/help/app-store-connect/reference/beta-tester-feedback

KRÉTA elérhetősége adatok módosításával, törlésével, vagy helyesbítésével kapcsolatban: https://www.e-kreta.hu/