# GymPlan

App web para el gimnasio: arma planes de entrenamiento con Gemini, busca
ejercicios con su animación y registra tus entrenamientos.

**Usala en:** <https://turuleca82.github.io/>

## Instalarla en el iPhone

1. Abrí el link en **Safari** (desde Chrome no se puede instalar).
2. Tocá **Compartir** (el cuadrado con la flecha hacia arriba).
3. Elegí **Agregar a pantalla de inicio**.

Queda con su ícono, a pantalla completa, y funciona sin conexión una vez
abierta. En Android también se puede instalar desde Chrome (menú →
*Instalar app* / *Agregar a la pantalla principal*).

## Instalarla en Android (APK)

Descargá el APK desde el celular:
<https://turuleca82.github.io/GymPlan.apk>
(también está en <https://github.com/Turuleca82/turuleca82.github.io/releases/download/apk/GymPlan.apk>)

Abrilo para instalarlo. La primera vez Android pide permitir instalar apps
desde el navegador (*Permitir desde esta fuente*); si aparece Play Protect,
tocá *Más detalles → Instalar de todas formas*. No hace falta cuenta de
GitHub.

## API key de Gemini

Para generar planes hace falta una API key gratuita de Google AI Studio:
<https://aistudio.google.com/apikey>. Se carga en el último paso de la
pantalla inicial o en **Ajustes**, y queda guardada solo en tu teléfono. Cada
persona tiene que usar su propia key.

En **Ajustes → Modelo**, dejá "Automático": la app usa el modelo Flash más
nuevo disponible y cambia sola si Google retira uno.

## Qué hace

- **Plan a medida:** según tus datos, objetivo, días por semana y minutos por
  sesión.
- **Buscador de ejercicios** en español, con animación, músculos y técnica.
- **Cambiar un ejercicio** por otro del mismo músculo si falta la máquina.
- **Galería:** cada ejercicio que abrís queda guardado como GIF en el teléfono.
- **Registro de entrenamientos** con temporizador de descanso, y **progreso**
  por ejercicio.

Todos los datos (perfil, planes, historial, API key) quedan solo en tu
teléfono. Si la usás desde Safari sin instalarla, iOS puede borrarlos después
de varios días sin uso: instalala en la pantalla de inicio.

## Desarrollo

El código está en `app/`:

```bash
cd app
npm install
npm run dev     # abre la app en el navegador
npm run build   # genera app/dist/
```

Cada cambio en `app/` se compila solo y la versión lista para usar se publica
en la raíz de `main` y en la rama `gh-pages`
(`.github/workflows/web.yml`). Los archivos de la raíz (`index.html`,
`assets/`, etc.) los genera ese proceso: no se editan a mano.

Imágenes de ejercicios: [free-exercise-db](https://github.com/yuhonas/free-exercise-db)
(dominio público).
