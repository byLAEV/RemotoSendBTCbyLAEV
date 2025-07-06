# RemotoSendBTCbyLAEV
Bitcoin Sends from the Termux Client with Remote Node 
# RemotoSendBTCbyLAEV

**Repositorio oficial del Cartel de Bitcoiners para envío remoto de transacciones en la red Bitcoin desde Termux.**

Este script permite solicitar el envío de BTC desde un cliente CLI en Termux, autenticado y vinculado a un backend seguro o nodo autorizado. El envío se completa tras verificación y aprobación remota.

---

## ⚙️ Funcionalidad

El cliente ejecuta un comando como:

```bash
sendbtc --to <walletBTC> --amount <monto_en_btc> [--memo "mensaje opcional"]

Esto genera una solicitud remota firmada y la envía a un backend controlado por LAEV o por un operador autorizado. Si la identidad es validada, se firma la transacción y se transmite a la red Bitcoin. Se devuelve el TXID como respuesta.


---

📦 Instalación

Requisitos en el cliente (Termux o Linux):

python3, curl, gnupg

Clave API o firma GPG exportada

Acceso a Internet

Permisos ejecutables


git clone https://github.com/LAEV/RemotoSendBTCbyLAEV.git
cd RemotoSendBTCbyLAEV
chmod +x sendbtc
./sendbtc --help


---

🧪 Modo de uso

./sendbtc --to bc1qexampleaddress... --amount 0.001 --memo "Prueba de vida LAEV"

Opcionalmente, puedes usar variables de entorno:

export API_KEY="..."
export REMOTO_NODE="https://remoto.laev.network"


---

🔐 Seguridad y arquitectura

El cliente nunca almacena claves privadas.

La autenticación puede realizarse vía:

Clave API cifrada (recomendado)

Firma GPG (opcional)


El backend valida:

Identidad

Límites diarios / cuotas

Autorización explícita o confirmación vía WhatsApp/Signal/Nostr


Todas las acciones quedan registradas con timestamp, IP y hash.



---

📡 Backend

Basado en FastAPI + RPC Bitcoin Core o ElectrumX

Opcional: PSBT only (requiere firma offline o vía hardware wallet)

Logs de auditoría firmados y cifrados.

Puede operar en caliente (hot wallet) o como multisig con voto remoto.



---

🛡️ Casos de uso

Verificación de estado físico / "prueba de vida" mediante firma obligatoria cada X horas.

Envíos programados tras validación remota.

Aplicaciones penitenciarias (bracelets vinculados al backend).

Registro de actividad, pagos u obligaciones legales en la red Bitcoin.



---

🧠 Visión del proyecto

Esta herramienta es parte del stack operativo del Cartel de Bitcoiners, para ofrecer alternativas descentralizadas de gobernanza, firma de voluntad, y ejecución en la red sin depender de custodios centralizados ni de interfaces gráficas. El objetivo es crear soberanía operativa remota.


---

🧾 Licencia

LICENCIA LAEV v1.0 – Ética y Código Abierto.

Este software se distribuye bajo los principios de soberanía tecnológica, pero NO puede ser usado por gobiernos, agencias estatales, partidos políticos, ONGs financiadas por fiat, ni estructuras que violen la privacidad individual.

Uso permitido: ✔ Bitcoiners soberanos
✔ Individuos autónomos
✔ Colectivos sin fines coercitivos

Uso prohibido: ✖ Intermediarios bancarios
✖ Agencias de inteligencia
✖ Gobiernos o alianzas militares

> "Si no es con libertad, no hay transacción." – LAEV




---

✊ Autoría

Desarrollado por LAEV
Fundador del Cartel de Bitcoiners
Costa Rica – El Salvador – Cypherpunks Planetarios
laev.lab.ele@gmail.com


---

---

