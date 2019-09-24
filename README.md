# VectorMan 🇵🇦

El juego vectorman tal vez no fue tan importante en su infancia, pero prometo que no lo olvidaran despues de esto. Para la actividad de DEEP Q Learning, quiero entrenen a vectorman, para que sea capaz de entrenar bien en los niveles que se le coloquen.

#### Entregable
  - Pueden usar Human behaviour cloning, (aprender de los usuarios) o Q learning,
  - Se entrega un video de bitacora
  - Un articulo de no mas de 6 páginas explicando que hicieron 
  - FORMATO IEEE conferencia. 
  - Rodigo mejorado en un repositorio en GitHub

**PD:** para importar vectorman solo deben colocarlo en la carpeta rom de su entorno de trabajo y ejecutar el import script

Si es primera vez que copias o clonas el repositorio, para que funcione debes de serguir lo siguentes pasos.

**Pasos para ejecutar este proyecto** 👽📙
- **Recuerda primero crear tu entorno virtual de python.**
- **Ejecutar comandos**
```console
pip3 install -r requeriment.txt

python3 -m retro.import roms

python3 vectorman2.py       # Si se ejecuta 
```

Contenido del archivo original

```
import retro

env = retro.make('Vectorman2-Genesis')

env.reset()

done = False

while not done:
    env.render()

    action = env.action_space.sample()
    ob, rew, done, info = env.step(action)
    print("Action ", action, "Reward ", rew)

```
