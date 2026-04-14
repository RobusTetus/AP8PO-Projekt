# Koncept Hry: Projekt: Steel & Glory

## 1. Základní Pilíře (Core Pillars)

- **Souboje:** Soubojový systém založený na načasování a reakcích.
- **Více druhů zbraní:** Použití Resources v Godot Engine.
- **Multiplayer:** Hra je od základu navržena pro hraní více hráčů v reálném čase.

---

## 2. Multiplayer Architektura

- **Model:** Klient je zároveň serverem pro ostatní klienty.
- **Synchronizace:**
  - `MultiplayerSynchronizer`: Pro plynulou synchronizaci pozice, rotace a akce hráčů.
  - `MultiplayerSpawner`: Pro dynamické instanciování projektilů (šípy, vrhací sekery) a efektů.

---

## 3. Systém Zbraní

- Více druhů zbraní. Každá zbraň bude obsahovat.
  - Typ
  - Poškození
  - Rychlost útoku
  - Schopnost vrhnutí
  - popř. Schopnost vystřelit
  - ...

---

## 4. FPS Bojový Systém

- **Lehký i těžký útok:** Rozdíl v poškození na úkor rychlosti útoku a spotřeby staminy.
- **Parry (Odražení):** Krátké okno pro blokování, které krátkodobě omráčí nepřítele.
- **Stamina:** Každý švih a skok spotřebovává výdrž, což zabraňuje bezhlavému klikání.
- **Detekce zásahu:** Využití `ShapeCast3D` pro detekci kolize zbraně s tělem nebo zbraní nepřítele.

---

## 5. Technický Stack (Godot 4.x)

- **CharacterBody3D:** Pro pohyb hráče.
- **NavigationRegion3D:** Pro practice mód a boty.
- **Environment:** Využití shaderů a filtrů pro navození atmosféry.
