# Metadaten Board -- Concept Map

**Source:** 20260413_NFDI4ING-RDMBasic4Engineers-3_Metadaten-Board-DI.pdf
**Context:** NFDI4ING RDM Basics for Engineers, Teil 3 -- visual concept board used during the metadata session

---

## Overview

This is a visual concept board mapping **information necessary to find, understand, and use data** of different types. It combines two views:

1. A **mind-map** of metadata fields organized by data type and purpose
2. The **DataCite metadata schema** showing mandatory, recommended, and optional fields

---

## Metadata by Data Type and Purpose

The board categorizes metadata needs across four data types and three purposes:

### Data Types
- **General information**
- **Simulation data**
- **Experimental data**
- **Survey data**
- **Software**

### Purpose Categories (color-coded)
- **To search for** (blue) -- metadata needed to find data
- **To understand** (magenta) -- metadata needed to comprehend data
- **To use** (yellow) -- metadata needed to work with data

### Key Metadata Fields

#### General Information
| Field | Search | Understand | Use |
|-------|--------|-----------|-----|
| Aufnahmedatum und Uhrzeit (recording date/time) | x | | |
| Beschreibung des Versuchsaufbaus / Versioning | x | x | |
| Sensorik (sensor types and methods) | | x | |
| Aufloesung (zeitlich, raeumlich) + Referenz | | x | x |
| Einheiten (units) | | x | x |
| Dokumentation nicht-sensorischer Informationen | | | x |
| Experimentelle Simulation: Besondere Ereignisse | | x | |

#### Simulation-Specific
| Field | Search | Understand | Use |
|-------|--------|-----------|-----|
| Modellaufbau (Modellbild) | x | | |
| Messstellenplan | | x | |
| Messmethoden | | | x |
| Ersteller/Verfasser der Daten | | | x |
| Beschreibung der Primaerdaten | | x | x |
| Beschreibung der Algorithmen zur Generierung der Sekundaerdaten | | x | |
| Angabe der Eingabeparameter | x | | |
| Auffaelligkeiten waehrend der Datenerhebung | x | | |
| Eingangsparameter und Annahmen | x | x | |
| Numerische Simulation: Randbedingungen | | x | |
| Grund der Simulation/Messung | | x | x |
| Gemessene Groessen | (listed separately) | | |
| Messtechnik | (listed separately) | | |
| Unsicherheit | (listed separately) | | |
| Beteiligte | (listed separately) | | |

---

## DataCite Metadata Schema

The board also shows the DataCite metadata schema fields, organized by category and obligation level:

### Identifikation (Identification)
| Field | Level |
|-------|-------|
| **Identifier** | Mandatory |
| **AlternateIdentifier** | Recommended |
| **Version** | Recommended |
| **PublicationYear** | Mandatory |
| **Date** | Recommended |

### Beschreibung (Description)
| Field | Level |
|-------|-------|
| **Title** | Mandatory |
| **Description** | Recommended |
| **Subject** | Recommended |
| **Language** | Optional |
| **GeoLocation** | Optional |

### Verbindungen (Connections)
| Field | Level |
|-------|-------|
| **RelatedIdentifier** | Recommended |
| **RelatedItem** | Optional |
| **FundingReference** | Optional |
| **Creator** | Mandatory |
| **Publisher** | Mandatory |
| **Contributor** | Recommended |

### Technische Informationen (Technical Information)
| Field | Level |
|-------|-------|
| **ResourceType** | Mandatory |
| **Size** | Optional |
| **Format** | Optional |

### Nutzung und Rechte (Usage and Rights)
| Field | Level |
|-------|-------|
| **Rights** | Recommended |

### Obligation Levels
- **Pflichtfeld** (Mandatory) -- must be filled
- **Empfohlen** (Recommended) -- should be filled
- **Optional** -- can be filled
