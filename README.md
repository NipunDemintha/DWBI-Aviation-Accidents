# ✈️ Aviation Accidents - Data Warehousing & Business Intelligence

## 📌 Project Overview
End-to-end DW & BI solution using NTSB Aviation Accidents dataset.
Implemented as part of IT3021 - Data Warehousing & Business Intelligence module at SLIIT.

---

## 📦 Assignment 1 - Data Warehouse & ETL

### Architecture
- 3-layer: Source DB → Staging → Data Warehouse
- Snowflake Schema with 6 Dimension tables + 1 Fact table

### SSIS Packages
| Package | Description |
|---------|-------------|
| Assignment_1_Load_Staging.dtsx | Extract from CSV & TXT → Staging |
| Assignment_1_Load_DW.dtsx | Transform & Load → Data Warehouse |
| Assignment_1_Update_Fact.dtsx | Accumulating Snapshot Fact Table |

### Key Concepts
- SCD Type 2 (DimPilot)
- Surrogate Keys
- Stored Procedures
- Event Handlers

### Database Stats
| Table | Rows |
|-------|------|
| DimLocation | 53,911 |
| DimAccident | 69,026 |
| DimAircraft | 48,968 |
| DimPilot | 20,000 |
| FactFlight | 10,011 |

---

## 📊 Assignment 2 - OLAP & Business Intelligence

### SSAS Cube
- Cube: Cube_Assignment_Retail
- Measures: Fact Flight Count, Txn Process Time Hours
- Dimensions: DimDate, DimPilot, DimAircraft, DimAccident
- Hierarchies: DH_01 (Year→Quarter→Month→Date), DH_02 (Year→Month→Date), Pilot_Hierarchy (Country→State→City→ZipCode)

### OLAP Operations (Excel)
| Operation | Description |
|-----------|-------------|
| Roll-Up | Aggregated flights by Weather Condition |
| Drill-Down | Year → Quarter → Month |
| Slice | Filtered by Engine Type |
| Dice | Aircraft Category + Weather Condition |
| Pivot | Rotated axes for alternative view |

### Power BI Reports
| Report | Description |
|--------|-------------|
| Report 1 | Matrix Visual - Flight counts by Country & Year |
| Report 2 | Cascading Slicers + Bar, Pie & Column Charts |
| Report 3 | Hierarchical Drill-Down using DH_01 |
| Report 4 | Drill-Through from Map to detail page |

---

## 🛠️ Tools & Technologies
- SQL Server 2019
- SQL Server Management Studio (SSMS)
- Visual Studio 2022 + SSIS + SSAS
- Microsoft Excel
- Power BI Desktop & Service

---

## 👨‍💻 Author
**Nipun Demintha** -
DS Undergraduate - SLIIT (Year 3 Semester 2)
