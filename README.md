## TP18 — Gestión Centralizada de Vulnerabilidades con OWASP DefectDojo

 Integración de **OWASP DefectDojo Community Edition** para consolidar, desduplicar y auditar los hallazgos de ciberseguridad provenientes de OWASP ZAP (DAST), Threagile (Threat Modeling), Semgrep (SAST), Trivy (SCA/Container/IaC) y Gitleaks (Secret Scanning).

 ### Arquitectura de Integración en 4 Fases

 Fase;Herramienta;Función;Mecanismo
 Fase 1;Docker Buildx;Compilación inmutable;Exporta app-image.tar
 Fase 2;OWASP ZAP / Threagile / Semgrep / Trivy / Gitleaks;Auditoría multidominio;Genera reportes JSON/XML estructurados
 Fase 3;OWASP DefectDojo;Vulnerability Management;Ingestión vía API v2 y deduplicación
 Fase 4;Helm & K8s;Despliegue a producción;Release verificado en Kubernetes
