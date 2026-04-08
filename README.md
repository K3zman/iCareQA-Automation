# 📱 iCareQA-Automation

Framework de automatización de pruebas móviles para la aplicación **iCare**, desarrollado como parte del proceso de aseguramiento de calidad end-to-end. Cubre flujos críticos en Android e iOS usando WebdriverIO + Appium con metodología BDD.

---

## 🛠️ Stack Tecnológico

| Categoría | Tecnología |
|-----------|-----------|
| Automatización móvil | WebdriverIO + Appium |
| Metodología | BDD — Gherkin / Cucumber |
| Lenguaje | JavaScript |
| Reportes | Allure Reports |
| Control de versiones | Git / GitHub |

---

## ✅ Cobertura de Pruebas

- 🔐 **Login** — flujos de autenticación (cuenta estándar y premium)
- 📝 **Registro de usuario** — validación de flujo completo y con bloqueantes
- 👤 **Cuenta profesional** — registro estándar y premium
- 📊 **Generación de informes** — validación de flujo exitoso
- 💨 **Smoke tests** — validación rápida de funcionalidades críticas

---

## 📁 Estructura del Proyecto

```
config/
├── package.json
├── wdio.conf.js
├── .gitignore
├── apps/
│   └── myapp.apk
├── config/                      # Configuración por entorno
│   ├── capabilities.android.js
│   ├── capabilities.ios.js
│   └── env.dev.json
├── features/                    # Gherkin — escenarios BDD
│   ├── login/
│   │   ├── login.feature
│   │   └── login.data.json
│   ├── common/
│   │   └── smoke.feature
│   └── step-definitions/
│       ├── login.steps.js
│       └── hooks.steps.js
├── pageobjects/                 # Patrón POM
│   └── base/
│       ├── BasePage.js
│       └── selectors/
│           ├── screens/
│           │   ├── LoginScreen.js
│           │   └── HomeScreen.js
│           └── components/
│               ├── BottomNav.js
│               └── PermissionModal.js
├── testdata/
│   ├── users.json
│   └── fixtures.json
├── utils/
│   ├── wait.js
│   ├── logger.js
│   └── random.js
└── reports/
    ├── screenshots/
    ├── videos/
    └── allure-results/
```

---

## 🚀 Cómo ejecutar

### Requisitos previos

- Node.js >= 16
- Appium instalado: `npm install -g appium`
- Android Studio (emulador Android) o Xcode (iOS)
- Dispositivo físico o emulador activo

### Instalación

```bash
git clone https://github.com/K3zman/iCareQA-Automation.git
cd iCareQA-Automation/config
npm install
```

### Ejecutar pruebas

```bash
# Todas las pruebas
npm test

# Solo smoke tests
npm run test:smoke

# Generar reporte Allure
npm run report
```

---

## 📊 Reportes

Los reportes se generan con **Allure** en `reports/allure-results/`. Para visualizarlos:

```bash
allure serve reports/allure-results/
```

---

## 🧠 Patrones y Buenas Prácticas Aplicadas

- **Page Object Model (POM)** — separación de selectores y lógica de prueba
- **BDD con Gherkin** — escenarios legibles por negocio y técnicos
- **Data-driven testing** — datos de prueba externos en JSON
- **Separación de ambientes** — configuración por entorno (dev, staging)
- **Hooks Before/After** — setup y teardown automatizados
- **Logging y screenshots** — evidencias automáticas en fallos

---

## 👤 Autor

**Kezman Santiago Riaño González**  
QA Tester | Automatización de Pruebas  
📧 kez.rigo@gmail.com  
🔗 [github.com/K3zman](https://github.com/K3zman)
