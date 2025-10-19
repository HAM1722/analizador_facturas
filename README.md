
[README.md](https://github.com/user-attachments/files/22989944/README.md)
# Analizador de Facturas EMCALI

Sistema para extraer información de facturas EMCALI en PDF y generar informes en DOCX.

## Objetivo

Extraer datos específicos de facturas de EMCALI (Empresas Municipales de Cali) y generar informes con la información extraída.

## Datos Extraídos

- **Número de Contrato**
- **Total a Pagar**
- **Tipo de Documento**
- **Servicios Incluidos:**
  - Energía Eléctrica (EMCALI)
  - Aseo (PROMOCALI)
  - Alumbrado Público (EMCALI)
  - Tasa de Seguridad (EMCALI)

## Instalación

1. Instalar dependencias:
```cmd
python -m pip install pdfplumber python-docx pandas rich tqdm
```

2. Para extracción avanzada (opcional):
```cmd
python -m pip install easyocr opencv-python pillow
```

## Uso

### Extraer texto del PDF
```cmd
python extractor_avanzado.py
```

### Generar informe simple
```cmd
python generar_informe_emcali_simple.py
```

## Archivos Generados

- `texto_extraido.txt` - Texto extraído del PDF
- `outputs/docx/INFORME_EMCALI_SIMPLE.docx` - Informe final

## Estructura del Proyecto

```
analizador_facturas/
├─ data/raw/                    # PDFs de facturas EMCALI
├─ outputs/docx/                # Informes generados
├─ extractor_avanzado.py        # Extracción de texto
├─ generar_informe_emcali_simple.py  # Generador de informes
└─ README.md
```
