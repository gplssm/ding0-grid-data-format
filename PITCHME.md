# A new data format for ding0 grid data

---

## Reviewing CSV data format developed by Jonas

---

@snap[midpoint span-40]

### HV/MV Transformers

| name       | description                       | unit           |
|------------|-----------------------------------|----------------|
| id         | unambiguous unique numer          | integer        |
| run_id     | time and date of table generation | yyyyMMddhhmmss |
| geom       | geometric coordinates             | WGS84 POINT    |
| name       | FIXME                             | string         |
| voltage_op | FIXME                             | float          |
| s_nom      | nominal apparent power as float   | kVA            |
| x          | as float                          | Ohm            |
| r          | as float                          | Ohm            |

@snapend
