<p align="center"><img src="https://raw.githubusercontent.com/DrakesCraft-Labs/Obsidian-Armor/main/banner.svg" alt="Obsidian-Armor" width="100%"></p>

# Obsidian-Armor

> ### 🏰 ¡Únete a la Comunidad Oficial de DrakesCraft!
> 
> * 🎮 **IP del Servidor**: `play.drakescraft.net` *(Java 1.21.11 & Bedrock)*
> * 💬 **Discord Oficial**: [discord.gg/drakescraft](https://discord.gg/rR7FbfCt9Y)
> * 🌐 **Web & Guía**: [drakescraft.net](https://drakescraft.net) — 🛒 **Tienda**: [tienda.drakescraft.net](https://tienda.drakescraft.net)
> 
> *¡Juega con este addon y más de 80 expansiones optimizadas en vivo en nuestra network de supervivencia técnica!*

---

Una armadura completa de aleación de obsidiana, adaptada al ecosistema Slimefun de
**DrakesCraft** (Paper/Purpur 1.21.11, Java 21).

## Qué añade

**Aleación de Obsidiana**, que se fabrica en la mesa de trabajo mejorada rodeando un bloque de
obsidiana con ocho diamantes.

**Cuatro piezas de armadura** — casco, peto, grebas y botas — hechas con esa aleación siguiendo
la disposición normal de cada pieza. Todas salen encantadas de fábrica.

## Qué cambiamos

Este repositorio **no es un fork**: es el código original integrado en el ecosistema de
DrakesCraft. Los cambios son estos.

**Usaba la API de Slimefun anterior a 2021.** `Category`, `CustomItem`, `RecipeType` y
`SlimefunItemStack` no solo se movieron de paquete: se repartieron entre destinos distintos, y
unas se renombraron por el camino. Están redirigidas una a una.

**Dependía de `org.bukkit:bukkit` 1.15.2.** Es el artefacto anterior incluso a `spigot-api`, y
fue el cambio que más costó ver: resolvía sin dar un solo error, así que el build parecía sano,
pero dejaba en el classpath una API de 1.15 donde la mitad de las constantes modernas todavía no
existían. El síntoma era un `cannot find symbol` sobre `Enchantment.UNBREAKING`, que sí está en
paper-api y no llevaba a ninguna parte hasta mirar qué jar había debajo. Ahora compila contra
paper-api 1.21.11, la misma versión que corre el servidor.

**`api-version` subió de 1.14 a 1.21**, para que Paper no le aplique reglas de compatibilidad
que ya no hacen falta.

## Pendiente

**Los nombres de los objetos siguen en chino.** El addon viene con 109 caracteres sin traducir;
la sesión de traducción va aparte.

**Los encantamientos están muy por encima de lo vanilla.** Cada una de las cuatro piezas lleva a
la vez Protección IV, Protección contra el Fuego VI y Protección contra Explosiones VI, y el
casco además Irrompibilidad III. En vanilla las tres protecciones son mutuamente excluyentes y
ninguna pasa de IV, así que un juego completo se acerca al tope de reducción de daño del juego
frente a fuego y explosiones. Está sin tocar a propósito: rebalancearlo es una decisión de
servidor, no de port.

## Créditos

Addon original de **JordanG8**. Este repositorio solo lo adapta.

## ⚖️ Upstream Attribution & License / Licencia y Créditos

- **Original Project / Upstream**: Slimefun4 Community Addon.
- **Port & Maintenance**: DrakesCraft Labs team (Compatibility for Paper / Purpur 1.21.11).
- **License**: GPL-3.0 / MIT.
- **Source Code**: [GitHub Repository](https://github.com/DrakesCraft-Labs/Obsidian-Armor)
- **Support & Issues**: [GitHub Issues](https://github.com/DrakesCraft-Labs/Obsidian-Armor/issues) | [Discord](https://discord.gg/rR7FbfCt9Y)

*This project is an open-source derivative work maintained by DrakesCraft Labs under the terms of its original license. All original assets and concepts belong to their respective creators.*
