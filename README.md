# NodeJsFirebase
Pasos de configuracion Node Js para notificaciones en firebase:
- instalamos express:
    npm install -g express
    npm install express
- instalamos el admin de firebse:
  npm install firebase-admin
Lo siguiente es ir a la configuración del proyecto y descargarse el archivo de configuracion (json).
Tenemos que ir al apartado cuentas de servicio -> sdk de administrador de firebase
pulsamos en node js y generar nueva clave privada.
luego hay que hacer referencia en el codigo a la ruta donde subimos este archivo 

var admin = require("firebase-admin");
admin.initializeApp({
credential: admin.credential.cert("ruta del fichero descargado"),
databaseURL: "https://nombre-de-tu-aplicacion.firebaseio.com"
});
