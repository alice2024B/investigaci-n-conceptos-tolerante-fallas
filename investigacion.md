#Investigación: Conceptos básicos en sistemas tolerantes a fallas

**Materia:** Computación tolerante a fallas

##Objetivo

Conocer los conceptos básicos en sistemas tolerantes a fallas.

##Introducción

Los sistemas computacionales están expuestos a diferentes problemas que pueden afectar su funcionamiento. Estos problemas pueden aparecer en los componentes físicos, en los programas, en las redes o por factores externos.

Por esta razón, es importante conocer los sistemas tolerantes a fallas y la manera en que pueden continuar funcionando cuando alguno de sus componentes presenta un problema.

##Desarrollo
1. ¿Qué son los sistemas tolerantes a fallas?
Un sistema tolerante a fallas es aquel que está diseñado para continuar proporcionando un servicio correcto aunque se presente algún problema en uno de sus componentes.
La idea principal no es evitar que todas las fallas ocurran, porque en un sistema real es difícil garantizar que nunca sucederá ninguna. En cambio, se busca que cuando ocurra una falla, el sistema pueda detectarla, manejarla y, cuando sea posible, continuar funcionando sin que el usuario note una interrupción importante.
Por ejemplo, un servidor puede tener dos fuentes de alimentación. Si una deja de funcionar, la otra puede continuar proporcionando energía. De esta manera, el servidor puede seguir funcionando aunque uno de sus componentes presente una falla.

2. ¿Qué es una falla?
Una falla es una condición o defecto que puede provocar que un componente de un sistema no funcione de acuerdo con lo esperado.
Una falla puede tener diferentes causas. Por ejemplo, puede producirse por un defecto en un componente de hardware, un problema de programación, una interrupción eléctrica o un problema en la comunicación entre dispositivos.
Un ejemplo sería una memoria RAM que presenta un defecto físico. Esa condición puede provocar posteriormente que el sistema maneje información de manera incorrecta.

3. ¿Qué es un error?
Un error es un estado interno incorrecto que se encuentra dentro de un sistema y que puede haber sido provocado por una falla.
Por ejemplo, si una memoria presenta una falla y como consecuencia se almacena información incorrecta, ese estado incorrecto representa un error.
Un error no necesariamente es visible para el usuario. Si el sistema consigue detectarlo y corregirlo antes de que afecte al servicio, el usuario puede no darse cuenta de que ocurrió un problema.

4. ¿Qué es una latencia de un fallo?
La latencia de un fallo es el período de tiempo que transcurre entre el momento en que ocurre una falla y el momento en que esa falla se manifiesta como un error dentro del sistema.
Por ejemplo, un componente puede comenzar a presentar un problema interno, pero continuar funcionando aparentemente con normalidad durante cierto tiempo. Cuando finalmente produce una condición incorrecta, ha pasado un período entre la aparición de la falla y la aparición del error.

5. ¿Qué es la latencia de un error?
La latencia de un error es el tiempo que transcurre desde que se produce un error hasta que este se manifiesta como un fallo que afecta el servicio proporcionado por el sistema.
Por ejemplo, puede existir información incorrecta dentro de la memoria de un sistema, pero mientras esa información no sea utilizada, el usuario podría no notar ningún problema. Si posteriormente un programa utiliza ese dato y produce un resultado incorrecto, el error se ha manifestado como un fallo.

6. Tipos de fallos:
Transitorio: ocurre durante un tiempo y después desaparece.
Ejemplo: una interferencia eléctrica que afecta un equipo por unos segundos.

Fallo intermitente: aparece y desaparece varias veces.
Ejemplo: un cable que a veces funciona y a veces pierde la conexión.

Fallo permanente: continúa hasta que se repara o cambia el componente.
Ejemplo: un disco duro que deja de funcionar por un daño físico.

7. Métricas clave:
Disponibilidad: indica cuánto tiempo un sistema está funcionando y disponible para usarse.

Confiabilidad: indica qué tan probable es que un sistema funcione correctamente durante un período sin presentar fallos.

MTTF (Mean Time To Failure: es el tiempo promedio que un componente funciona antes de fallar.

MTTR(Mean Time To Repair: es el tiempo promedio que se necesita para reparar un sistema después de una falla.

8. Conclusión
Los sistemas tolerantes a fallas permiten que un sistema siga funcionando aunque alguna parte presente un problema. Para estudiarlos es importante conocer las diferencias entre falla, error y fallo, además de los tipos de fallos y las métricas que ayudan a medir qué tan confiable y disponible es un sistema.
