## pront:
antes de continuar con los proximos pasos, quiero los paso para poder crear un nuevo proyecto en local, luego de crear el proyecto en local copiare los archivos

## Pasos para Crear el Proyecto Local

### 1. **Crear el Proyecto Next.js**

```shellscript
# Crear nuevo proyecto Next.js con TypeScript
npx create-next-app@latest newclosbell --typescript --tailwind --eslint --app --src-dir=false --import-alias="@/*"

# Navegar al directorio del proyecto
cd newclosbell
```

### 2. **Instalar Dependencias Adicionales**

```shellscript
# Instalar shadcn/ui
npx shadcn@latest init

# Cuando te pregunte por la configuración, usa estos valores:
# ✔ Would you like to use TypeScript (recommended)? … yes
# ✔ Which style would you like to use? › Default
# ✔ Which color would you like to use as base color? › Slate
# ✔ Where is your global CSS file? … app/globals.css
# ✔ Would you like to use CSS variables for colors? … yes
# ✔ Where is your tailwind.config.js located? … tailwind.config.ts
# ✔ Configure the import alias for components? … @/components
# ✔ Configure the import alias for utils? … @/lib/utils

# Instalar componentes de shadcn/ui necesarios
npx shadcn@latest add button
npx shadcn@latest add card
npx shadcn@latest add input
npx shadcn@latest add label
npx shadcn@latest add dialog
npx shadcn@latest add dropdown-menu
npx shadcn@latest add avatar
npx shadcn@latest add alert

# Instalar iconos de Lucide React
npm install lucide-react

# Instalar next-themes para el sistema de temas
npm install next-themes
```

### 3. **Crear la Estructura de Directorios**

```shellscript
# Crear estructura de módulos
mkdir -p modules/auth/components
mkdir -p modules/auth/types
mkdir -p modules/landing/components
mkdir -p modules/user-choice/components
mkdir -p modules/business/components
mkdir -p modules/business/types
mkdir -p modules/clients/components
mkdir -p modules/clients/types

# Crear directorio de documentación
mkdir docs

# Crear directorio lib si no existe
mkdir -p lib
```

### 4. **Verificar la Estructura del Proyecto**

Después de crear los directorios, tu estructura debería verse así:

```plaintext
newclosbell/
├── app/
│   ├── favicon.ico
│   ├── globals.css
│   ├── layout.tsx
│   └── page.tsx
├── components/
│   └── ui/
│       ├── button.tsx
│       ├── card.tsx
│       ├── dialog.tsx
│       ├── input.tsx
│       └── label.tsx
├── lib/
│   └── utils.ts
├── modules/
│   ├── auth/
│   │   ├── components/
│   │   └── types/
│   ├── landing/
│   │   └── components/
│   ├── user-choice/
│   │   └── components/
│   ├── business/
│   │   ├── components/
│   │   └── types/
│   └── clients/
│       ├── components/
│       └── types/
├── docs/
├── next.config.mjs
├── package.json
├── tailwind.config.ts
└── tsconfig.json
```

### 5. **Configurar Variables de Entorno**

```shellscript
# Crear archivo de variables de entorno
touch .env.local

# Agregar al archivo .env.local:
echo "NEXT_PUBLIC_API_URL=http://localhost:3001" >> .env.local
```

### 6. **Verificar la Instalación**

```shellscript
# Ejecutar el proyecto para verificar que todo funciona
npm run dev
```

El proyecto debería ejecutarse en `http://localhost:3000`

### 7. **Preparar para Copiar Archivos**

Una vez que tengas la estructura base creada, puedes:

1. **Copiar los archivos** del código que te proporcioné
2. **Reemplazar** los archivos existentes (como `app/layout.tsx`, `app/page.tsx`, etc.)
3. **Crear** los nuevos archivos en sus respectivos directorios


### 8. **Archivos a Reemplazar/Crear**

**Reemplazar estos archivos existentes:**

- `app/layout.tsx`
- `app/page.tsx`
- `app/globals.css`


**Crear estos nuevos archivos:**

- `app/user-choice/page.tsx`
- `app/business/page.tsx`
- `app/clients/page.tsx`
- Todos los archivos en `modules/`
- `lib/api-config.ts`
- `docs/README.md`
- `docs/TECHNICAL_GUIDE.md`


### 9. **Instalar Theme Provider**

```shellscript
# Crear el theme provider
npx shadcn@latest add theme-provider
```

### 10. **Verificación Final**

Después de copiar todos los archivos:

```shellscript
# Instalar dependencias (por si acaso)
npm install

# Ejecutar el proyecto
npm run dev
```

## 🎯 Resumen de Comandos Completos

```shellscript
# 1. Crear proyecto
npx create-next-app@latest newclosbell --typescript --tailwind --eslint --app --src-dir=false --import-alias="@/*"
cd newclosbell

# 2. Configurar shadcn/ui
npx shadcn@latest init

# 3. Instalar componentes
npx shadcn@latest add button card input label dialog dropdown-menu avatar alert
npm install lucide-react next-themes

# 4. Crear estructura
mkdir -p modules/{auth,landing,user-choice,business,clients}/{components,types}
mkdir docs

# 5. Variables de entorno
echo "NEXT_PUBLIC_API_URL=http://localhost:3001" > .env.local

# 6. Verificar
npm run dev
```

Una vez completados estos pasos, tendrás la estructura base lista para copiar todos los archivos del código que implementé. ¿Te gustaría que proceda con algún paso específico o tienes alguna pregunta sobre la configuración?
