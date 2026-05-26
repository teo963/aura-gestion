# 🔥 GUÍA DE CONFIGURACIÓN FIREBASE - AURA GESTIÓN

## ✅ Estado Actual
- ✅ Proyecto Firebase creado
- ✅ Base de datos Realtime creada
- ✅ Aplicación web configurada
- ✅ App AURA con Firebase integrado

---

## 🚀 CÓMO USAR LA APP CON FIREBASE

### OPCIÓN A: Usar localmente (en tu ordenador)
1. **Descarga** `aura_gestio_FIREBASE.html`
2. **Abre** en tu navegador
3. Los datos se guardarán tanto **localmente** como **en Firebase**
4. Puedes acceder desde otros navegadores/ordenadores y verás los mismos datos

### OPCIÓN B: Publicar en internet (RECOMENDADO para acceso remoto)

#### Usando GitHub Pages (GRATIS):

1. **Crea una cuenta en** [GitHub.com](https://github.com)

2. **Crea un nuevo repositorio:**
   - Nombre: `aura-gestion`
   - Público
   - Sin README

3. **Sube los archivos:**
   ```bash
   git clone https://github.com/tunombre/aura-gestion.git
   cd aura-gestion
   # Copia aquí: aura_gestio_FIREBASE.html
   # Copia aquí: Descargar_Plantilla.html
   # Copia aquí: Plantilla_Importacion_Facturas.xlsx
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

4. **Activa GitHub Pages:**
   - Ve a Settings → Pages
   - Branch: main
   - Clic en Save

5. **Tu app estará en:**
   ```
   https://tunombre.github.io/aura-gestion/aura_gestio_FIREBASE.html
   ```

6. **Comparte el link** con otros dispositivos

---

## 📊 CÓMO FUNCIONA FIREBASE

### Sincronización automática:
- ✅ Guardas datos en la app → Se guardan en Firebase automáticamente
- ✅ Cambias desde otro dispositivo → Los datos se sincronizan en tiempo real
- ✅ Sin conexión → Los datos se guardan localmente y se sincronizan cuando conectes

### Datos guardados en Firebase:
```
aura-gestion/
  users/
    anonymous/
      alumnes/
      factures/
      gastos/
      previsions/
      beques/
      etc...
```

---

## 🔐 SEGURIDAD

**IMPORTANTE:** Las reglas de seguridad actuales están en "test mode" (acceso público por 30 días).

Para producción, ve a Firebase → Realtime Database → Reglas:

```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "$uid === auth.uid || auth.uid === null",
        ".write": "$uid === auth.uid || auth.uid === null"
      }
    }
  }
}
```

---

## 📱 ACCEDER DESDE MÚLTIPLES DISPOSITIVOS

1. Abre el link desde tu teléfono, tablet, otro ordenador
2. **Todos verán los mismos datos**
3. Los cambios se sincronizan en **tiempo real**

### Ejemplo:
- Tu ordenador: Agregas una factura
- Tu teléfono: ¡La factura aparece automáticamente!

---

## 🆘 SOLUCIÓN DE PROBLEMAS

### No sincroniza:
1. Comprueba que tienes conexión a internet
2. Abre la consola del navegador (F12)
3. Busca mensajes de error con "Firebase"

### Datos no aparecen en otro dispositivo:
1. Espera 30 segundos (tiempo de sincronización)
2. Recarga la página
3. Si sigue sin aparecer, comprueba que ambos usan la misma cuenta Firebase

### ¿Cómo hacer login personal? (AVANZADO)
Puedo agregarte autenticación por email. Avísame si lo necesitas.

---

## 📞 PRÓXIMOS PASOS

1. ✅ Usa `aura_gestio_FIREBASE.html` en tu ordenador
2. ✅ Prueba que los datos se guardan y sincronizan
3. ✅ (Opcional) Publica en GitHub Pages si quieres acceso desde internet
4. ✅ Comparte el link con otros usuarios

---

**¿Necesitas ayuda? Avísame cualquier duda.**
