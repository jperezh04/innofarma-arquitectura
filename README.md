# Innofarma — Visor Interactivo de Arquitectura de Software (Marifarma)

Visor interactivo en HTML/SVG de la Arquitectura de Software del sistema **Innofarma** para **Botica Marifarma** (UNSA • EPIS • Semestre 2026-B).

## 🌐 Ver en vivo (GitHub Pages)

👉 **[Abrir Visor Interactivo en GitHub Pages](https://jperezh04.github.io/innofarma-arquitectura/)**

### Enlaces directos por vista
- **Vista Física Oficial (V01.00):** [fig5_1_vista_fisica_despliegue.html](https://jperezh04.github.io/innofarma-arquitectura/#fig5_1_vista_fisica_despliegue.html)
- **Vista Lógica Oficial (V01.00):** [fig3_1_interconexion_modulos.html](https://jperezh04.github.io/innofarma-arquitectura/#fig3_1_interconexion_modulos.html)
- **Vista de Procesos BPMN 2.0:** [fig4_1_bpmn_proceso_venta.html](https://jperezh04.github.io/innofarma-arquitectura/#fig4_1_bpmn_proceso_venta.html)

---

## 💻 Clonar y abrir localmente

No requiere dependencias ni servidor adicional. Puedes clonarlo y abrir `index.html` directamente en cualquier navegador:

```bash
git clone https://github.com/jperezh04/innofarma-arquitectura.git
cd innofarma-arquitectura
```

Luego abre el archivo `index.html` en tu navegador web (Chrome, Edge, Firefox).

---

## 📂 Estructura de Diagramas Incluidos

| Archivo | Vista / Módulo | Descripción |
|---|---|---|
| `index.html` | **Visor Principal** | Panel lateral jerárquico con buscador, filtro por EDU/ILA y leyenda semántica |
| `fig5_1_vista_fisica_despliegue.html` | **1. Vista Física (Oficial)** | Arquitectura de despliegue de 2 locales, Admin remota y túneles WireGuard |
| `fig5_2_flujo_modo_offline.html` | 1. Vista Física (Anexo) | Flujo operativo en modo offline y stock segmentado (`IndexedDB` / `Dexie.js`) |
| `fig5_3_secuencia_sincronizacion.html` | 1. Vista Física (Anexo) | Secuencia de sincronización e idempotencia post-corte (`UUID v4`) |
| `fig5_4_secuencia_acceso_remoto.html` | 1. Vista Física (Anexo) | Secuencia de acceso remoto seguro de la Administradora (`WireGuard QR`) |
| `fig5_5_comparativa_arquitecturas.html` | 1. Vista Física (Anexo) | Comparativa arquitectónica: Servidor Local vs Nube |
| `fig3_1_interconexion_modulos.html` | **2. Vista Lógica (Oficial)** | Diagrama de clases y relaciones de dominio (`EDU-0002` a `EDU-0013`) |
| `fig1_1_arquitectura_generica.html` | 2. Vista Lógica (Anexo) | Arquitectura genérica modular en 5 capas |
| `fig4_1_bpmn_proceso_venta.html` | **3. Vista de Procesos (BPMN)** | Orquestación global de venta en mostrador (BPMN 2.0 en 5 carriles) |
| `fig4_2_secuencia_proceso_venta.html` | `EDU-0004` / `ILA-0005` | Venta transaccional y bloqueo pesimista FEFO (`SELECT FOR UPDATE`) |
| `fig4_8_secuencia_idempotencia_wan.html` | `EDU-0004` / `ILA-0008` | Manejo de idempotencia ante reintentos WAN (`UUID v4`) |
| `fig4_7_secuencia_anulacion_venta.html` | `EDU-0004` / `ILA-0006, 0007` | Anulación de venta, reversión al lote original y compensación en caja |
| `fig4_5_secuencia_inventario_fefo.html` | `EDU-0002` / `ILA-0001` | Ingreso de lotes y validación sanitaria de caducidad (>180 días) |
| `fig4_9_secuencia_busqueda_fefo.html` | `EDU-0002` / `ILA-0002` | Búsqueda indexada FEFO por sucursal (`Index Scan`) |
| `fig4_4_secuencia_catalogo_medicamentos.html` | `EDU-0005, 0008` / `ILA-0009, 0021` | Catálogo DIGEMID y factores de fraccionamiento (caja / blíster / unidad) |
| `fig4_6_secuencia_caja_arqueo.html` | `EDU-0011` / `ILA-0033, 0035` | Apertura de sesión de caja y arqueo ciego de turno |
| `fig4_3_secuencia_control_rbac.html` | `EDU-0006` / `ILA-0013..0015` | Autenticación (`Argon2id`), middleware RBAC y auditoría |
