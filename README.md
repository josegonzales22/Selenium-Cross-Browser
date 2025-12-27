# 🚀 Selenium Cross Browser – Automation Template

Framework base para **pruebas funcionales automatizadas** con ejecución **multinavegador**, soporte para ejecución *
*local y remota**, y generación automática de **reportes HTML** con dashboard.

Este proyecto sirve como *template* inicial para construir una arquitectura limpia y escalable de automatización con *
*Selenium WebDriver + JUnit 5 + Maven**, soportando ejecución en:

- **Chrome**
- **Edge**
- **Firefox**
- **Safari** *(solo local en macOS o remoto vía RemoteWebDriver)*
- **Remote WebDriver** (Selenium Grid, Selenoid, BrowserStack, LambdaTest, etc.)

## 📦 Características Principales

- ✔️ Ejecuta múltiples navegadores con un solo comando: `mvn clean test`
- ✔️ Descarga automática de drivers con **WebDriverManager**
- ✔️ Reportes HTML profesionales con **ExtentReports 5**
- ✔️ Arquitectura modular, limpia y escalable
- ✔️ Soporte completo para **RemoteWebDriver configurable**
- ✔️ Compatible con CI/CD (Windows/Linux/macOS)
- ✔️ Codificación UTF-8 forzada para ambientes CI
- ✔️ Perfiles Maven que activan Safari únicamente en macOS

## 🧩 Tecnologías Usadas

| Tecnología         | Versión | Uso                             |
|--------------------|---------|---------------------------------|
| Selenium WebDriver | 4.25.0  | Automatización web              |
| JUnit Jupiter      | 5.11.0  | Ejecución y estructura de tests |
| WebDriverManager   | 5.9.2   | Gestión automática de drivers   |
| ExtentReports      | 5.1.1   | Reportes HTML visuales          |
| Jackson Databind   | 2.18.0  | Manejo de configuración         |
| Apache Commons IO  | 2.16.1  | Manejo de archivos              |
| Maven              | –       | Build & dependency management   |

## ▶️ Ejecución del Proyecto

### 🔹 Ejecutar el siguiente comando

```bash
mvn clean test
```

## 🌐 Navegadores Soportados

### Ejecución Local

| Navegador | Local | Notas                     |
|-----------|-------|---------------------------|
| Chrome    | ✔️    | Windows, Linux, macOS     |
| Edge      | ✔️    | Windows, Linux, macOS     |
| Firefox   | ✔️    | Windows, Linux, macOS     |
| Safari    | ✔️    | Solo macOS (SafariDriver) |

### Ejecución en CI/CD

| Navegador | CI/CD Local | Notas                            |
|-----------|-------------|----------------------------------|
| Chrome    | ✔️          | Totalmente soportado             |
| Edge      | ✔️          | Totalmente soportado             |
| Firefox   | ✔️          | Totalmente soportado             |
| Safari    | ❌           | No soportado localmente en CI/CD |

> **Safari sí puede ejecutarse en CI/CD usando RemoteWebDriver.**

### RemoteWebDriver

Safari y cualquier otro navegador pueden ejecutarse mediante proveedores remotos:

- Selenium Grid
- Selenoid / Moon
- BrowserStack
- LambdaTest
- SauceLabs

## 📄 Reportes HTML (ExtentReports)

Los reportes se generan automáticamente en:

```
/reports/ExecutionReport_CrossBrowserSuite_<timestamp>.html
```

Incluyen:

- Dashboard general
- Pasos del flujo funcional
- Capturas de pantalla
- Resultados por navegador
- Detalle de errores

## ⚙️ Configuración Destacada del POM

- Compilación con Java 17
- Surefire configurado para ejecutar `CrossBrowserSuiteTest`
- Codificación UTF-8 forzada
- Perfiles Maven:
    - **windows** → excluye Safari
    - **mac** → activa soporte Safari
- Dependencias modernas y estables

## ⭐ Conclusión

**Selenium Cross Browser** es un template moderno y robusto que permite ejecutar pruebas funcionales en múltiples
navegadores, con reportes profesionales y compatibilidad total con pipelines CI/CD.

Ideal para:

- QA Automation
- Pruebas de regresión
- Validación cross-browser
- Integración continua

## Licencia

Este proyecto utiliza la [Licencia MIT](https://opensource.org/licenses/MIT).

## Disclaimer

La aplicación web utilizada en los ejemplos de este
proyecto [angular-dashboard-lime.vercel.app](https://angular-dashboard-lime.vercel.app) pertenece
a [Zoaib Khan](https://www.youtube.com/@ZoaibKhan). Se utiliza exclusivamente con fines educativos, demostrativos y para
prácticas de automatización.
