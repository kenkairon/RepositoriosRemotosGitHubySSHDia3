# **Ejercicio**: Configura SSH y conecta con GitHub

## Generar clave SSH:

```bash
ssh-keygen -t ed25519 -C "tu.email@ejemplo.com"
# Presiona Enter para todas las preguntas (usa passphrase si quieres)
```

## Agregar clave el agente SSH:

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

## Copiar clave pública:

```bash
cat ~/.ssh/id_ed25519.pub
# Copia toda la salida
```

## Agregar a GitHub:


- Ve a GitHub.com → Settings → SSH and GPG keys
- Click "New SSH key"
- Pega la clave pública y guarda

## Probar conexión

```bash
ssh -T git@github.com
# Deberías ver un mensaje de bienvenida
```

## Crear repositorio remoto (desde el repo local del día anterior):

```bash
# En GitHub, crea un nuevo repositorio vacío
git remote add origin git@github.com:TU_USUARIO/NOMBRE_REPO.git
git push -u origin main
```

## Verificación: Confirma que puedes hacer push y pull sin ingresar contraseña.

Requerimientos:
- Git instalado y configurado (del día anterior)
- Cuenta en GitHub (github.com)
- Terminal con acceso a comandos SSH
