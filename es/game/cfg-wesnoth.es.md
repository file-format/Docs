{
"fecha": "2023-09-27",
  "keywords": [
"cfg",
"archivo cfg",
"archivo de lenguaje de marcado cfg wesnoth",
"¿Qué es un archivo cfg?",
"cómo abrir un archivo cfg",
"archivo",
"extensión de archivo cfg",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CFG - Archivo de lenguaje de marcado Wesnoth",
  "description":"Obtenga más información sobre el formato de archivo CFG Wesnoth Markup Language y las API que pueden crear y abrir archivos CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent" : "game"
}
},
"última modificación": "2023-09-27"
}

## ¿Qué es un archivo CFG?

El archivo CFG también se conoce como **"Wesnoth Markup Language" (WML)**. Es un lenguaje de marcado personalizado que se utiliza principalmente en el juego "Battle for Wesnoth", que es un juego de estrategia por turnos. WML se utiliza para definir y personalizar varios aspectos del juego, incluidos escenarios, campañas, unidades y más. Es una forma para que los modders y desarrolladores creen contenido para el juego.

Está escrito en un formato que se asemeja a una combinación de XML y secuencias de comandos simples. A continuación se ofrece una descripción general de algunos elementos y estructuras comunes que puede encontrar en un archivo WML:

1. **Etiquetas:** WML usa etiquetas para definir diferentes elementos en el juego. Las etiquetas están encerradas entre corchetes angulares. Por ejemplo:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atributos:** Dentro de las etiquetas, puede definir atributos para especificar propiedades o valores asociados con el elemento. En el ejemplo anterior, "tipo" y "puntos de impacto" son atributos.
    










3. **Matrices y matrices de matrices:** Puedes crear matrices de datos e incluso matrices de matrices para definir listas de unidades, tipos de terreno u otros elementos del juego.
    










4. **Declaraciones condicionales:** WML admite declaraciones condicionales para controlar el flujo del juego. Por ejemplo:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Bucles:** Puede utilizar bucles para recorrer listas de elementos o realizar acciones repetidamente.
    










6. **Incluye:** Puede incluir otros archivos WML dentro de un archivo WML principal para organizar y modularizar su contenido.
    










7. **Controladores de eventos:** Puedes definir controladores de eventos para activar acciones cuando ocurren eventos específicos en el juego.
    











A continuación se muestra un ejemplo simplificado de un archivo WML que define una unidad personalizada:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## La batalla por Wesnoth

"The Battle for Wesnoth" es un popular juego de estrategia por turnos de código abierto. Está disponible para múltiples plataformas, incluidas Mac, Windows, Linux y más. Desarrollado por una dedicada comunidad de voluntarios, el juego es conocido por su juego profundo y atractivo, así como por su rico mundo de fantasía.

Las características clave de "La batalla por Wesnoth" incluyen:

1. **Escenario de fantasía:** El juego se desarrolla en un mundo de fantasía con varias razas, incluidos humanos, elfos, enanos, orcos y más. La historia y la narración del juego son una parte integral de su atractivo.
    










2. **Estrategia por turnos:** El juego se basa en turnos, donde los jugadores se toman su tiempo para planificar y ejecutar sus movimientos en cuadrículas hexagonales. Combina el combate táctico con la toma de decisiones estratégicas.
    










3. **Campañas:** El juego ofrece una amplia gama de campañas para un jugador, cada una con su propia historia, personajes y desafíos. Los jugadores pueden explorar diferentes narrativas y escenarios.
    










4. **Multijugador:** "Wesnoth" admite el modo multijugador en línea, lo que permite a los jugadores competir entre sí en batallas estratégicas. Los modos multijugador incluyen juego cooperativo y partidos competitivos.

## ¿Cómo abrir el archivo CFG?

Los archivos CFG, que se asocian comúnmente con el lenguaje de marcado Wesnoth (WML) utilizado en el juego "The Battle for Wesnoth", se pueden editar fácilmente con cualquier editor de texto estándar. Estos archivos contienen código legible por humanos escrito en WML, que define varios aspectos del juego, incluidos escenarios, unidades y campañas.

Si bien puede utilizar cualquier editor de texto para modificar archivos CFG, algunos editores de texto avanzados como Emacs y Vi tienen complementos de resaltado de sintaxis WML disponibles. Estos complementos proporcionan códigos de colores y formatos útiles para que a los usuarios les resulte más fácil distinguir diferentes elementos y estructuras dentro del código WML.

Los programas que abren o hacen referencia a archivos CFG incluyen

- La batalla por Wesnoth (Gratis) para (Windows, MAC, Linux)
- Bloc de notas de Microsoft

## Otros archivos CFG

Aquí hay otros tipos de archivos que usan la extensión de archivo **.cfg**.

**Ajustes**
- [CFG - Archivo de configuración de Celestia](/es/settings/cfg-celestia/)
- [CFG - Archivo de conexión del servidor Citrix](/es/settings/cfg-citrix/)
- [CFG - Archivo de configuración MAME](/es/settings/cfg-mame/)
- [CFG - Archivo de configuración LightWave](/es/settings/cfg-lightwave/)

**Juego**
- [CFG - Archivo de lenguaje de marcado Wesnoth](/es/game/cfg-wesnoth/)
- [CFG - Archivo de configuración MUGEN](/es/game/cfg-mugen/)
- [CFG - Archivo de configuración del motor fuente](/es/game/cfg-sourceengine/)

**Sistema y miscelánea**
- [CFG - Archivo CFG](/es/system/cfg/)
- [CFG - Archivo de configuración del modelo Cal3D](/es/misc/cfg-cal3d/)

## Referencias
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
